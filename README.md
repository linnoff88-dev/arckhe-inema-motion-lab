# INEMA Motion Lab

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![INEMA Motion Lab](guia/assets/banner.jpg)](https://inematds.github.io/inema-motion-lab/guia/)

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

## O que Ã©

O INEMA Motion Lab ensina a pedir animaÃ§Ãµes de site para uma IA (Claude, Codex ou outra) e receber algo com acabamento profissional, nÃ£o um efeito genÃ©rico. Ele traz um molde de prompt em trÃªs partes (aparÃªncia, movimento e regras) e vinte exemplos reais feitos com ele: buscas e menus, rodapÃ©s, galerias, botÃµes, uma pÃ¡gina 404 jogÃ¡vel, uma tela de carregamento e um botÃ£o de tema dia/noite, todos com Raio-X e modo `?motion=off`. Cada peÃ§a Ã© um Ãºnico arquivo HTML que vocÃª abre no navegador e cola no seu site, e vem com o prompt que a gerou e um vÃ­deo curto. Serve para quem faz pÃ¡ginas, guias ou cursos e quer movimento sem depender de biblioteca pesada.

## ðŸ“– Guia de uso

Guia completo (landing + passo a passo, com as peÃ§as ao vivo): **https://inematds.github.io/inema-motion-lab/guia/**

## ConteÃºdo

| Pasta | O que tem |
|---|---|
| `molde/MOLDE-PROMPT-ANIMACAO.md` | O molde de prompt: aparÃªncia, movimento numerado, regras tÃ©cnicas |
| `pecas/<nome>/PROMPT.md` | O prompt de cada peÃ§a, escrito com o molde |
| `pecas/<nome>/index.html` | A peÃ§a pronta, um arquivo sÃ³ |
| `videos/` | DemonstraÃ§Ã£o de 8 s de cada peÃ§a (WebM, MP4 e imagem de capa) |
| `tools/testar-pecas.cjs` | Testa todas as peÃ§as no navegador (erros, 360 px, movimento reduzido, rolagem) |
| `tools/gravar-videos.cjs` | Grava o modo demonstraÃ§Ã£o (`?demo=1`) de cada peÃ§a |

## As 20 peÃ§as

Cada peÃ§a tem `index.html` e `PROMPT.md`, e aceita `?demo=1` (demonstraÃ§Ã£o contÃ­nua), `?motion=xray` (Raio-X: etiqueta o que se move) e `?motion=off` (tudo parado no estado final).

**Busca e navegaÃ§Ã£o**

| PeÃ§a | Link |
|---|---|
| Busca âŒ˜K | [`pecas/busca-cmdk/`](pecas/busca-cmdk/index.html) |
| NavegaÃ§Ã£o com pulo | [`pecas/nav-pulo/`](pecas/nav-pulo/index.html) |
| Menu que se transforma | [`pecas/menu-morfo/`](pecas/menu-morfo/index.html) |
| Menu em tela cheia | [`pecas/menu-tela-cheia/`](pecas/menu-tela-cheia/index.html) |
| Dock lÃ­quido | [`pecas/dock-liquido/`](pecas/dock-liquido/index.html) |

**RodapÃ©s**

| PeÃ§a | Link |
|---|---|
| RodapÃ© INEMA com fÃ­sica | [`pecas/rodape-inema/`](pecas/rodape-inema/index.html) |
| RodapÃ© cortina | [`pecas/rodape-cortina/`](pecas/rodape-cortina/index.html) |
| RodapÃ© flor | [`pecas/rodape-flor/`](pecas/rodape-flor/index.html) |
| RodapÃ© mapa | [`pecas/rodape-mapa/`](pecas/rodape-mapa/index.html) |
| RodapÃ© quebra | [`pecas/rodape-quebra/`](pecas/rodape-quebra/index.html) |

**Galerias e imagens**

| PeÃ§a | Link |
|---|---|
| Grade bento com moldura que desliza | [`pecas/bento-glide/`](pecas/bento-glide/index.html) |
| Galeria giro | [`pecas/galeria-giro/`](pecas/galeria-giro/index.html) |
| Rastro de imagens | [`pecas/rastro-imagens/`](pecas/rastro-imagens/index.html) |
| Adesivo hologrÃ¡fico | [`pecas/adesivo-holo/`](pecas/adesivo-holo/index.html) |

**BotÃµes e detalhes**

| PeÃ§a | Link |
|---|---|
| BotÃµes de geleia | [`pecas/botoes-geleia/`](pecas/botoes-geleia/index.html) |
| Cursor amigo | [`pecas/cursor-amigo/`](pecas/cursor-amigo/index.html) |
| Faixa flap | [`pecas/faixa-flap/`](pecas/faixa-flap/index.html) |
| Dia e noite | [`pecas/dia-noite/`](pecas/dia-noite/index.html) |

**PÃ¡ginas especiais**

| PeÃ§a | Link |
|---|---|
| 404 que vira jogo | [`pecas/404-corre/`](pecas/404-corre/index.html) |
| Revela carga | [`pecas/revela-carga/`](pecas/revela-carga/index.html) |

## Uso rÃ¡pido

```bash
git clone https://github.com/inematds/inema-motion-lab && cd inema-motion-lab
python3 -m http.server 8850 --directory . --bind 127.0.0.1
# abra http://127.0.0.1:8850/pecas/busca-cmdk/   (acrescente ?demo=1 para a demonstraÃ§Ã£o nÃ£o parar)

# testar e gravar (Node 18+, playwright e ffmpeg)
node tools/testar-pecas.cjs 8850
node tools/gravar-videos.cjs 8850
```

## CrÃ©ditos

Prompts e cÃ³digo escritos do zero para o INEMA.
ConteÃºdo aberto e gratuito do [INEMA.CLUB](https://inema.club).

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>