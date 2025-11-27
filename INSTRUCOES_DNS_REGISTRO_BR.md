# Instruções de Configuração DNS - Registro.br

## Configuração do domínio voltsolutions.tec.br para GitHub Pages

Para finalizar a hospedagem do site, você precisa configurar os registros DNS no **Registro.br**.

### Passo a passo:

1. **Acesse o painel do Registro.br**
   - Vá para: https://registro.br
   - Faça login com sua conta

2. **Acesse a configuração de DNS do domínio**
   - Clique no domínio `voltsolutions.tec.br`
   - Selecione "Editar Zona DNS" ou "Configurar DNS"

3. **Configure os registros DNS**

   **IMPORTANTE**: Delete todos os registros A e AAAA existentes antes de adicionar os novos.

   **Adicione os seguintes registros do tipo A** (para o domínio raiz `@`):
   ```
   Tipo: A
   Nome: @ (ou deixe em branco)
   Valor: 185.199.108.153
   TTL: 3600 (ou padrão)

   Tipo: A
   Nome: @ (ou deixe em branco)
   Valor: 185.199.109.153
   TTL: 3600 (ou padrão)

   Tipo: A
   Nome: @ (ou deixe em branco)
   Valor: 185.199.110.153
   TTL: 3600 (ou padrão)

   Tipo: A
   Nome: @ (ou deixe em branco)
   Valor: 185.199.111.153
   TTL: 3600 (ou padrão)
   ```

   **Adicione um registro CNAME para www** (opcional, mas recomendado):
   ```
   Tipo: CNAME
   Nome: www
   Valor: thiago143.github.io
   TTL: 3600 (ou padrão)
   ```

4. **Salve as alterações**

5. **Aguarde a propagação DNS**
   - A propagação pode levar de 15 minutos a 48 horas
   - Normalmente leva cerca de 1-2 horas no Brasil

### Verificando a configuração:

Após algumas horas, você pode verificar se está funcionando:

**Comando no terminal:**
```bash
dig voltsolutions.tec.br +short
```

Deve retornar os 4 IPs do GitHub Pages.

**Teste no navegador:**
- http://voltsolutions.tec.br
- https://voltsolutions.tec.br (HTTPS pode levar até 24h para ser ativado automaticamente)

### Observações importantes:

1. **HTTPS**: O GitHub Pages ativará automaticamente o certificado SSL (HTTPS) após a propagação DNS. Isso pode levar até 24 horas.

2. **Email não é afetado**: Esta configuração é apenas para o site. Os registros MX do seu email Hostinger devem permanecer intactos.

3. **Arquivo CNAME**: O arquivo `CNAME` no repositório já está configurado com `voltsolutions.tec.br`.

### Caso algo não funcione:

1. Verifique se removeu todos os registros A antigos
2. Confirme que os 4 IPs estão corretos
3. Aguarde mais tempo para propagação DNS
4. Execute: `dig voltsolutions.tec.br` para verificar os registros

---

## Status atual:

✅ Site criado
✅ Repositório GitHub criado: https://github.com/Thiago143/volt-website
✅ GitHub Pages ativado
✅ Arquivo CNAME configurado
⏳ **PENDENTE**: Configuração DNS no Registro.br (você precisa fazer este passo)

Após configurar o DNS, o site estará disponível em: https://voltsolutions.tec.br
