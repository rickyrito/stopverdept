# Segurança e privacidade

## Superfície atual

O site serve ficheiros públicos e não implementa contas, base de dados, pagamentos ou receção de formulários. Os contactos comerciais estão publicados. Não guardar credenciais, dados de clientes ou documentos privados no repositório ou recursos.

Não há dependências de aplicação declaradas para atualizar por gestor de pacotes. Permanecem riscos de conteúdo, integrações externas, JavaScript malicioso e acesso indevido ao repositório ou alojamento.

## Consentimento e terceiros

- Língua e consentimento ficam em `localStorage`. A interface chama-lhes cookies, mas as preferências próprias usam este armazenamento.
- O mapa usa `data-src` e só carrega após aceitação funcional. Revogar muda o endereço para `about:blank` e oculta o mapa; não desfaz dados já transmitidos.
- As fontes Google carregam antes da escolha; alojá-las localmente é uma melhoria pendente.
- WhatsApp, Facebook e Google Maps externo têm políticas próprias.
- Não existe expiração explícita do consentimento. A presença do banner não comprova conformidade legal integral.

Verificar os pedidos de rede conforme [Testes](TESTING.md). Novos conteúdos externos opcionais devem ser bloqueados até à aceitação correspondente.

## Regras de alteração

- Manter traduções usadas com `innerHTML` sob controlo do projeto, sem dados não confiáveis.
- Preservar `rel="noopener"` com `target="_blank"`; usar também `noreferrer` quando se pretenda omitir a referência.
- Rever URLs, SVG e recursos externos. Acompanhar autorizações de logótipos no [inventário](../inventory.md).
- Não colocar segredos em HTML, JavaScript, `.env` ou outros ficheiros que possam ser publicados.
- Definir tratamento e informação ao visitante antes de acrescentar recolha de dados, formulários ou análise de tráfego.
- O HTML não declara Content Security Policy. Os cabeçalhos do alojamento não foram auditados nesta revisão.

## Comunicação e resposta

Não há canal privado dedicado de segurança registado nem política na raiz. Comunicar vulnerabilidades ao responsável de manutenção por um canal privado acordado. Não publicar credenciais, dados pessoais ou detalhes de exploração numa issue pública.

Perante exposição, remover conteúdo público, corrigir a origem e verificar histórico e versão publicada. Credenciais expostas devem ser revogadas; removê-las do último ficheiro não elimina o histórico. Confirmar a publicação corrigida antes de considerar o incidente resolvido.
