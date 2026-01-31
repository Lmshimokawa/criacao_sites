# Lição O3 — Infraestrutura Básica

> **Objetivo**: Configurar ambiente de desenvolvimento e realizar primeiro deploy funcional.
> 
> **Pré-requisitos**: Lição O2 concluída (stack definida)

---

## 📚 Camada 1: Conceitos Fundamentais

### O que é "Infraestrutura" de um Site?

**Definição simples**: Toda a estrutura técnica que permite seu site existir e funcionar na internet — desde onde o código mora até onde os dados são salvos.

**Analogia**: Construir uma casa
- **Código** = Design da casa (planta, layout)
- **Repositório (Git)** = Arquivo com todos os projetos e versões
- **Hospedagem (Vercel)** = Terreno onde a casa é construída
- **Banco de dados (Supabase)** = Cofre onde guarda documentos importantes
- **Pagamentos (Stripe)** = Sistema de cobranças
- **Domínio** = Endereço da casa (rua, número)

### Ambientes de Desenvolvimento

| Ambiente | Propósito | URL exemplo |
|----------|-----------|-------------|
| **Local** | Desenvolver no seu computador | `localhost:3000` |
| **Preview** | Testar antes de publicar | `verde-barro-git-feature-xyz.vercel.app` |
| **Produção** | Site real para clientes | `verdebarro.com.br` |

### Variáveis de Ambiente

**O que são**: Configurações sensíveis (senhas, chaves de API) que ficam separadas do código.

**Por que separar**:
- Segurança (não expor senhas no código)
- Flexibilidade (diferentes valores por ambiente)
- Boas práticas (padrão da indústria)

---

## 🏠 Camada 2: Aplicação para Verde Barro

### Checklist de Infraestrutura

```
┌─────────────────────────────────────────────────────────────┐
│                    SETUP COMPLETO                           │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  CONTAS NECESSÁRIAS                                         │
│  ─────────────────────                                      │
│  □ GitHub (código)                                          │
│  □ Vercel (hospedagem)                                      │
│  □ Supabase (banco de dados)                                │
│  □ Stripe (pagamentos)                                      │
│  □ Resend (emails)                                          │
│  □ Cal.com (agendamentos)                                   │
│                                                             │
│  CONFIGURAÇÕES                                              │
│  ─────────────────                                          │
│  □ Repositório criado                                       │
│  □ Projeto Next.js inicializado                             │
│  □ Projeto Supabase criado                                  │
│  □ Tabelas do banco criadas                                 │
│  □ Conta Stripe configurada                                 │
│  □ Variáveis de ambiente configuradas                       │
│  □ Deploy na Vercel funcionando                             │
│                                                             │
│  DOMÍNIO (opcional agora)                                   │
│  ───────                                                    │
│  □ Domínio registrado                                       │
│  □ DNS configurado                                          │
│  □ SSL ativo                                                │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Guia Passo a Passo

### ETAPA 1: Criar Repositório no GitHub

**1.1. Criar conta** (se não tiver)
- Acesse: https://github.com
- Criar conta gratuita

**1.2. Criar repositório**
- Clique em "New repository"
- Nome: `verde-barro-site`
- Visibilidade: **Private** (recomendado)
- Inicializar com README: Sim
- .gitignore: Node
- Licença: Nenhuma (privado)

**1.3. Clonar no computador**
```bash
git clone https://github.com/SEU_USUARIO/verde-barro-site.git
cd verde-barro-site
```

---

### ETAPA 2: Criar Projeto Next.js

**2.1. Inicializar projeto**
```bash
npx create-next-app@latest . --typescript --tailwind --eslint --app --src-dir --import-alias "@/*"
```

Opções recomendadas:
- TypeScript: **Yes**
- ESLint: **Yes**
- Tailwind CSS: **Yes**
- `src/` directory: **Yes**
- App Router: **Yes**
- Import alias: **@/***

**2.2. Instalar dependências essenciais**
```bash
# Supabase
npm install @supabase/supabase-js @supabase/ssr

# Stripe
npm install stripe @stripe/stripe-js

# Email
npm install resend @react-email/components

# UI (shadcn) - NOTA: pacote foi renomeado de shadcn-ui para shadcn
npx shadcn@latest init

