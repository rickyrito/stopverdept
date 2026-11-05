# Guia de contribuição

## Antes de alterar

Ler as [regras](../CLAUDE.md), a [arquitetura](ARCHITECTURE.md) e o [inventário](../inventory.md). Consultar `git status --short` e preservar alterações locais existentes. Criar uma branch para trabalho a rever, por exemplo:

```powershell
git switch -c docs/atualizar-documentacao
```

Adaptar o nome ao objetivo. Não há convenção de nomes imposta por configuração no repositório.

## Convenções

- Preservar o estilo existente: dois espaços no HTML, CSS e JavaScript; não introduzir compilação para alterações pequenas.
- Guardar texto em UTF-8 e usar português de Portugal no conteúdo base e documentação.
- Usar caminhos relativos nos recursos e ligações internas. Preferir SVG para ícones quando adequado e verificar o aspeto.
- Para texto novo, adicionar `data-i18n` e tradução no objeto `EN`. Para atributos, usar `data-i18n-attr="atributo:chave"`, separando pares com `;`.
- Atualizar contactos em todas as ocorrências e não substituir dados pendentes por suposições.
- Preservar teclado, movimento reduzido e bloqueio do mapa antes do consentimento.
- Atualizar o [inventário](../inventory.md) quando o conteúdo mudar e o [registo](REGISTRY.md) para decisões estruturais.

## Revisão e commit

Cumprir as verificações aplicáveis em [Testes](TESTING.md) e rever:

```powershell
git diff --check
git diff
git status --short
```

Selecionar com `git add` os caminhos concretos pretendidos. O histórico usa mensagens curtas em português, por exemplo «Moderniza o design preservando a identidade STOP verde». Não incluir temporários, dados privados ou credenciais.

Numa proposta de alteração, descrever problema, comportamento final e verificações efetivamente realizadas. Não há modelo de PR ou pipeline de testes versionado no estado analisado.

## Publicação

Publicar apenas quando autorizado para esse efeito. O procedimento histórico publica a raiz de `main` no GitHub Pages:

```powershell
git push origin main
```

Executar na branch `main` com os commits pretendidos; não é um passo automático de edição. Com GitHub CLI instalada e autenticada, consultar:

```powershell
gh api repos/rickyrito/stopverdept/pages/builds/latest -q '.status+" "+.commit'
```

Confirmar sucesso e correspondência do commit. Se o endpoint não refletir o método configurado, consultar Pages e Actions no GitHub. Abrir o site público e verificar recursos, contactos, línguas e consentimento.
