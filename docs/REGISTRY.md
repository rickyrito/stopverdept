# Registo de alterações e decisões

## Decisões documentadas

As decisões seguintes descrevem o código e as instruções históricas. Foram formalizadas nesta documentação em 5 de novembro de 2026; a data original de aprovação não está registada.

### ADR-001 — Site estático de página única

- **Contexto:** apresentar oficina, serviços e contactos com alojamento simples.
- **Decisão observada:** HTML, CSS e JavaScript nativo no [ficheiro principal](../index.html), recursos locais e publicação documentada no GitHub Pages.
- **Consequências:** sem compilação ou infraestrutura de aplicação; não há processamento próprio de envios. O crescimento do ficheiro exige revisão cuidadosa.

### ADR-002 — Português no HTML e inglês por chaves

- **Contexto:** duas línguas sem framework.
- **Decisão observada:** `data-i18n` e `data-i18n-attr` ligam conteúdo ao objeto `EN`; escolha por URL, armazenamento e navegador.
- **Consequências:** atualizar ambas as línguas e rótulos. O português continua legível sem JavaScript; a tradução depende dele.

### ADR-003 — Mapa condicionado ao consentimento

- **Contexto:** mostrar localização sem carregar automaticamente o mapa.
- **Decisão observada:** guardar escolha em `localStorage` e copiar `data-src` para `src` após aceitação funcional; oferecer ligação externa alternativa.
- **Consequências:** testar aceitação, rejeição e revogação. Fontes Google permanecem fora deste mecanismo, uma limitação conhecida.

### ADR-004 — Preservar a identidade STOP verde

- **Contexto:** modernizar a composição mantendo o símbolo.
- **Decisão registada:** conservar o [símbolo verde](../assets/stopverde.svg), fundos verde-carvão, Poppins e Roboto; composição assimétrica e serviços numerados.
- **Consequências:** manter identidade e verificar contraste e adaptação em PT/EN.

## Histórico relevante

| Data | Commit | Alteração registada |
|---|---|---|
| 2026-11-04 | `2b3bbc5` | WhatsApp na barra, contactos e botão flutuante |
| 2026-11-04 | `f8e021e` | Preçómetro, luzes e WhatsApp com volante |
| 2026-11-04 | `89ce258` | Marcas Bosch, Liqui Moly, Osram, Michelin e Monroe |
| 2026-11-04 | `07620c4` | Seguradoras e parceria DECO PROteste |
| 2026-11-04 | `a69d048` | Logótipos oficiais, PT/EN, consentimento e ajustes responsivos |
| 2026-11-04 | `a0174fc` | Modernização visual preservando o STOP verde |

## Diário de manutenção

- **2026-11-05 — Parceiros com logótipos:** por pedido do cliente, removidos «Fornecedores» e «Marcas com que trabalhamos». A lista textual InterGarage foi substituída por grelha responsiva com os 27 logótipos obtidos no site oficial, alojados localmente; origens e dimensões em [sources.json](../assets/marcas/intergarage/sources.json). Removidos os estilos e traduções dos blocos retirados e ajustadas seguradoras e parcerias diretas a duas colunas. Validados os 27 logótipos por descodificação no navegador, traduções e sintaxe JavaScript; sem deslocamento horizontal em PT/EN nas oito larguras de 320 a 1280 px. Confirmada ausência dos blocos antigos na página e nos seletores e traduções correspondentes.
- **2026-11-05 — InterGarage:** acrescentada em PT/EN a adesão confirmada pelo cliente, explicação da rede e 27 marcas parceiras consultadas no site oficial. Menu e referência em Quem Somos atualizados; seguradoras e parcerias diretas preservadas. As marcas da rede usam nomes em texto, sem novos logótipos ou carregamentos externos. Divergência do horário na captura registada no inventário para confirmação. Validados sintaxe JavaScript, 141 chaves de tradução sem faltas e ausência de deslocamento horizontal nas larguras 320, 360, 560, 760, 960, 1080, 1180 e 1280 px, nas duas línguas. No navegador, confirmados alternância EN→PT, navegação pelo menu móvel e mapa bloqueado após rejeição, sem erros JavaScript observados.
- **2026-11-05:** preenchidos a apresentação, regras para agentes e guias técnicos a partir do código local, inventário e histórico. Removidos exemplos genéricos; mantidas confirmações comerciais pendentes. Sem alterações ao site, publicação ou pesquisa externa. A revisão documental não constitui validação funcional em navegador.

Para novos registos, indicar data, alteração, motivo e verificações realizadas. Não registar propostas como trabalho concluído.