# Utilitários
npm install date-fns zod react-hook-form @hookform/resolvers
```

**2.3. Configurar shadcn**
```bash
# Componentes base (pode adicionar todos de uma vez)
npx shadcn@latest add button card input label textarea dialog sheet sonner form select checkbox
```

**2.4. Testar localmente**
```bash
npm run dev
```
Acesse: http://localhost:3000

---

### ETAPA 3: Configurar Supabase

**3.1. Criar conta e projeto**
- Acesse: https://supabase.com
- "Start your project"
- Nome: `verde-barro`
- Região: **South America (São Paulo)** — mais perto = mais rápido
- Senha do banco: Anote em lugar seguro!

**3.2. Obter credenciais**

No dashboard do Supabase (versão atual):

1. **Project URL**  
   - Aba **Settings** (ícone engrenagem) → **API**  
   - Ou use o diálogo **Connect** (botão "Connect" no projeto)  
   - Copie o **Project URL**

2. **Chaves de API (modelo atual)**  
   - **Settings** → **API** → aba **API Keys** (não use "Legacy API Keys")  
   - **Publishable key** (`sb_publishable_...`) — uso no **client** (browser, app). Pode expor.  
   - **Secret key** (`sb_secret_...`) — uso **apenas no servidor** (API routes, webhooks). Nunca exponha.  
   - Se não aparecer Publishable/Secret, clique em **Create new API Keys** e copie os valores.

3. **Onde colar no projeto**  
   - **Project URL** → `NEXT_PUBLIC_SUPABASE_URL`  
   - **Publishable key** → `NEXT_PUBLIC_SUPABASE_ANON_KEY` (nome da variável segue o padrão do Supabase)  
   - **Secret key** → `SUPABASE_SERVICE_ROLE_KEY`

**Nota:** As chaves antigas (`anon` e `service_role`, em JWT) estão na aba **Legacy API Keys** e foram substituídas por Publishable e Secret. Use as novas quando possível.

**3.3. Criar tabelas**

Vá em SQL Editor e execute o schema completo (de O2_Stack_Tecnologica.md):

```sql
-- ============================================================
-- SOLICITAÇÕES DE EXPERIÊNCIAS (antes do pagamento)
-- ============================================================
CREATE TABLE solicitacoes_experiencias (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  
  -- Experiência
  experiencia TEXT NOT NULL,
  num_pessoas INTEGER NOT NULL CHECK (num_pessoas >= 2 AND num_pessoas <= 8),
  
  -- Agendamento desejado
  data_desejada DATE NOT NULL,
  horario_desejado TEXT,
  
  -- Local
  endereco_cep TEXT NOT NULL,
  endereco_rua TEXT NOT NULL,
  endereco_numero TEXT NOT NULL,
  endereco_complemento TEXT,
  endereco_bairro TEXT NOT NULL,
  endereco_cidade TEXT NOT NULL DEFAULT 'São Paulo',
  
  -- Dados do solicitante
  nome TEXT NOT NULL,
  email TEXT NOT NULL,
  whatsapp TEXT NOT NULL,
  
  -- Forma de pagamento escolhida
  tipo_pagamento TEXT NOT NULL,
  
  -- Observações do cliente
  observacoes TEXT,
  
  -- Status do fluxo
  status TEXT DEFAULT 'pendente',
  
  -- Valor calculado
  valor_total DECIMAL(10,2),
  valor_por_pessoa DECIMAL(10,2),
  
  -- Link de pagamento
  link_pagamento_id UUID,
  stripe_session_id TEXT,
  
  -- Motivo (se recusado)
  motivo_recusa TEXT,
  
  -- Metadata
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW(),
  confirmado_em TIMESTAMP,
  pago_em TIMESTAMP
);

