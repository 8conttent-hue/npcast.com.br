# CLAUDE.md — NPCAST

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** NPCAST
**Nicho:** Entretenimento
**Keywords:** O Np Cast e um portal de conteudo fundado pelos amigos Trabuco
**Paleta de cores:** forest | **Fonte:** poppins

O Np Cast! é um portal de conteúdo fundado pelos amigos Trabuco e Eldake, em 2014 com o objetivo de trazer crônicas e críticas da cultura pop e informações do mundo dos podcasts para nossos leitores. O que era brincadeira, evoluiu para algo sério, tão sério que mudou até de nome! O que era Nostromo Podcast hoje é apenas NP Cast! É publicado quinzenalmente sempre as terças feiras, e gerou uma família, sim a Família NP!, temos hoje Drops, Games, Mysterium e Talk Show! Com um conteúdo bem variado, trazemos aos nossos ouvintes, temáticas variadas, já falamos de filmes de trash horror, a estudos científicos, de ufologia ao futebol. Esse é o intuito da Família NP, trazer a cultura pop e a inserir dinamicamente em seu cotidiano! Se está gostando do nosso conteúdo, nos envie uma mensagem!



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-G |
| Hero | Hero-I |
| Features | Features-F |
| About Section | About-A |
| Posts | Posts-A |
| Footer | Footer-F |
| Página Sobre | Sobre-H |
| Página Contato | Contato-E |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
