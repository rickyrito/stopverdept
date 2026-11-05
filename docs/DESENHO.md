# Desenho e especificação visual

## Referência e percurso

A referência implementada é o [HTML](../index.html) e os [recursos da marca](../assets/). Não existe ligação Figma ou protótipo externo registado.

O visitante conhece a oficina, explora os serviços, consulta preços e contacta por telefone ou WhatsApp. O menu dá acesso às secções; o cabeçalho permite mudar PT/EN. O mapa requer consentimento funcional. Não existe marcação ou pagamento dentro do site.

## Identidade

O [símbolo original](../assets/stopverde.svg) é um octógono STOP verde, com contorno e letras brancas. Surge no cabeçalho, topo, rodapé e favicon. Preservar a geometria e `textLength` do texto SVG.

| Variável CSS | Cor | Utilização |
|---|---|---|
| `--green` | `#1fbf43` | Marca e chamadas para ação |
| `--green-dark` | `#127b2a` | Destaques sobre fundos claros |
| `--black`, `--dark` | `#101713` | Fundos verde-carvão e títulos |
| `--dark-2` | `#1b2520` | Superfícies escuras secundárias |
| `--text` | `#48534b` | Texto principal |
| `--muted` | `#656970` | Texto secundário |
| `--line` | `#dce2da` | Separadores |
| `--light` | `#f3f5ef` | Fundos claros alternados |

`--red` existe, mas não deve passar a cor da marca. Usar texto escuro sobre verde principal e branco sobre verde escuro; voltar a medir contraste quando as cores mudarem.

Tipografia: Poppins 600 nos títulos, Poppins 800 na marca e Roboto no corpo. Os títulos têm espaçamento apertado. As fontes vêm atualmente do Google Fonts.

## Componentes

- Cabeçalho aderente com âncoras, PT/EN e menu de telemóvel.
- Topo assimétrico, símbolo em destaque e geometria técnica.
- Apresentação em duas colunas e três valores ilustrados.
- Oito serviços numerados com SVG.
- Preçómetro animado e luzes do painel, com preços «Sob consulta».
- Logótipos em placas claras; contactos e mapa com alternativa sem incorporação.
- Apresentação InterGarage em cartão de duas colunas (uma até 760 px), seguida de 27 logótipos locais em grelha branca: nove colunas em computador, seis até 960 px, quatro até 760 px, três até 560 px e duas até 360 px. Os logótipos preservam as cores e proporções. Seguradoras e parcerias diretas surgem em duas colunas, reduzidas a uma até 760 px. Não existem blocos «Fornecedores» ou «Marcas com que trabalhamos».
- WhatsApp fixo com ícone de volante e espaço reservado no rodapé.
- Banner e janela de consentimento: Necessário e Funcional.

Não existe biblioteca UI, Tailwind ou tema claro/escuro selecionável. Os fundos claros e escuros integram a mesma composição.

## Adaptação e acessibilidade

O contentor tem máximo de 1280 px. Há quebras a 1180, 1080, 960, 760, 560 e 360 px e ajustes para orientação horizontal de pouca altura. O menu compacto aparece até 1080 px. Validar de 320 a 1280 px em PT/EN.

Preservar ligação para saltar conteúdo, foco visível, rótulos, estados ARIA, título do mapa e foco da janela. As animações respeitam `prefers-reduced-motion`. Estes mecanismos não substituem uma auditoria; consultar [Testes](TESTING.md).