-- ============================================================
-- PEDIDOS DE EXPERIÊNCIAS (após pagamento confirmado)
-- ============================================================
CREATE TABLE pedidos_experiencias (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  
  solicitacao_id UUID REFERENCES solicitacoes_experiencias(id),
  
  experiencia TEXT NOT NULL,
  num_pessoas INTEGER NOT NULL,
  data_agendada DATE NOT NULL,
  horario TEXT,
  endereco JSONB NOT NULL,
  
  nome TEXT NOT NULL,
  email TEXT NOT NULL,
  whatsapp TEXT NOT NULL,
  
  tipo_pagamento TEXT NOT NULL,
  valor_total DECIMAL(10,2) NOT NULL,
  stripe_payment_intent TEXT,
  
  status TEXT DEFAULT 'confirmado',
  
  created_at TIMESTAMP DEFAULT NOW(),
  realizado_em TIMESTAMP
);

-- ============================================================
-- PEDIDOS DE PEÇAS AUTORAIS
-- ============================================================
CREATE TABLE pedidos_pecas (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  
  itens JSONB NOT NULL,
  valor_subtotal DECIMAL(10,2) NOT NULL,
  valor_frete DECIMAL(10,2) NOT NULL,
  valor_total DECIMAL(10,2) NOT NULL,
  
  nome TEXT NOT NULL,
  email TEXT NOT NULL,
  whatsapp TEXT,
  
  endereco_cep TEXT NOT NULL,
  endereco_rua TEXT NOT NULL,
  endereco_numero TEXT NOT NULL,
  endereco_complemento TEXT,
  endereco_bairro TEXT NOT NULL,
  endereco_cidade TEXT NOT NULL,
  endereco_estado TEXT NOT NULL,
  
  stripe_session_id TEXT,
  stripe_payment_intent TEXT,
  
  status TEXT DEFAULT 'pendente',
  
  codigo_rastreio TEXT,
  enviado_em TIMESTAMP,
  
  created_at TIMESTAMP DEFAULT NOW(),
  pago_em TIMESTAMP
);

-- ============================================================
-- GRUPOS (checkout compartilhável)
-- ============================================================
CREATE TABLE grupos (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  
  solicitacao_id UUID REFERENCES solicitacoes_experiencias(id),
  
  num_vagas INTEGER NOT NULL,
  valor_por_pessoa DECIMAL(10,2) NOT NULL,
  
  expira_em TIMESTAMP NOT NULL,
  
  status TEXT DEFAULT 'aberto',
  
  created_at TIMESTAMP DEFAULT NOW()
);

-- ============================================================
-- PARTICIPANTES DO GRUPO
-- ============================================================
CREATE TABLE grupo_participantes (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  grupo_id UUID REFERENCES grupos(id),
  
  nome TEXT NOT NULL,
  email TEXT NOT NULL,
  whatsapp TEXT,
  
  stripe_payment_intent TEXT,
  pago BOOLEAN DEFAULT FALSE,
  pago_em TIMESTAMP,
  
  is_organizador BOOLEAN DEFAULT FALSE,
  
  created_at TIMESTAMP DEFAULT NOW()
);

-- ============================================================
-- NEWSLETTER
-- ============================================================
CREATE TABLE newsletter (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  email TEXT UNIQUE NOT NULL,
  nome TEXT,
  origem TEXT,
  created_at TIMESTAMP DEFAULT NOW()
);

-- ============================================================
-- CUPONS
-- ============================================================
CREATE TABLE cupons (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  codigo TEXT UNIQUE NOT NULL,
  
  tipo TEXT NOT NULL,
  
  pedido_peca_id UUID REFERENCES pedidos_pecas(id),
  influenciadora_nome TEXT,
  campanha_nome TEXT,
  
  desconto_tipo TEXT NOT NULL DEFAULT 'percentual',
  desconto_valor DECIMAL(10,2) NOT NULL,
  
  aplica_em TEXT NOT NULL DEFAULT 'experiencias',
  
  valor_minimo DECIMAL(10,2),
  
  valido_de TIMESTAMP DEFAULT NOW(),
  valido_ate TIMESTAMP NOT NULL,
  
  uso_maximo INTEGER DEFAULT 1,
  uso_atual INTEGER DEFAULT 0,
  
  status TEXT DEFAULT 'ativo',
  
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW()
);

