# CLAUDE.md

Site da **Stopverde, Lda.** — oficina auto multimarcas na Pontinha (Odivelas).
Feito em colaboração com o dono da oficina, para substituir o antigo site Webnode
(`stopverde.webnode.pt`).

- Site publicado: https://rickyrito.github.io/stopverdept/
- Repositório: https://github.com/rickyrito/stopverdept
- Inventário de conteúdos e pendentes: [inventory.md](inventory.md)

## Estrutura

Site estático numa só página, sem build, sem dependências.

```
index.html               Página única: HTML + CSS + JS (menu, ano, animações, PT/EN e consentimento)
assets/stopverde.svg     Símbolo da marca (sinal de STOP verde); também é o favicon
assets/valores/*.svg     Ícones dos valores: confianca, simpatia, qualidade
assets/marcas/*          Logótipos das marcas, seguradoras e parceria
.nojekyll                Desliga o Jekyll no GitHub Pages
```

Secções de `index.html` (âncoras do menu): `#inicio`, `#sobre`, `#servicos`,
faixa "Tem um problema…", `#precos`, `#parceiros`, `#contactos`.

## Publicar

O GitHub Pages serve a branch `main`, pasta raiz. Cada push para `main` publica.

```sh
git push origin main
# confirmar que o build terminou para o último commit:
gh api repos/rickyrito/stopverdept/pages/builds/latest -q '.status+" "+.commit'
```

Para ver localmente: `python3 -m http.server` na raiz e abrir http://localhost:8000.

## Identidade visual

- **Símbolo:** sinal de STOP octogonal **verde** (o vermelho do STOP é substituído
  pelo verde), borda branca, "STOP" a branco. Não reintroduzir vermelho na marca.
- **Nome:** "STOP" a branco + "VERDE" a verde (sobre fundo escuro), por baixo
  "SERVIÇOS AUTO".
- **Cores** (variáveis em `:root`): verde `--green #1fbf43`, verde escuro
  `--green-dark #127b2a`, fundos escuros `--black #101713`, `--dark #101713`,
  `--dark-2 #1b2520`. Texto secundário em fundo claro: `--muted #656970`.
  Usar texto escuro sobre o verde principal e branco sobre o verde escuro.
  `--red` existe mas não é usado na marca.
- **Letra:** Poppins 600 nos títulos, com espaçamento apertado entre letras;
  Poppins 800 no nome da marca e Roboto no texto (Google Fonts).
- **Estilo:** composição assimétrica no topo, símbolo STOP verde original em
  grande plano, geometria técnica e fundos verde-carvão alternados com branco
  suave. Títulos em escrita normal, serviços numerados e secções com espaço.
  O símbolo original em `assets/stopverde.svg` mantém-se intacto.
- O `<text>` do `stopverde.svg` usa `textLength` para caber no octógono com
  qualquer letra de recurso — manter isso se o editar.

## Regras de conteúdo

- Língua: português de Portugal.
- **Não inventar factos** (preços, seguradoras, fornecedores, anos de experiência,
  garantias, horários). Só usar dados confirmados pelo dono — ver
  [inventory.md](inventory.md). Onde falta informação, usar "Sob consulta" ou
  "Em construção".
- "Quem Somos" fala de **continuidade e confiança** ("A sua oficina de sempre").
  Não mencionar a fusão Pontelectro/Garepol.
- Contactos (telefone, email, morada, horário) aparecem em vários sítios: barra do
  topo, faixa verde, secção Contactos e rodapé. Ao alterar um, alterar todos.
- WhatsApp (telemóvel 960 219 587, link `https://wa.me/351960219587`) aparece na
  barra do topo, na secção Contactos e no botão flutuante "Fale connosco"
  (`.wa-float`, canto inferior direito, botão arredondado com ícone circular). O rodapé
  tem `padding-bottom` extra para o botão não tapar o texto.
  O ícone do WhatsApp é o balão de conversa com um **volante** lá dentro
  ("conduzimos o seu problema até à solução"); manter este ícone em todos os sítios.
- A secção Preços é propositadamente divertida ("A parte que ninguém gosta"):
  Preçómetro animado (ponteiro de Ai! até Justo) e serviços como luzes do painel
  que piscam ao entrar no ecrã. Respeita `prefers-reduced-motion`.
- Marcas (Bosch, Liqui Moly, Osram, Michelin, Monroe), seguradoras (Fidelidade,
  Allianz Auto) e parcerias (DECO PROteste) aparecem com logótipos oficiais em
  `#parceiros`, guardados em `assets/marcas/`, a pedido do cliente. A autorização
  de utilização continua por confirmar no inventário; não acrescentar outros
  logótipos sem autorização confirmada.
- **Bilingue PT/EN:** o português está no HTML; o inglês está no objeto `EN` do
  `<script>`, por chave `data-i18n` (texto) ou `data-i18n-attr="atributo:chave"`.
  Todo o texto novo precisa das duas línguas. Língua inicial: `?lang=` → escolha
  guardada (`stopverde-lang`) → língua do browser.
- **Cookies:** banner + janela "Personalizar as preferências de consentimento"
  (inspirado em sodicentro.pt/CookieYes). Categorias: Necessário (sempre ativo) e
  Funcional (mapa da Google). O mapa só carrega com consentimento funcional
  (`iframe[data-src]`). Escolha em `localStorage` `stopverde-consent`.
  As fontes Google são carregadas logo na abertura, fora deste mecanismo; alojá-las
  localmente é uma melhoria pendente. Se forem acrescentados outros conteúdos
  externos opcionais, incluí-los nas preferências e bloquear o carregamento
  até à escolha correspondente.
- Sem formulários: o GitHub Pages não processa envios. Usar `tel:` e `mailto:`.

## Verificar antes de publicar

- Responsivo: menu ☰ até 1080px; quebras em 1180/1080/960/760/560/360px e telemóvel
  na horizontal. Testar 320–1280px nas duas línguas sem scroll horizontal (o Chrome
  headless não abre janelas < ~500px: testar dentro de um iframe com a largura certa).
- Acessibilidade: verificar contraste, rótulo Abrir/Fechar do menu em PT/EN e
  retorno do foco ao fechar ou guardar as preferências de cookies.
- Ícones novos: desenhar em SVG e confirmar o aspeto (por ex. `qlmanage -t -s 300 ficheiro.svg`).
- Depois do push, confirmar o build e abrir o site publicado.
