# Inventário — site Stopverde

Estado do conteúdo do site https://rickyrito.github.io/stopverdept/ e o que falta
pedir ao dono da oficina. Atualizado a 5 de novembro de 2026.

Legenda da origem: **Webnode** = veio do site antigo `stopverde.webnode.pt` ·
**Novo** = texto escrito para o site novo (o dono deve validar).

## Dados da empresa

| Dado | Valor | Origem |
|---|---|---|
| Nome | Stopverde, Lda. | Webnode |
| Morada | Av. de São Pedro, Lote R-7 Loja A, 1675-129 Pontinha – Odivelas | Webnode |
| Telefone | 214 794 122 | Webnode |
| Telemóvel / WhatsApp | 960 219 587 (`wa.me/351960219587`) — barra do topo, Contactos, botão flutuante | Cliente |
| Email | stopverde@sapo.pt | Webnode |
| Facebook | https://www.facebook.com/Stopverde/ | Webnode |
| Horário | Seg–Sex 8:30–18:30 (almoço 13:00–14:30) · Sáb 9:00–13:00 | Webnode |
| Domingo | Não indicado (não aparece no site) | — |

## Secções da página

| Secção | Âncora | Conteúdo | Origem | Estado |
|---|---|---|---|---|
| Topo | `#inicio` | Sinal STOP verde, "Oficina Multimarcas · Pontinha", título "O seu carro em boas mãos.", símbolo STOP verde em destaque, frase de apresentação, botões Ligar / Explorar serviços e faixa de morada | Novo | Validar texto |
| Quem Somos | `#sobre` | "A sua oficina de sempre" + texto sobre continuidade e confiança | Novo | Validar texto |
| Valores | `#sobre` | Confiança (Trabalho transparente), Simpatia (Atendimento próximo), Qualidade (Serviço garantido) | Novo, frases dadas pelo cliente | ✅ |
| Serviços | `#servicos` | 8 serviços (lista abaixo) + "…e muito mais!" | Nomes: Webnode · Descrições: Novo | Validar descrições |
| Faixa | — | "Tem um problema com o seu carro?" + telefone | Novo | ✅ |
| Preços | `#precos` | "A parte que ninguém gosta": Preçómetro animado + luzes do painel (Mudanças de óleo, Revisões, Mão de obra/hora — todos "Sob consulta") + botões WhatsApp/Ligar | Itens: Webnode · Textos e animação: Novo | ⏳ Faltam preços · validar textos |
| Rede e Parcerias | `#parceiros` | Apresentação da rede InterGarage e grelha com 27 logótipos dos parceiros · Seguradoras: Fidelidade, Allianz Auto · Parcerias: DECO PROteste | Cliente e site oficial InterGarage | Adesão e apresentação dos parceiros indicadas pelo cliente; autorizações dos logótipos por confirmar |
| Contactos | `#contactos` | Telefone, morada, email, Facebook, horário, mapa Google | Webnode | ✅ |

## Rede InterGarage

A adesão da Stopverde à rede foi confirmada pelo cliente em 5 de novembro de
2026, com captura da listagem «STOPVERDE» no site oficial. A apresentação da
rede e as marcas parceiras foram consultadas em https://www.intergarage.pt/
nessa data. O site da Stopverde inclui a explicação em PT/EN e uma ligação
para a InterGarage, além de uma referência na secção Quem Somos.

Marcas listadas pela rede: APLUS, Blue Print, Bosch, Delphi, DELS, ELF, Gates,
Geimex, IADA, MANN-FILTER, MANNOL, Mecafilter, NAPA, NRF, Purflux, Schaeffler
Group, Shell, SKF, SWAG, TAB, Total Lubricants, TRW, Valeo, Valvoline,
Veneporte, Wolf e ZF. São apresentadas como **parceiras da rede**, sem afirmar
uma relação direta individual de cada marca com a Stopverde. A pedido do
cliente, os nomes foram substituídos pelos 27 logótipos apresentados no site
oficial da rede, guardados localmente em [assets/marcas/intergarage/](assets/marcas/intergarage/).
Os endereços de origem e as dimensões estão em [sources.json](assets/marcas/intergarage/sources.json).
Não há carregamento de imagens de terceiros durante a visita ao site.

A captura enviada apresenta um horário diferente: segunda a sexta,
09:00–13:00 e 16:00–18:00. O horário atual da Stopverde foi mantido até
confirmação do cliente; a captura não foi usada para substituir os contactos
ou a morada do site.

