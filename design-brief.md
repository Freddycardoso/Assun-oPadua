# Design Brief — Assunção e Pádua Odontologia

## Conceito: Editorial Clínico & Orgânico
Grafite arquitetônico da fachada + off-white acolhedor + verde botânico do jardim vertical.
Atmosfera: **Equilíbrio, Rigor, Acolhimento.**

## Pesquisa (Fase 0)

> Transparência: ✔ = site aberto e capturado; ○ = apareceu só na busca (observação indireta).

### Nicho
| Site | Status | Aprendizado |
|---|---|---|
| dentalboutique.com.au | ✔ | Retrato humano real no hero + selo Google 5.0. **Evitar:** texto demais na primeira dobra. |
| theluxurydentist.com | ✔ | Título atribuído ao fundador, serifa + sans. **Evitar:** dourado/azul-noturno de "luxo" genérico. |
| Premier Arts Dental | ○ | Grid assimétrico, neutros quentes. Evitar fotos de banco. |

### Fora do nicho
| Site | Status | Aprendizado |
|---|---|---|
| snohetta.com | ✔ | Espaço negativo altíssimo, tipografia discreta, hover sutil. |
| Boutique Dermatology | ○ | Colunas bem definidas, tom concierge. |

### Premiado
| Site | Status | Aprendizado |
|---|---|---|
| nekohealth.com | ✔ | Off-white + carvão, cartões planos, bordas finas, zero sombra pesada. |

### Concorrência em Passos-MG (○ — análise indireta, sites não abertos)
- Sorriso Minas, OralClinic Passos: padrão de catálogo de procedimentos, "avaliação grátis", gradientes azuis, banners genéricos, WhatsApp flutuante padrão.
- **Como nos diferenciamos:** fundadores reais em paridade, fachada e recepção reais, sem promoção, paleta grafite + musgo.

## Decisões
- **Tipografia:** Plus Jakarta Sans (400/500/600/700), uma única família. Base 18px, `leading-relaxed`, H1 38–44px.
- **Linguagem:** linhas de 1px (`#E5E7EB`), `rounded-xl` (12px máx.), cartões com borda tonal, sem sombras.
- **Layout:** ritmo variado (hero 2 col assimétrico, dores 3 col, serviços 2x2, timeline, autoridade 2 col pareada, FAQ estreito). Evita 3 colunas idênticas repetidas.
- **Motion:** apenas CSS, `transition: all .25s ease-in-out`, `prefers-reduced-motion` respeitado.
- **JS no cliente:** zero. FAQ em `<details>/<summary>`.

## Paleta (estrita)
| Token | Hex |
|---|---|
| offwhite (fundo) | #F8F9FA |
| surface | #FFFFFF |
| grafite-900 | #24282B |
| grafite-600 (apoio) | #5C646A |
| brand-green | #3E5C56 |
| brand-navy | #1E2B37 |
| line | #E5E7EB |

## Inventário de imagens (`src/assets/images/`)
| Arquivo | Dimensão real | Uso | Observação |
|---|---|---|---|
| hero-socios-julio-e-mirian.png | 669×1020 | Hero (eager + preload) | Retrato conjunto |
| autoridade-dra-mirian-assuncao.png | 757×1020 | Autoridade | OK |
| autoridade-dr-julio-cesar.png | 141×235 | Autoridade | **Baixa resolução** — ver riscos |
| fachada-clinica-assuncao-padua.png | 750×1020 | Seção de estrutura | OK |
| recepcao-clinica-monograma-ap.png | 141×235 | Seção de estrutura | **Baixa resolução** |
| equipe-socios-jaleco-preto.png | 141×235 | Não usada, pois seria ampliada em excesso | — |

## Riscos / pendências
1. **Foto do Dr. Júlio (141×235)** é bem menor que a da Dra. Mirian (757×1020). Isso ameaça a paridade visual exigida. Mitigação: ambas exibidas no mesmo tamanho CSS pequeno e mesma moldura; recomenda-se solicitar foto original em alta.
2. **`placa-fachada-cro-contato.png`** não existe na pasta e não foi inventada.
3. Imagens são PNG (não JPG como no PRD); o Astro converte para WebP/AVIF.
4. Depoimentos e o selo "5.0" do PRD são marcados como exemplo/substituir (compliance: confirmar dados reais).
