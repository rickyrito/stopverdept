# Investigação e contexto

## Objetivo e âmbito

Substituir o site Webnode por uma página estática que facilite conhecer os serviços e contactar a oficina. Este documento reúne evidências existentes e questões em aberto. A revisão documental inicial usou apenas o repositório; a atualização InterGarage incluiu consulta do site oficial, conforme descrito abaixo. Não foi realizada análise de concorrentes ou recolha de métricas comerciais.

## Fontes disponíveis

| Fonte | Evidência | Limitação |
|---|---|---|
| [Inventário](../inventory.md) | Dados da empresa, origens e pendentes | Itens assinalados requerem confirmação do dono |
| [HTML](../index.html) | Conteúdo e comportamento implementados | Não comprova o estado publicado nem qualidade visual em todos os dispositivos |
| Histórico Git | Evolução e intenção registada nos commits | Não demonstra aprovação comercial ou jurídica |
| https://stopverde.webnode.pt/ | Endereço identificado como site anterior | Não consultado nesta revisão |
| https://rickyrito.github.io/stopverdept/ | Endereço público registado | Não consultado nesta revisão |

## Descobertas

### Rede InterGarage — 5 de novembro de 2026

O cliente confirmou a adesão da Stopverde e enviou uma captura da sua listagem
na rede. O [site oficial InterGarage](https://www.intergarage.pt/) foi consultado
para explicar a rede multimarcas, a formação, os procedimentos técnicos e as
peças de qualidade, e identificar as 27 marcas apresentadas como parceiras.
Estas são identificadas no site como parceiras da rede. A lista pode mudar;
voltar a consultar a fonte quando for necessário atualizá-la.

A captura contém um horário diferente do site da Stopverde. A confirmação
ficou pendente no [inventário](../inventory.md), sem substituir o horário atual.

### Código e conteúdo

- A arquitetura estática serve divulgação e contacto direto, sem processamento de formulários.
- PT/EN está implementado, incluindo metadados e rótulos; textos novos precisam de validação do cliente.
- O mapa depende de consentimento funcional; fontes Google carregam antes da escolha.
- Não há ferramentas de análise de tráfego declaradas no HTML nem métricas de conversão registadas.
- Existem título, descrição, favicon e ligações de línguas alternativas. Faltam dados estruturados da oficina, metadados de partilha social e ligação canónica.
- Não existem fotografias reais da oficina nos recursos atuais.

## Próximos levantamentos

1. Confirmar preços ou manutenção de «Sob consulta», textos PT/EN e horários de domingo e feriados.
2. Validar relação pública com DECO PROteste, categoria Bosch e autorizações dos logótipos.
3. Obter fotografias e decidir domínio próprio e transição do Webnode.
4. Avaliar alojamento local das fontes e informação de privacidade.
5. Validar composição e percursos nas duas línguas, conforme [Testes](TESTING.md).

Os pendentes comerciais ficam no [inventário](../inventory.md). Recomendações futuras devem indicar fonte e data de consulta, distinguindo observação, hipótese e decisão aprovada. Não atribuir resultados comerciais, desempenho ou conformidade sem medição.
