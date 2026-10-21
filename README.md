# Vitrine Móvel

Portefólio público do **Vitrine Móvel**, uma plataforma de publicidade digital pensada para gerir clientes, campanhas e a exibição de conteúdos em tablets.

> Este repositório é apenas de apresentação. O código-fonte principal permanece privado por conter lógica de produto, integrações e configuração de infraestrutura.

## Capturas reais

Capturas reais do ambiente de demonstração (staging), com versões desktop e mobile. O e-mail da conta e os dados de acesso não fazem parte das imagens.

### Área do motorista

Dashboard com clientes, anúncios, limites por tablet e resumo de utilização. A versão mobile inclui o resumo e o primeiro cartão completo.

<table>
<tr><th>Desktop</th><th>Mobile</th></tr>
<tr>
<td width="70%" valign="top"><a href="screenshots/desktop-01-dashboard.jpg"><img src="screenshots/desktop-01-dashboard.jpg" alt="Área do motorista em desktop" width="100%"></a></td>
<td width="30%" valign="top"><a href="screenshots/mobile-01-dashboard.jpg"><img src="screenshots/mobile-01-dashboard.jpg" alt="Área do motorista em mobile" width="100%"></a></td>
</tr>
</table>

### Registo de cliente e campanha

Formulário existente com dados do cliente, datas da campanha, envio de media e duração de exibição.

<table>
<tr><th>Desktop</th><th>Mobile</th></tr>
<tr>
<td width="70%" valign="top"><a href="screenshots/desktop-02-registar-cliente.jpg"><img src="screenshots/desktop-02-registar-cliente.jpg" alt="Registo de cliente e campanha em desktop" width="100%"></a></td>
<td width="30%" valign="top"><a href="screenshots/mobile-02-registar-cliente.jpg"><img src="screenshots/mobile-02-registar-cliente.jpg" alt="Registo de cliente e campanha em mobile" width="100%"></a></td>
</tr>
</table>

### Gestão de divulgação

Janela de edição de um anúncio de demonstração, com opções de media, datas e tempo de exibição.

<table>
<tr><th>Desktop</th><th>Mobile</th></tr>
<tr>
<td width="70%" valign="top"><a href="screenshots/desktop-03-editar-divulgacao.jpg"><img src="screenshots/desktop-03-editar-divulgacao.jpg" alt="Gestão de divulgação em desktop" width="100%"></a></td>
<td width="30%" valign="top"><a href="screenshots/mobile-03-editar-divulgacao.jpg"><img src="screenshots/mobile-03-editar-divulgacao.jpg" alt="Gestão de divulgação em mobile" width="100%"></a></td>
</tr>
</table>

### Plano e assinatura

Resumo de um plano de teste em staging, com estado da assinatura e regras de mudança de plano. Os valores e as datas correspondem ao ambiente de demonstração.

<table>
<tr><th>Desktop</th><th>Mobile</th></tr>
<tr>
<td width="70%" valign="top"><a href="screenshots/desktop-04-assinatura.jpg"><img src="screenshots/desktop-04-assinatura.jpg" alt="Plano e assinatura em desktop" width="100%"></a></td>
<td width="30%" valign="top"><a href="screenshots/mobile-04-assinatura.jpg"><img src="screenshots/mobile-04-assinatura.jpg" alt="Plano e assinatura em mobile" width="100%"></a></td>
</tr>
</table>

> A galeria documenta interfaces observadas; não representa validação de pagamentos ou de gravação de dados. As janelas foram abertas sem submeter alterações. O dashboard administrativo e a reprodução no tablet não foram capturados nesta sessão.



## Sobre o projeto

O Vitrine Móvel nasceu da ideia de transformar tablets em pontos de divulgação digital geridos de forma centralizada.

A plataforma foi pensada para permitir que motoristas/operadores cadastrem clientes e campanhas, enviem imagens ou vídeos, iniciem sessões de divulgação e acompanhem informações relacionadas com planos, acesso e utilização.

Além da experiência do utilizador, o projeto envolve autenticação, pagamentos por subscrição, controlo de acesso, armazenamento de media, infraestrutura cloud, monitorização e preparação para distribuição como aplicação.

## O que trabalhei no projeto

- Autenticação e gestão de utilizadores
- Perfis e regras de acesso
- Gestão de clientes e campanhas
- Upload e apresentação de imagens e vídeos
- Planos de subscrição e integração com Stripe
- Validação de webhooks e idempotência em pagamentos
- Integração com Supabase
- Infraestrutura com Cloudflare Workers, D1 e R2
- Monitorização de erros com Sentry
- Regras de sessão e utilização em tablets
- Estrutura para suporte ao utilizador
- Preparação do produto para publicação futura em Google Play e Apple App Store

## Tecnologias

- **Supabase** — autenticação e serviços de backend
- **Stripe** — subscrições e pagamentos
- **Cloudflare Workers** — backend/edge runtime
- **Cloudflare D1** — base de dados
- **Cloudflare R2** — armazenamento de ficheiros/media
- **Sentry** — monitorização e observabilidade
- **Git / GitHub** — versionamento e gestão do projeto

## Arquitetura simplificada

```mermaid
flowchart LR
    U[Utilizador / Tablet] --> A[Aplicação Vitrine Móvel]
    A --> S[Supabase Auth]
    A --> W[Cloudflare Worker]
    W --> D[(D1)]
    W --> R[(R2)]
    W --> P[Stripe]
    A --> E[Sentry]
```

## Estado do projeto

Projeto em desenvolvimento ativo.

Entre os pontos já trabalhados estão autenticação, onboarding, regras de sessão, integração Stripe, webhook, idempotência, integração Supabase, infraestrutura Cloudflare e monitorização com Sentry.

Ainda fazem parte do roadmap funcionalidades como recuperação de palavra-passe, gestão completa de plano e pagamento, relatórios, suporte ao utilizador, reforço de segurança, Google Login/MFA e preparação final para publicação nas lojas.

## Screenshots
As capturas em desktop e mobile estão na [galeria de interfaces](#capturas-reais) e na pasta [`screenshots/`](screenshots/).

## Repositório privado

O repositório de desenvolvimento permanece privado por motivos de segurança e proteção do produto.

## Autor

**Hasan Marouf**  
Web Developer Júnior — Coimbra, Portugal
