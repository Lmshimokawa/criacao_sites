# Lição O4 — Segurança e LGPD

> **Fase**: O — Operação & Infraestrutura  
> **Status**: ✅ Concluída  
> **Data de conclusão**: 2025-01-28

---

## 🎯 Objetivo da Lição

Garantir que o site da Verde Barro trate dados pessoais de forma transparente e em conformidade com a LGPD (Lei Geral de Proteção de Dados), com política de privacidade publicada e mecanismo de consentimento quando aplicável.

---

## 📚 Camada 1: Conceitos

### LGPD em uma frase

**LGPD**: Lei que exige que empresas informem claramente quais dados coletam, para que usam e com quem compartilham, e que obtenham consentimento (ou outra base legal) para o tratamento.

### Bases legais para tratamento (resumo)

| Base | Quando usar |
|------|-------------|
| **Consentimento** | Newsletter, cookies não essenciais, marketing |
| **Execução de contrato** | Pedido, pagamento, agendamento |
| **Legítimo interesse** | Segurança, antifraude, melhorias do site |
| **Obrigação legal** | Notas fiscais, retenção por lei |

### O que o site da Verde Barro coleta

| Dado | Onde | Base sugerida |
|------|------|----------------|
| Nome, e-mail, WhatsApp | Solicitação de experiência, checkout, contato | Execução de contrato / pré-contrato |
| Endereço | Solicitação (workshop), entrega (peças) | Execução de contrato |
| E-mail (newsletter) | Formulário "Fique por dentro" | Consentimento |
| Dados de pagamento | Stripe (não ficam no seu servidor) | Execução de contrato |

---

## 📄 Camada 2: Política de Privacidade

### Estrutura recomendada

1. **Quem somos** — identificação da Verde Barro (nome, CNPJ/CPF se houver, contato).
2. **Dados que coletamos** — lista clara por finalidade (pedidos, newsletter, contato).
3. **Para que usamos** — finalidade de cada uso (ex.: enviar confirmação, enviar newsletter).
4. **Com quem compartilhamos** — Stripe, Supabase, Resend, Vercel; nenhuma venda de dados.
5. **Por quanto tempo guardamos** — prazos ou critérios (ex.: enquanto a conta existir, 5 anos para fins fiscais).
6. **Seus direitos** — acesso, correção, exclusão, portabilidade, revogar consentimento, reclamação na ANPD.
7. **Cookies e tecnologias semelhantes** — o que usa (ex.: essenciais, analytics) e como desativar quando aplicável.
8. **Alterações** — como avisamos mudanças (ex.: data da última atualização, link na política).
9. **Contato** — e-mail ou canal para dúvidas e exercício de direitos.

### Texto-base para a Verde Barro (adaptar e publicar)

Use o bloco abaixo como **rascunho**. Ajuste nomes, contatos e prazos antes de publicar. Recomenda-se revisão por advogado.

---

**POLÍTICA DE PRIVACIDADE — Verde Barro Cerâmica**

**Última atualização:** 2026-02-01

**1. Quem somos**  
Verde Barro Cerâmica (“nós”) oferece experiências de cerâmica (workshops) e peças autorais. Esta política explica como tratamos seus dados pessoais neste site.

**2. Dados que coletamos**  
- **Solicitação de experiência:** nome, e-mail, WhatsApp, endereço onde deseja realizar o workshop, data desejada, número de participantes e forma de pagamento (individual ou compartilhado).  
- **Compra de peças:** nome, e-mail, WhatsApp (opcional), endereço de entrega e dados necessários ao pagamento (processados pelo Stripe; nós não armazenamos número de cartão).  
- **Newsletter:** e-mail e, se informado, nome.  
- **Contato:** dados que você enviar por WhatsApp ou por outros canais indicados no site.

**3. Para que usamos**  
- Cumprir pedidos, agendamentos e envio de peças.  
- Enviar confirmações, avisos e comunicações relacionadas ao serviço.  
- Enviar newsletter somente se você tiver se inscrito (consentimento).  
- Melhorar o site e a experiência do usuário (incluindo analytics, quando houver).  
- Cumprir obrigações legais (ex.: fiscais).

**4. Com quem compartilhamos**  
Seus dados podem ser processados por:  
- **Stripe** — processamento de pagamentos.  
- **Supabase** — armazenamento seguro dos dados do site.  
- **Resend** — envio de e-mails transacionais e newsletter.  
- **Vercel** — hospedagem do site.  
Não vendemos nem alugamos seus dados a terceiros.

