ï»¿# INEMA Motion Lab

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![INEMA Motion Lab](guia/assets/banner.jpg)](https://inematds.github.io/inema-motion-lab/guia/)

**ê°Å¸â¡Â§ê°Å¸â¡Â· [PortuguêÂªs](README.md) êÂ· ê°Å¸â¡Âºê°Å¸â¡Â¸ [English](README.en.md) êÂ· ê°Å¸â¡Âªê°Å¸â¡Â¸ [EspaêÂ±ol](README.es.md)**

## O que êÂ©

O INEMA Motion Lab ensina a pedir animaêÂ§êÂµes de site para uma IA (Claude, Codex ou outra) e receber algo com acabamento profissional, nêÂ£o um efeito genêÂ©rico. Ele traz um molde de prompt em trêÂªs partes (aparêÂªncia, movimento e regras) e vinte exemplos reais feitos com ele: buscas e menus, rodapêÂ©s, galerias, botêÂµes, uma pêÂ¡gina 404 jogêÂ¡vel, uma tela de carregamento e um botêÂ£o de tema dia/noite, todos com Raio-X e modo `?motion=off`. Cada peêÂ§a êÂ© um êÂºnico arquivo HTML que vocêÂª abre no navegador e cola no seu site, e vem com o prompt que a gerou e um vêÂ­deo curto. Serve para quem faz pêÂ¡ginas, guias ou cursos e quer movimento sem depender de biblioteca pesada.

## ê°Å¸ââ Guia de uso

Guia completo (landing + passo a passo, com as peêÂ§as ao vivo): **https://inematds.github.io/inema-motion-lab/guia/**

## ConteêÂºdo

| Pasta | O que tem |
|---|---|
| `molde/MOLDE-PROMPT-ANIMACAO.md` | O molde de prompt: aparêÂªncia, movimento numerado, regras têÂ©cnicas |
| `pecas/<nome>/PROMPT.md` | O prompt de cada peêÂ§a, escrito com o molde |
| `pecas/<nome>/index.html` | A peêÂ§a pronta, um arquivo sêÂ³ |
| `videos/` | DemonstraêÂ§êÂ£o de 8 s de cada peêÂ§a (WebM, MP4 e imagem de capa) |
| `tools/testar-pecas.cjs` | Testa todas as peêÂ§as no navegador (erros, 360 px, movimento reduzido, rolagem) |
| `tools/gravar-videos.cjs` | Grava o modo demonstraêÂ§êÂ£o (`?demo=1`) de cada peêÂ§a |

## As 20 peêÂ§as

Cada peêÂ§a tem `index.html` e `PROMPT.md`, e aceita `?demo=1` (demonstraêÂ§êÂ£o contêÂ­nua), `?motion=xray` (Raio-X: etiqueta o que se move) e `?motion=off` (tudo parado no estado final).

**Busca e navegaêÂ§êÂ£o**

| PeêÂ§a | Link |
|---|---|
| Busca ê¢ÅËK | [`pecas/busca-cmdk/`](pecas/busca-cmdk/index.html) |
| NavegaêÂ§êÂ£o com pulo | [`pecas/nav-pulo/`](pecas/nav-pulo/index.html) |
| Menu que se transforma | [`pecas/menu-morfo/`](pecas/menu-morfo/index.html) |
| Menu em tela cheia | [`pecas/menu-tela-cheia/`](pecas/menu-tela-cheia/index.html) |
| Dock lêÂ­quido | [`pecas/dock-liquido/`](pecas/dock-liquido/index.html) |

**RodapêÂ©s**

| PeêÂ§a | Link |
|---|---|
| RodapêÂ© INEMA com fêÂ­sica | [`pecas/rodape-inema/`](pecas/rodape-inema/index.html) |
| RodapêÂ© cortina | [`pecas/rodape-cortina/`](pecas/rodape-cortina/index.html) |
| RodapêÂ© flor | [`pecas/rodape-flor/`](pecas/rodape-flor/index.html) |
| RodapêÂ© mapa | [`pecas/rodape-mapa/`](pecas/rodape-mapa/index.html) |
| RodapêÂ© quebra | [`pecas/rodape-quebra/`](pecas/rodape-quebra/index.html) |

**Galerias e imagens**

| PeêÂ§a | Link |
|---|---|
| Grade bento com moldura que desliza | [`pecas/bento-glide/`](pecas/bento-glide/index.html) |
| Galeria giro | [`pecas/galeria-giro/`](pecas/galeria-giro/index.html) |
| Rastro de imagens | [`pecas/rastro-imagens/`](pecas/rastro-imagens/index.html) |
| Adesivo hologrêÂ¡fico | [`pecas/adesivo-holo/`](pecas/adesivo-holo/index.html) |

**BotêÂµes e detalhes**

| PeêÂ§a | Link |
|---|---|
| BotêÂµes de geleia | [`pecas/botoes-geleia/`](pecas/botoes-geleia/index.html) |
| Cursor amigo | [`pecas/cursor-amigo/`](pecas/cursor-amigo/index.html) |
| Faixa flap | [`pecas/faixa-flap/`](pecas/faixa-flap/index.html) |
| Dia e noite | [`pecas/dia-noite/`](pecas/dia-noite/index.html) |

**PêÂ¡ginas especiais**

| PeêÂ§a | Link |
|---|---|
| 404 que vira jogo | [`pecas/404-corre/`](pecas/404-corre/index.html) |
| Revela carga | [`pecas/revela-carga/`](pecas/revela-carga/index.html) |

## Uso rêÂ¡pido

```bash
git clone https://github.com/inematds/inema-motion-lab && cd inema-motion-lab
python3 -m http.server 8850 --directory . --bind 127.0.0.1
# abra http://127.0.0.1:8850/pecas/busca-cmdk/   (acrescente ?demo=1 para a demonstraêÂ§êÂ£o nêÂ£o parar)

# testar e gravar (Node 18+, playwright e ffmpeg)
node tools/testar-pecas.cjs 8850
node tools/gravar-videos.cjs 8850
```

## CrêÂ©ditos

Prompts e cêÂ³digo escritos do zero para o INEMA.
ConteêÂºdo aberto e gratuito do [INEMA.CLUB](https://inema.club).

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>