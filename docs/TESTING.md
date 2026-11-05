# Diretrizes de testes

## Estratégia

Não existem testes automatizados, runner, mocks ou pipeline de CI versionados no repositório analisado. A validação do site é manual em HTTP local, seguida de confirmação após publicação autorizada. Os pontos abaixo são verificações a executar, não resultados obtidos.

Para alterações documentais, verificar coerência com o código, ligações relativas, ausência de campos de modelo e `git diff --check`. Alterações visuais ou funcionais exigem os cenários aplicáveis abaixo.

## Preparação

Servir conforme [Ambiente](ENVIRONMENT.md). Usar ferramentas do navegador para consola, rede, armazenamento e dimensões. Testar estado limpo e preferências guardadas. Para limpar preferências, remover `stopverde-lang` e `stopverde-consent` do armazenamento da origem local.

## Conteúdo e navegação

- [ ] Âncoras chegam à secção correta, sem o cabeçalho ocultar títulos.
- [ ] Destinos de telefone, email, WhatsApp e Facebook coincidem com o [inventário](../inventory.md); inspecionar URLs sem enviar mensagens ou fazer chamadas.
- [ ] Recursos e favicon carregam sem erros; consola sem erros JavaScript.
- [ ] Contactos e horários são coerentes; preços não confirmados continuam «Sob consulta».
- [ ] Ano do rodapé acompanha a data do dispositivo.

## PT/EN

- [ ] `?lang=pt` e `?lang=en` prevalecem sobre preferência guardada diferente.
- [ ] O botão atualiza textos, atributos, título, descrição, `html[lang]` e rótulos.
- [ ] A escolha pelo botão persiste ao recarregar sem parâmetro.
- [ ] Sem parâmetro nem preferência, usa-se PT se alguma língua do navegador começar por `pt`; caso contrário, EN.
- [ ] Texto novo tem tradução, sem fragmentos indevidos em português no modo EN.
- [ ] Com armazenamento bloqueado, a troca funciona durante a visita sem erros não tratados.

## Consentimento e mapa

- [ ] Na primeira visita, aparece o banner e não há pedido do mapa incorporado. Fontes Google são a exceção externa conhecida.
- [ ] Rejeitar guarda `functional: false`, mantém o mapa bloqueado e esconde o banner.
- [ ] Aceitar permite o mapa; deslocar até à secção para verificar o carregamento diferido.
- [ ] Personalizar e guardar respeita Funcional; Necessário permanece ativo.
- [ ] Reabrir mostra a escolha atual; revogar oculta o mapa e muda o endereço para `about:blank`.
- [ ] Recarregar preserva a escolha; fechar sem escolher não concede consentimento.
- [ ] A ligação externa Google Maps está disponível sem incorporar o mapa.

## Ecrãs e acessibilidade

- [ ] Verificar 320, 360, 560, 760, 960, 1080, 1180 e 1280 px, incluindo valores próximos das quebras, em PT/EN, sem deslocamento horizontal.
- [ ] Até 1080 px, o menu fecha por botão, ligação, clique fora e Escape; ao voltar para computador, o estado é reposto.
- [ ] Na horizontal em telemóvel, menu e preferências continuam utilizáveis.
- [ ] WhatsApp, banner e janela não impedem acesso a contactos e rodapé.
- [ ] Teclado: ligação para saltar conteúdo, foco visível e ordem útil.
- [ ] Janela: Tab/Shift+Tab fica no diálogo, Escape fecha e o foco regressa a elemento visível.
- [ ] Leitor de ecrã: nomes, estado do menu, língua e título do mapa.
- [ ] Movimento reduzido: animações desnecessárias desativadas; verificar também contraste e zoom a 200%.
- [ ] Sem JavaScript, conteúdo base português legível; registar limitações dos controlos.

Usar emulação ou iframe com largura definida se a janela não permitir dimensões estreitas. Quando possível, complementar com telemóvel real e navegadores de motores diferentes.

## Publicação

- [ ] `git diff --check` sem problemas e alterações revistas.
- [ ] Após publicação autorizada, build concluído para o commit pretendido.
- [ ] Site público carrega recursos em `/stopverdept/` e funciona em PT/EN; verificar contactos e consentimento.

Registar verificações executadas, navegador, dimensões, resultados e limitações. Esta lista não equivale a auditoria de acessibilidade ou privacidade concluída.
