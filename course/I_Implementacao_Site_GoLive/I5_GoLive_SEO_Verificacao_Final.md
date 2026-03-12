# Lição I5 — Go-Live, SEO e Verificação Final

> **Fase**: I — Implementação de Site Completo e Go-Live  
> **Status**: 🔄 Em andamento  
> **Pré-requisito**: I3 (páginas e branding) e I4 (integrações) concluídos

---

## Objetivo da Lição

Colocar o site **em produção** (deploy estável), garantir **SEO e sitemap** funcionais, deixar **métricas** ativas ou configuráveis, e produzir o documento **"Informações que o usuário precisa fornecer"** (incluindo **referências de site** e direção de design para futuras iterações).

---

## Camada 1: Conceitos

### Deploy estável

Site em produção (ex.: Vercel); variáveis de ambiente configuradas e documentadas; build sem erros.

### SEO e sitemap

Meta tags por página; sitemap.xml com URL base normalizada e resiliência a falhas externas (evitar "Couldn't fetch"); robots.txt; Google Search Console via meta tag (env).

### Métricas

Search Console verificado ou pronto; analytics (ex.: Vercel Analytics) ativo; dados transacionais (Supabase) acessíveis.

### Documento para o usuário

Listar: **referências de site** (URLs usadas em I2) e direção de design; variáveis de ambiente (WhatsApp, Cal.com, URL, GSC); nome/foto fundadora; depoimentos; preços; peças/fotos; logo; IDs Stripe se aplicável. O usuário sabe o que configurar para o site refletir o negócio e manter o nível agência.

---

## Camada 2: Checklist de go-live

- [ ] Deploy com env definidas.
- [ ] sitemap.xml retornando 200; robots.txt correto.
- [ ] Meta tag GSC no head (NEXT_PUBLIC_GOOGLE_SITE_VERIFICATION); usuário verifica e envia sitemap.
- [ ] Vercel Analytics ativado.
- [ ] Documento INFORMACOES_PARA_O_USUARIO.md (ou equivalente) no repositório do site.

### Verificação final

Navegar todas as páginas; enviar formulário; testar WhatsApp e Cal.com. Sem "Em breve" bloqueante.

### Entregáveis

- [ ] Site em produção.
- [ ] SEO e sitemap funcionais; GSC e analytics configuráveis/ativos.
- [ ] Documento de informações para o usuário.

---

## Conclusão da Fase I

Ao fechar o checklist da Fase I (I1), o site está completo, em go-live e no **nível de qualidade definido** (referências + direção de design). Seguir para **Fase S — Scale, SEO & Otimização Contínua**.