## Seguradoras e parcerias

Indicadas pelo cliente. Mostradas com o logótipo oficial, a pedido do cliente;
a autorização de utilização dos logótipos e o âmbito público da parceria DECO
continuam pendentes de confirmação.

| Nome | Onde aparece | Logótipo |
|---|---|---|
| Fidelidade | Seguradoras | `assets/marcas/fidelidade.png` (site oficial) |
| Allianz Auto | Seguradoras | `assets/marcas/allianz.svg` (Wikimedia) |
| DECO PROteste | Parcerias | `assets/marcas/deco.svg` (site oficial) |

## Blocos substituídos

Em 5 de novembro de 2026, por pedido do cliente, foram retirados do site o
bloco «Fornecedores» e a lista «Marcas com que trabalhamos» (Bosch, Liqui Moly,
Osram, Michelin e Monroe). A grelha «Parceiros InterGarage» apresenta os
parceiros da rede. Bosch surge apenas nessa qualidade. Os ficheiros antigos
continuam no repositório, sem utilização na página.

## Serviços

| Serviço | Descrição no site (Novo) |
|---|---|
| Revisões Gerais | Manutenção periódica para todas as marcas. |
| Chapa e Pintura | Reparação de carroçaria e pintura. |
| Correias de Distribuição | Substituição de kits de distribuição. |
| Kits de Embraiagem | Diagnóstico e substituição de embraiagens. |
| Mudanças de Óleo | Óleo e filtros trocados no momento certo. |
| Serviços Rápidos | Pequenas reparações sem complicações. |
| Focagem de Faróis | Faróis bem alinhados, melhor visibilidade. |
| Inspeções | Preparamos o seu carro para a inspeção. |

## Ficheiros de imagem

| Ficheiro | O que é | Onde aparece |
|---|---|---|
| `assets/stopverde.svg` | Símbolo: sinal de STOP verde com "STOP" a branco | Cabeçalho, topo da página, rodapé, favicon |
| `assets/valores/confianca.svg` | Aperto de mão em círculo verde | Valor Confiança |
| `assets/valores/simpatia.svg` | Cara sorridente com coração vermelho | Valor Simpatia |
| `assets/valores/qualidade.svg` | Medalha com visto | Valor Qualidade |

O logótipo antigo (STOP vermelho com carro, `logo.jpg`) foi removido; está no
histórico do Git (commit `6adcb2a`).

## Pendentes — pedir ao dono

- [ ] Preços de revisões, mudanças de óleo e mão de obra/hora (ou confirmar "Sob consulta")
- [x] Lista de seguradoras indicada pelo cliente: Fidelidade e Allianz Auto
- [x] Adesão à rede InterGarage confirmada pelo cliente; apresentação e marcas da rede acrescentadas em PT/EN
- [ ] Confirmar o horário atual: a listagem InterGarage enviada pelo cliente diverge do horário no site da Stopverde
- [ ] Confirmar a relação com a DECO PROteste (o que se pode dizer publicamente)
- [ ] Confirmar autorização para os logótipos oficiais apresentados a pedido do cliente: Fidelidade, Allianz, DECO PROteste e os 27 parceiros InterGarage — ex.: material de distribuidor/oficina aderente
- [ ] Fotografias reais da oficina, da equipa e de trabalhos feitos (para o topo e as secções)
- [ ] Validar os textos marcados como **Novo**
- [ ] Confirmar se abrem ao domingo ou em feriados
- [ ] Domínio próprio (ex.: `stopverde.pt`) — configurar no GitHub Pages quando existir
- [ ] Desativar ou redirecionar o site antigo `stopverde.webnode.pt` quando o novo for o oficial

## Funcionalidades

- Site em **português e inglês** (botão PT/EN no cabeçalho; `?lang=en` abre em inglês). Textos em inglês: Novo — validar.
- **Consentimento de cookies** (banner + preferências; Necessário / Funcional). O mapa da Google só aparece com consentimento.
- **Design atualizado:** topo assimétrico com símbolo original, serviços numerados, fundos claros e verde-carvão, contactos em destaque.
- **Responsivo:** regras para computador e telemóvel implementadas; validar visualmente a nova composição de 320px a 1280px nas duas línguas antes de publicar.

## Melhorias técnicas pendentes

- [ ] Alojar Poppins e Roboto localmente; atualmente o Google Fonts carrega antes da escolha de consentimento.
- [ ] Acrescentar dados estruturados da oficina, metadados de partilha social e definir o URL canónico.