**5. Por quanto tempo guardamos**  
- Dados de pedidos e solicitações: pelo tempo necessário ao cumprimento do contrato e às obrigações legais (ex.: 5 anos para fins fiscais).  
- Newsletter: até você cancelar a inscrição ou solicitar exclusão.  
- Logs e dados técnicos: conforme política de retenção dos provedores e necessidade de segurança.

**6. Seus direitos (LGPD)**  
Você pode: acessar, corrigir, solicitar exclusão ou portabilidade dos seus dados, revogar consentimento (ex.: newsletter) e apresentar reclamação à ANPD. Para exercer esses direitos, use o canal de contato abaixo.

**7. Cookies e tecnologias**  
O site pode usar cookies essenciais (funcionamento do site) e, se configurado, cookies de analytics. Você pode configurar o navegador para recusar cookies não essenciais; a experiência pode ser afetada.

**8. Alterações**  
Podemos atualizar esta política. A data da última versão aparece no topo. O uso continuado do site após alterações pode ser considerado aceite; para mudanças relevantes, podemos avisar por e-mail ou destaque no site.

**9. Contato**  
Para dúvidas ou para exercer seus direitos: [e-mail ou formulário de contato].

---

### Onde publicar no site

- **Página fixa:** `/legal/privacidade` (ou `/politica-de-privacidade`).  
- **Link no footer:** “Política de privacidade” em todas as páginas.  
- **Link em formulários:** próximo à newsletter e, se houver, aos campos de dados pessoais (ex.: “Ao enviar, você concorda com nossa [Política de privacidade].”).

---

## ✅ Camada 3: Consentimento configurado

### Quando pedir consentimento

- **Newsletter:** obrigatório (consentimento explícito).  
- **Cookies não essenciais (ex.: analytics):** recomendável banner ou aviso + opção de aceitar/recusar.  
- **Pedidos/solicitações:** a base é execução de contrato; ainda assim, é boa prática informar na própria tela que os dados serão usados para processar o pedido e conforme a Política de privacidade.

### Opções de implementação

| Abordagem | Complexidade | Uso sugerido |
|-----------|--------------|--------------|
| **Checkbox “Li e aceito a Política de privacidade”** no formulário de newsletter | Baixa | Obrigatório na newsletter |
| **Banner de cookies** (aceitar / recusar / só essenciais) | Média | Se usar analytics ou cookies de terceiros |
| **Página “Termos e Privacidade”** com link no footer | Baixa | Obrigatório (já previsto no R3) |

### Checklist mínimo para Verde Barro

- [x] Página **Política de privacidade** publicada em `/legal/privacidade`.  
- [x] Link para a política no **footer** do site.  
- [x] No formulário de **newsletter**: checkbox “Aceito receber e-mails da Verde Barro e li a [Política de privacidade]” e só inscrever se marcado.  
- [ ] Se usar analytics ou cookies de terceiros: aviso/banner de cookies (opcional).  
- [ ] Na **solicitação de experiência** e no **checkout**: menção breve + link à Política (quando implementar formulários).

---

## 🛠️ Entregáveis da Lição O4

| Entregável | Status | Observação |
|------------|--------|------------|
| Política de privacidade (texto-base) | ✅ | Incluída neste doc e publicada em `/legal/privacidade` |
| Página `/legal/privacidade` no site | ✅ | `verde-barro-site/src/app/(site)/legal/privacidade/page.tsx` |
| Link no footer para Política de privacidade | ✅ | Footer atualizado |
| Checkbox de consentimento no formulário de newsletter | ✅ | Checkbox obrigatório; API exige `aceite_privacidade: true`; campo `aceite_privacidade` no Supabase |
| Banner de cookies (opcional) | [ ] Opcional | Implementar se usar analytics/cookies de terceiros |

---

## 📌 Migração Supabase (newsletter)

Se o projeto já tinha a tabela `newsletter` sem a coluna de consentimento, execute no SQL Editor do Supabase:

```sql
ALTER TABLE newsletter ADD COLUMN IF NOT EXISTS aceite_privacidade BOOLEAN DEFAULT true;
```

---

**Status**: ✅ Concluída  
**Data de conclusão**: 2025-01-28  
**Última atualização**: 2025-01-28