-- ============================================================
-- HISTÓRICO DE USO DE CUPONS
-- ============================================================
CREATE TABLE cupons_uso (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  cupom_id UUID REFERENCES cupons(id) NOT NULL,
  
  solicitacao_id UUID REFERENCES solicitacoes_experiencias(id),
  pedido_peca_id UUID REFERENCES pedidos_pecas(id),
  
  valor_original DECIMAL(10,2) NOT NULL,
  valor_desconto DECIMAL(10,2) NOT NULL,
  valor_final DECIMAL(10,2) NOT NULL,
  
  usado_em TIMESTAMP DEFAULT NOW()
);

-- ============================================================
-- ÍNDICES
-- ============================================================
CREATE INDEX idx_solicitacoes_status ON solicitacoes_experiencias(status);
CREATE INDEX idx_solicitacoes_email ON solicitacoes_experiencias(email);
CREATE INDEX idx_solicitacoes_data ON solicitacoes_experiencias(data_desejada);

CREATE INDEX idx_pedidos_exp_status ON pedidos_experiencias(status);
CREATE INDEX idx_pedidos_exp_email ON pedidos_experiencias(email);

CREATE INDEX idx_pedidos_pecas_status ON pedidos_pecas(status);
CREATE INDEX idx_pedidos_pecas_email ON pedidos_pecas(email);

CREATE INDEX idx_grupos_status ON grupos(status);
CREATE INDEX idx_grupos_expira ON grupos(expira_em);

CREATE INDEX idx_cupons_codigo ON cupons(codigo);
CREATE INDEX idx_cupons_status ON cupons(status);
CREATE INDEX idx_cupons_tipo ON cupons(tipo);
CREATE INDEX idx_cupons_validade ON cupons(valido_ate);
```

**3.4. Verificar tabelas**
- Vá em Table Editor
- Deve ver 8 tabelas criadas

---

### ETAPA 4: Configurar Stripe

**4.1. Criar conta**
- Acesse: https://stripe.com
- Criar conta (ou usar existente)
- Ativar modo de teste primeiro

**4.2. Obter credenciais**
- Dashboard → Developers → API Keys
- Copie:
  - `Publishable key` (pk_test_...)
  - `Secret key` (sk_test_...)

**4.3. Configurar webhook (depois do deploy)**
- Developers → Webhooks → Add endpoint
- URL: `https://seu-site.vercel.app/api/webhooks/stripe`
- Eventos:
  - `checkout.session.completed`
  - `payment_intent.succeeded`
  - `payment_intent.payment_failed`
- Copie o `Webhook signing secret` (whsec_...)

**4.4. Criar produtos no Stripe (opcional agora)**
```
Experiência Modelagem — R$ 350/pessoa
Experiência Pintura — R$ 280/pessoa
```

---

### ETAPA 5: Configurar Resend (Email)

**5.1. Criar conta**
- Acesse: https://resend.com
- Criar conta gratuita (3.000 emails/mês)

**5.2. Obter API Key**
- Settings → API Keys
- Create API Key
- Copie: `re_...`

**5.3. Configurar domínio (depois)**
- Para enviar de `verdebarro.ceramica@gmail.com`
- Domains → Add domain
- Configurar DNS

---

### ETAPA 6: Configurar Cal.com (Agendamento)

**6.1. Criar conta**
- Acesse: https://cal.com
- Criar conta gratuita

**6.2. Criar evento**
- Nome: "Chamada de apresentação Verde Barro"
- Duração: 15 minutos
- Disponibilidade: Seus horários

**6.3. Obter link/embed**
- Copie link público ou código de embed

---

### ETAPA 7: Configurar Variáveis de Ambiente

**7.1. Criar arquivo `.env.local`**

```env
# ===========================================
# APP
# ===========================================
NEXT_PUBLIC_APP_URL=http://localhost:3000
NEXT_PUBLIC_APP_NAME="Verde Barro Cerâmica"

# ===========================================
# SUPABASE
# ===========================================
# Project URL (Settings → API)
NEXT_PUBLIC_SUPABASE_URL=https://xxxxxxxxxxxx.supabase.co
# Publishable key (Settings → API → API Keys) — client-side
NEXT_PUBLIC_SUPABASE_ANON_KEY=sb_publishable_...
# Secret key (Settings → API → API Keys) — server-side apenas!
SUPABASE_SERVICE_ROLE_KEY=sb_secret_...

# ===========================================
# STRIPE
# ===========================================
STRIPE_SECRET_KEY=sk_test_...
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...

# ===========================================
# RESEND (Email)
# ===========================================
RESEND_API_KEY=re_...

# ===========================================
# CAL.COM (Agendamento)
# ===========================================
NEXT_PUBLIC_CAL_LINK=https://cal.com/verde-barro/apresentacao

# ===========================================
# WHATSAPP
# ===========================================
NEXT_PUBLIC_WHATSAPP_NUMBER=5511999999999
```

