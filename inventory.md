# Inventário — site Stopverde

Estado do conteúdo do site https://rickyrito.github.io/stopverdept/ e o que falta
pedir ao dono da oficina. Atualizado a 4 de novembro de 2026.

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
| Topo | `#inicio` | Sinal STOP verde, "Oficina Multimarcas · Pontinha", título "O seu carro em boas mãos", frase de apresentação, botões Ligar / Serviços | Novo | Validar texto |
| Quem Somos | `#sobre` | "A sua oficina de sempre" + texto sobre continuidade e confiança | Novo | Validar texto |
| Valores | `#sobre` | Confiança (Trabalho transparente), Simpatia (Atendimento próximo), Qualidade (Serviço garantido) | Novo, frases dadas pelo cliente | ✅ |
| Serviços | `#servicos` | 8 serviços (lista abaixo) + "…e muito mais!" | Nomes: Webnode · Descrições: Novo | Validar descrições |
| Faixa | — | "Tem um problema com o seu carro?" + telefone | Novo | ✅ |
| Preços | `#precos` | "A parte que ninguém gosta": Preçómetro animado + luzes do painel (Mudanças de óleo, Revisões, Mão de obra/hora — todos "Sob consulta") + botões WhatsApp/Ligar | Itens: Webnode · Textos e animação: Novo | ⏳ Faltam preços · validar textos |
| Seguradoras e Fornecedores | `#parceiros` | Seguradoras: Fidelidade, Allianz Auto · Fornecedores: remete para as marcas · Parcerias: DECO PROteste · Faixa "Marcas com que trabalhamos" | Cliente | ✅ (logótipos por confirmar) |

## Seguradoras e parcerias

Indicadas pelo cliente. Mostradas com o logótipo oficial.

| Nome | Onde aparece | Logótipo |
|---|---|---|
| Fidelidade | Seguradoras | `assets/marcas/fidelidade.png` (site oficial) |
| Allianz Auto | Seguradoras | `assets/marcas/allianz.svg` (Wikimedia) |
| DECO PROteste | Parcerias | `assets/marcas/deco.svg` (site oficial) |

## Marcas com que trabalham

Indicadas pelo cliente. Logótipos oficiais em `assets/marcas/` (Wikimedia Commons).

| Marca | Categoria no site |
|---|---|
| Bosch | Peças auto |
| Liqui Moly | Óleos |
| Osram | Iluminação |
| Michelin | Pneus |
| Monroe | Amortecedores |
| Contactos | `#contactos` | Telefone, morada, email, Facebook, horário, mapa Google | Webnode | ✅ |

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
- [ ] Lista de seguradoras com quem trabalham
- [ ] Confirmar a relação com a DECO PROteste (o que se pode dizer publicamente)
- [ ] Confirmar autorização para os logótipos oficiais (já estão no site, a pedido do cliente) das marcas (Fidelidade, Allianz, DECO PROteste, Bosch, Liqui Moly, Osram, Michelin, Monroe) — ex.: material de distribuidor/oficina aderente
- [ ] Confirmar a categoria da Bosch (está "Peças auto")
- [ ] Fotografias reais da oficina, da equipa e de trabalhos feitos (para o topo e as secções)
- [ ] Validar os textos marcados como **Novo**
- [ ] Confirmar se abrem ao domingo ou em feriados
- [ ] Domínio próprio (ex.: `stopverde.pt`) — configurar no GitHub Pages quando existir
- [ ] Desativar ou redirecionar o site antigo `stopverde.webnode.pt` quando o novo for o oficial

## Funcionalidades

- Site em **português e inglês** (botão PT/EN no cabeçalho; `?lang=en` abre em inglês). Textos em inglês: Novo — validar.
- **Consentimento de cookies** (banner + preferências; Necessário / Funcional). O mapa da Google só aparece com consentimento.
- **Responsivo** testado de 320px a 1280px, nas duas línguas.
