# Ambiente e configuração

## Requisitos

Um navegador moderno permite consultar o site; editor de texto e Git permitem mantê-lo. Para servir localmente, usar Python 3 ou um servidor estático já disponível no editor. Não são necessários Node.js, npm, base de dados ou instalação de pacotes.

Na sessão de documentação de 5 de novembro de 2026, Python e o lançador `py` não foram encontrados no PATH. Os comandos seguintes destinam-se a uma máquina com Python instalado; não foram executados nesta revisão.

## Arranque local

Na raiz do repositório:

```powershell
python -m http.server 8000 --bind 127.0.0.1
```

No Windows com lançador Python, pode usar-se `py` em vez de `python`. Abrir http://127.0.0.1:8000/; forçar PT com `?lang=pt` e EN com `?lang=en`. Parar com `Ctrl+C`. Se a porta estiver ocupada, escolher outra e atualizar o endereço.

Como alternativa, usar um servidor estático do editor com a raiz do repositório como pasta publicada. Validar através de HTTP local; o acesso direto por `file://` pode ter comportamento diferente quanto a origens e armazenamento.

## Configuração e variáveis

Não há ficheiro `.env`, variáveis de ambiente consumidas pelo site ou segredos necessários à execução. Contactos, URLs, estilos e traduções estão no [HTML](../index.html). Alterá-los exige editar e publicar os ficheiros.

Não colocar credenciais em ficheiros publicados: o navegador pode descarregá-los. O estado local de língua e consentimento é descrito na [arquitetura](ARCHITECTURE.md).

## Serviços externos

| Serviço | Finalidade | Momento de acesso |
|---|---|---|
| GitHub Pages | Alojamento | Ao visitar o site público |
| Google Fonts | Poppins e Roboto | Na abertura, antes do consentimento |
| Google Maps incorporado | Localização | Após aceitação funcional; carregamento diferido |
| Google Maps por ligação | Abrir localização | Ao seguir a ligação |
| WhatsApp e Facebook | Contacto e rede social | Ao seguir as ligações |
| InterGarage | Conhecer a rede da qual a Stopverde faz parte | Ao seguir a ligação externa |
| Telefone e email | Contacto direto | Ao ativar `tel:` ou `mailto:` |

Não existem chaves de API configuradas no código.

## Alojamento

Endereço registado: https://rickyrito.github.io/stopverdept/. A configuração histórica é branch `main`, raiz. [.nojekyll](../.nojekyll) evita o processamento Jekyll. A configuração remota não foi verificada nesta revisão.

Não existe ficheiro `CNAME` no repositório atual; domínio próprio continua pendente no [inventário](../inventory.md). Ver [Publicação](CONTRIBUTING.md).
