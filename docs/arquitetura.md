# Arquitetura — visão pública

Esta documentação mostra apenas a arquitetura de alto nível do Vitrine Móvel.

## Componentes principais

### Aplicação
Interface utilizada para autenticação, gestão de clientes, campanhas, sessão de divulgação e acesso às áreas da conta.

### Supabase
Usado no fluxo de autenticação e gestão de utilizadores.

### Cloudflare
A infraestrutura utiliza Workers para execução backend, D1 para dados e R2 para media.

### Stripe
Responsável pelos fluxos relacionados com subscrições e pagamentos.

Foram trabalhados mecanismos de:
- reaproveitamento de Customer por e-mail
- rastreio de checkout session
- idempotência
- validação de webhook
- prevenção de criação duplicada de subscrições

### Sentry
Utilizado para monitorização técnica e diagnóstico de erros.

## Segurança

Este repositório público não contém:
- ficheiros `.env`
- secrets
- chaves de API
- credenciais
- código-fonte de produção
- configuração privada de infraestrutura