**7.2. Adicionar ao `.gitignore`**
```gitignore
# Já deve estar, mas confirme:
.env*.local
```

⚠️ **NUNCA** commite o `.env.local` no Git!

---

### ETAPA 8: Criar Estrutura Base do Projeto

**8.1. Estrutura de pastas**

```
src/
├── app/
│   ├── (site)/
│   │   ├── page.tsx              # Home
│   │   ├── experiencias/
│   │   │   └── page.tsx
│   │   ├── pecas/
│   │   │   └── page.tsx
│   │   └── contato/
│   │       └── page.tsx
│   │
│   ├── api/
│   │   ├── solicitacao/
│   │   │   └── route.ts
│   │   ├── checkout/
│   │   │   └── route.ts
│   │   ├── webhooks/
│   │   │   └── stripe/
│   │   │       └── route.ts
│   │   └── newsletter/
│   │       └── route.ts
│   │
│   ├── layout.tsx
│   └── globals.css
│
├── components/
│   ├── ui/                       # shadcn/ui
│   ├── layout/
│   │   ├── header.tsx
│   │   └── footer.tsx
│   └── forms/
│       └── newsletter-form.tsx
│
├── lib/
│   ├── supabase/
│   │   ├── client.ts
│   │   └── server.ts
│   ├── stripe.ts
│   ├── resend.ts
│   └── utils.ts
│
└── emails/
    └── confirmacao.tsx
```

**8.2. Criar cliente Supabase**

`src/lib/supabase/client.ts`:
```typescript
import { createBrowserClient } from '@supabase/ssr'

export function createClient() {
  return createBrowserClient(
    process.env.NEXT_PUBLIC_SUPABASE_URL!,
    process.env.NEXT_PUBLIC_SUPABASE_ANON_KEY!
  )
}
```

`src/lib/supabase/server.ts`:
```typescript
import { createServerClient, type CookieOptions } from '@supabase/ssr'
import { cookies } from 'next/headers'

export function createClient() {
  const cookieStore = cookies()

  return createServerClient(
    process.env.NEXT_PUBLIC_SUPABASE_URL!,
    process.env.NEXT_PUBLIC_SUPABASE_ANON_KEY!,
    {
      cookies: {
        get(name: string) {
          return cookieStore.get(name)?.value
        },
        set(name: string, value: string, options: CookieOptions) {
          cookieStore.set({ name, value, ...options })
        },
        remove(name: string, options: CookieOptions) {
          cookieStore.set({ name, value: '', ...options })
        },
      },
    }
  )
}
```

**8.3. Criar cliente Stripe**

`src/lib/stripe.ts`:
```typescript
import Stripe from 'stripe'

export const stripe = new Stripe(process.env.STRIPE_SECRET_KEY!, {
  apiVersion: '2023-10-16',
  typescript: true,
})
```

**8.4. Criar cliente Resend**

`src/lib/resend.ts`:
```typescript
import { Resend } from 'resend'

export const resend = new Resend(process.env.RESEND_API_KEY)
```

---

### ETAPA 9: Página Home Básica

`src/app/(site)/page.tsx`:
```tsx
export default function Home() {
  return (
    <main className="min-h-screen">
      {/* Hero */}
      <section className="flex flex-col items-center justify-center min-h-[80vh] px-4 text-center">
        <h1 className="text-4xl md:text-6xl font-serif mb-6">
          Verde Barro Cerâmica
        </h1>
        <p className="text-lg md:text-xl text-muted-foreground max-w-2xl mb-8">
          Experiências de cerâmica na sua casa. 
          Transformamos encontros em memórias que duram para sempre.
        </p>
        <div className="flex flex-col sm:flex-row gap-4">
          <a 
            href="/experiencias"
            className="px-8 py-3 bg-primary text-primary-foreground rounded-full"
          >
            Ver experiências
          </a>
          <a 
            href="/pecas"
            className="px-8 py-3 border border-primary rounded-full"
          >
            Peças autorais
          </a>
        </div>
      </section>
    </main>
  )
}
```

