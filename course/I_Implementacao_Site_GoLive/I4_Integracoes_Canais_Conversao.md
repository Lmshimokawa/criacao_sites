# Lição I4 — Integrações e Canais de Conversão

> **Fase**: I — Implementação de Site Completo e Go-Live  
> **Status**: 🔄 Em andamento  
> **Pré-requisito**: I3 (páginas, conteúdo e branding seguindo direção de design); insumos C3 e O

---

## Objetivo da Lição

Integrar **todos os canais de conversão** no front e no back: formulário de solicitação → API → banco; WhatsApp (env); agendamento (Cal.com); checkout (Stripe) quando aplicável. Validar **UX** (loading, erro, sucesso; mobile-first) e manter **polimento visual** dos fluxos no mesmo nível de qualidade da direção de design (I2/I3).

---

## Camada 1: Conceitos

### Formulário → API → banco

Formulário envia para API (ex.: `POST /api/solicitacao`), que persiste no banco. Usuário recebe feedback imediato (sucesso ou erro).

### Canais configuráveis

- **WhatsApp:** link com número de `NEXT_PUBLIC_WHATSAPP_NUMBER`.
- **Agendamento:** link Cal.com em `NEXT_PUBLIC_CAL_LINK` (Experiências, Contato).
- **Checkout:** Stripe com produtos/preços; fluxo até página de obrigado ou alternativa via WhatsApp.

### UX dos fluxos

Loading ("Enviando..."), erro (toast ou mensagem clara), sucesso (confirmação visível). Mobile-first; touch targets adequados.

---

## Camada 2: Aplicação — Verde Barro

| Canal | Front | Back |
|-------|-------|------|
| Solicitação | Form em Experiências | POST /api/solicitacao → Supabase |
| WhatsApp | Links Contato, Peças | env |
| Cal.com | Links Experiências, Contato | env |
| Checkout | Botão → Stripe ou WhatsApp | /api/checkout + webhook |
| Newsletter | Form Home | /api/newsletter (já integrado) |

### Entregáveis

- [ ] Formulário solicitação funcionando (loading/sucesso/erro).
- [ ] WhatsApp e Cal.com via env; links nas páginas corretas.
- [ ] Checkout ou fluxo alternativo claro.
- [ ] UX validada (fluxos fechados, tratamento de erros).

---

## Próximos passos

Seguir para **I5 — Go-Live, SEO e Verificação Final**.
