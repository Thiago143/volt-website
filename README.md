# Volt Solutions - Website Institucional

Site institucional da Volt Solutions - Infraestrutura, Automação e Inteligência Conectada.

## 🌐 URLs

- **Site Principal**: https://voltsolutions.tec.br (aguardando propagação DNS)
- **GitHub Pages**: https://thiago143.github.io/volt-website/
- **Repositório**: https://github.com/Thiago143/volt-website

## 📧 Emails Configurados

- **Principal**: thiago@voltsolutions.tec.br
- **Aliases**:
  - contato@voltsolutions.tec.br (formulário do site)
  - vendas@voltsolutions.tec.br
  - projetos@voltsolutions.tec.br
  - suporte@voltsolutions.tec.br
  - financeiro@voltsolutions.tec.br
  - noreply@voltsolutions.tec.br

## 🛠 Tecnologias

- **Frontend**: HTML5, CSS3, JavaScript vanilla
- **Design**: Responsivo, mobile-first
- **Formulário**: FormSubmit (integração com email)
- **Hospedagem**: GitHub Pages
- **Email**: Hostinger Business Starter
- **Domínio**: Registro.br

## 📁 Estrutura do Projeto

```
volt-website/
├── index.html              # Landing page principal
├── CNAME                   # Configuração domínio GitHub Pages
├── README.md               # Este arquivo
├── docs/                   # Documentação técnica
│   ├── DNS-SETUP.md       # Configuração DNS completa
│   └── EMAIL-SETUP.md     # Configuração de email
└── INSTRUCOES_DNS_REGISTRO_BR.md  # Instruções originais DNS
```

## 🎨 Características do Site

### Seções
- **Hero**: Apresentação principal com CTA
- **Serviços**: 4 principais serviços (TI, Redes, CFTV, Automação)
- **Sobre**: Diferenciais da empresa
- **Contato**: Formulário integrado com email

### Design
- Paleta de cores: Azul escuro (#0F172A), Ciano (#22D3EE), Amarelo (#FACC15)
- Tipografia: Poppins (Google Fonts)
- Animações sutis e efeitos de hover
- 100% responsivo (desktop, tablet, mobile)

### Funcionalidades
- Menu hambúrguer em mobile
- Scroll suave entre seções
- Formulário de contato funcional
- Header com efeito de scroll
- Logo animado

## 🚀 Deploy

### Status Atual
- ✅ Site publicado no GitHub Pages
- ✅ Arquivo CNAME configurado
- ⏳ Aguardando propagação DNS (1-24h)
- ⏳ HTTPS será ativado automaticamente após propagação

### Como Atualizar o Site

1. **Editar arquivo**:
   ```bash
   # Edite index.html ou outros arquivos
   ```

2. **Commit e push**:
   ```bash
   git add .
   git commit -m "descrição da alteração"
   git push origin main
   ```

3. **Deploy automático**: GitHub Pages atualiza automaticamente em ~1 minuto

## 🔧 Configurações Técnicas

### DNS (Registro.br)
- 4 registros A apontando para GitHub Pages
- CNAME www → thiago143.github.io
- Registros MX, SPF, DKIM para email Hostinger

Ver documentação completa: [`docs/DNS-SETUP.md`](docs/DNS-SETUP.md)

### Email (Hostinger)
- Plano: Business Starter (R$ 3,45/mês)
- 1 conta principal + 6 aliases configurados
- Webmail: https://webmail.hostinger.com

Ver documentação completa: [`docs/EMAIL-SETUP.md`](docs/EMAIL-SETUP.md)

## ✅ Checklist de Verificação

### Site
- [x] HTML criado e validado
- [x] Design responsivo implementado
- [x] Formulário de contato configurado
- [x] Repository GitHub criado
- [x] GitHub Pages ativado
- [x] Arquivo CNAME adicionado
- [ ] DNS propagado (aguardando)
- [ ] HTTPS ativo (após DNS propagar)

### Email
- [x] Conta Hostinger contratada
- [x] Conta principal criada
- [x] Aliases configurados
- [x] Registros DNS adicionados
- [ ] DNS propagado (aguardando)
- [ ] Teste de envio/recebimento (após DNS)

## 📝 Próximos Passos

1. **Aguardar propagação DNS** (1-24 horas)
2. **Testar site**: Acessar https://voltsolutions.tec.br
3. **Testar email**: Enviar/receber emails de teste
4. **Testar formulário**: Submeter formulário do site
5. **Ativar HTTPS**: Verificar se GitHub ativou certificado SSL
6. **Configurar email no celular/desktop** (opcional)

## 🆘 Troubleshooting

### Site não carrega
```bash
# Verificar se DNS propagou
dig voltsolutions.tec.br A +short
# Deve retornar: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
```

### Email não funciona
```bash
# Verificar registros MX
dig voltsolutions.tec.br MX +short
# Deve retornar: 5 mx1.hostinger.com, 10 mx2.hostinger.com
```

Ver mais em: [`docs/DNS-SETUP.md`](docs/DNS-SETUP.md)

## 📞 Informações da Empresa

**Volt Solutions**
- CNPJ: 28.353.782/0001-61
- Endereço: Rua Tereza Cavalcanti, 67 – Rio de Janeiro/RJ
- Telefone: (21) 96592-6943
- Email: contato@voltsolutions.tec.br

## 📄 Licença

© 2025 Volt Solutions. Todos os direitos reservados.

---

**Data de criação**: 27 de novembro de 2025
**Última atualização**: 27 de novembro de 2025