---

### ETAPA 10: Deploy na Vercel

**10.1. Criar conta na Vercel**
- Acesse: https://vercel.com
- Fazer login com GitHub

**10.2. Importar projeto**
- "Add New..." → "Project"
- Selecionar repositório `verde-barro-site`
- Framework: Next.js (auto-detectado)

**10.3. Configurar variáveis de ambiente**
- Em "Environment Variables"
- Adicionar TODAS as variáveis do `.env.local`
- **IMPORTANTE**: Mudar `NEXT_PUBLIC_APP_URL` para URL do Vercel

**10.4. Deploy**
- Clique em "Deploy"
- Aguarde ~2 minutos
- Acesse a URL gerada (ex: `verde-barro-site.vercel.app`)

**10.5. Configurar webhook do Stripe**
- Volte no Stripe → Webhooks
- Adicione URL: `https://verde-barro-site.vercel.app/api/webhooks/stripe`
- Copie o novo webhook secret
- Atualize a variável `STRIPE_WEBHOOK_SECRET` na Vercel

---

## ✅ Checklist de Verificação

### Ambiente Local
- [ ] `npm run dev` funciona
- [ ] Página inicial carrega em localhost:3000
- [ ] Sem erros no console

### Supabase
- [ ] 8 tabelas criadas
- [ ] Consegue conectar (sem erros de auth)

### Stripe
- [ ] API keys configuradas
- [ ] Webhook criado (após deploy)

### Vercel
- [ ] Deploy bem-sucedido
- [ ] Site abre na URL do Vercel
- [ ] Variáveis de ambiente configuradas

---

## 🚨 Troubleshooting

### Erro: "Invalid API key"
**Causa**: Variável de ambiente não configurada
**Solução**: Verificar se copiou corretamente no Vercel

### Erro: "CORS policy"
**Causa**: Supabase não permite origem
**Solução**: Em Supabase → Settings → API, verificar URLs permitidas

### Erro: "Module not found"
**Causa**: Dependência não instalada
**Solução**: `npm install` novamente

### Deploy falha na Vercel
**Causa comum**: Erro de TypeScript
**Solução**: `npm run build` local para ver erros

---

## 📦 Commit Inicial

```bash
git add .
git commit -m "feat: setup inicial do projeto Verde Barro

- Next.js 14 com App Router
- Tailwind CSS + shadcn/ui
- Supabase client configurado
- Stripe client configurado
- Resend client configurado
- Estrutura de pastas definida
- Página home básica"

git push origin main
```

---

## 🎯 Próximos Passos (Lição O4)

Após infraestrutura básica funcionando:
1. Configurar políticas de segurança (RLS) no Supabase
2. Criar política de privacidade
3. Implementar consentimento LGPD
4. Configurar backup automático

---

## 💡 Dicas Importantes

### Segurança
- **NUNCA** commite arquivos `.env` no Git
- Use `NEXT_PUBLIC_` apenas para variáveis que podem ser públicas
- `SUPABASE_SERVICE_ROLE_KEY` (Secret key `sb_secret_...`) é **secreta** — só use no servidor; nunca no browser

### Performance
- Vercel deploy automático a cada push no main
- Use branch `develop` para testes antes de ir para `main`

### Custos Atuais
| Serviço | Plano | Custo |
|---------|-------|-------|
| GitHub | Free | R$ 0 |
| Vercel | Hobby | R$ 0 |
| Supabase | Free | R$ 0 |
| Stripe | Pay as you go | 3.99% + R$ 0.39/tx |
| Resend | Free (3k/mês) | R$ 0 |
| Cal.com | Free | R$ 0 |
| **Total fixo** | | **R$ 0/mês** |

---

**Status**: ✅ Concluída  
**Data de conclusão**: 2025-01-31  
**Última atualização**: 2025-01-28
