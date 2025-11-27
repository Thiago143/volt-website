# Configuração DNS - Volt Solutions

## Informações do Domínio

- **Domínio**: voltsolutions.tec.br
- **Registrador**: Registro.br
- **Data de configuração**: 27 de novembro de 2025

## Registros DNS Configurados

### Registros A (GitHub Pages - Site)

Configurados para hospedar o site institucional no GitHub Pages:

```
Tipo: A
Nome: voltsolutions.tec.br (ou @)
Valores:
  - 185.199.108.153
  - 185.199.109.153
  - 185.199.110.153
  - 185.199.111.153
TTL: Padrão
```

### Registro CNAME (WWW)

```
Tipo: CNAME
Nome: www.voltsolutions.tec.br
Valor: thiago143.github.io
TTL: Padrão
```

### Registros MX (Email - Hostinger)

Configurados para receber emails através da Hostinger:

```
Tipo: MX
Nome: voltsolutions.tec.br (ou @)
Valores:
  - 5 mx1.hostinger.com
  - 10 mx2.hostinger.com
TTL: 14400
```

### Registro TXT (SPF - Anti-spam)

Protege a reputação do domínio contra spam:

```
Tipo: TXT
Nome: voltsolutions.tec.br (ou @)
Valor: v=spf1 include:_spf.mail.hostinger.com ~all
TTL: 300
```

### Registros CNAME (DKIM - Autenticação de Email)

Melhoram a entregabilidade dos emails:

```
Tipo: CNAME
Nome: hostingermail-a._domainkey.voltsolutions.tec.br
Valor: hostingermail-a.dkim.mail.hostinger.com
TTL: 300

Tipo: CNAME
Nome: hostingermail-b._domainkey.voltsolutions.tec.br
Valor: hostingermail-b.dkim.mail.hostinger.com
TTL: 300

Tipo: CNAME
Nome: hostingermail-c._domainkey.voltsolutions.tec.br
Valor: hostingermail-c.dkim.mail.hostinger.com
TTL: 300
```

### Registros CNAME (Autoconfig - Configuração Automática de Email)

Permite configuração automática em clientes de email:

```
Tipo: CNAME
Nome: autoconfig.voltsolutions.tec.br
Valor: autoconfig.mail.hostinger.com
TTL: 300

Tipo: CNAME
Nome: autodiscover.voltsolutions.tec.br
Valor: autodiscover.mail.hostinger.com
TTL: 300
```

## Propagação DNS

- **Tempo estimado**: 15 minutos a 24 horas
- **Tempo médio no Brasil**: 1-2 horas

### Verificar propagação:

```bash
# Verificar registros A (site)
dig voltsolutions.tec.br A +short

# Verificar registros MX (email)
dig voltsolutions.tec.br MX +short

# Verificar CNAME www
dig www.voltsolutions.tec.br CNAME +short

# Verificar SPF
dig voltsolutions.tec.br TXT +short
```

## Troubleshooting

### Site não carrega

1. Verificar se os registros A propagaram: `dig voltsolutions.tec.br A +short`
2. Deve retornar os 4 IPs: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
3. Aguardar propagação DNS completa

### Email não recebe

1. Verificar registros MX: `dig voltsolutions.tec.br MX +short`
2. Deve retornar: `5 mx1.hostinger.com.` e `10 mx2.hostinger.com.`
3. Verificar configuração no painel Hostinger

### HTTPS não ativa

- O GitHub Pages ativa HTTPS automaticamente após a propagação DNS
- Pode levar até 24 horas após o domínio começar a responder
- Verificar em: Repositório GitHub > Settings > Pages > "Enforce HTTPS"

## Contatos de Suporte

- **Registro.br**: https://registro.br/suporte
- **Hostinger**: https://www.hostinger.com.br/suporte
- **GitHub Pages**: https://docs.github.com/pages

## Histórico de Alterações

| Data | Alteração | Responsável |
|------|-----------|-------------|
| 2025-11-27 | Configuração inicial DNS completa | Claude Code |
