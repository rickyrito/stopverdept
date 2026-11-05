# Contexto e regras do projeto

Site estático da Stopverde, Lda., oficina multimarcas na Pontinha, Odivelas. Antes de alterar código, consultar o [índice técnico](docs/README.md) e o [inventário](inventory.md).

## Estrutura e execução

- [index.html](index.html) contém HTML, CSS e JavaScript nativo. Não existe framework, compilação, gestor de pacotes ou backend.
- [assets/](assets/) contém recursos locais. Preservar caminhos relativos para a publicação em `/stopverdept/`.
- Servir localmente com `python -m http.server 8000 --bind 127.0.0.1` se Python 3 estiver instalado. Ver [Ambiente](docs/ENVIRONMENT.md).
- A publicação documentada é GitHub Pages, `main`, raiz. Não fazer push como parte de uma simples edição local.

## Conteúdo e identidade

- Escrever em português de Portugal e fornecer inglês para todo o texto novo.
- Não inventar preços, garantias, anos de experiência, horários ou relações comerciais. Consultar o [inventário](inventory.md); onde faltam preços, manter «Sob consulta».
- «Quem Somos» comunica continuidade e confiança («A sua oficina de sempre»). Não mencionar a fusão Pontelectro/Garepol.
- Preservar o sinal STOP **verde**, borda e letras brancas. Não reintroduzir vermelho na marca. Manter `textLength` no [símbolo SVG](assets/stopverde.svg).
- Manter o ícone WhatsApp com volante e o espaço no rodapé para o botão flutuante.
- Não acrescentar logótipos sem autorização confirmada. As autorizações dos existentes continuam pendentes no inventário.
- Sincronizar contactos em todas as ocorrências: barra superior, faixas, contactos e rodapé. WhatsApp: `https://wa.me/351960219587`.

## Comportamento a preservar

- Português no HTML; inglês no objeto `EN`, por `data-i18n` e `data-i18n-attr`. Traduzir também rótulos acessíveis e metadados.
- Língua inicial: parâmetro `?lang=` válido → `stopverde-lang` → línguas do navegador (PT se alguma for portuguesa; EN caso contrário).
- Consentimento em `stopverde-consent`; mapa em `iframe[data-src]`, sem carregar antes da aceitação funcional. Novos conteúdos externos opcionais devem respeitar a escolha correspondente.
- As fontes Google carregam antes do consentimento: limitação conhecida, não assumir bloqueio integral de terceiros.
- Preservar teclado, retorno de foco das preferências e `prefers-reduced-motion`.
- Sem formulários de envio: usar `tel:`, `mailto:` ou WhatsApp, salvo alteração explícita da arquitetura.

## Documentação e validação

Consultar [Arquitetura](docs/ARCHITECTURE.md), [Desenho](docs/DESENHO.md), [Contribuição](docs/CONTRIBUTING.md), [Testes](docs/TESTING.md) e [Segurança](docs/SECURITY.md). Atualizar a documentação quando o comportamento mudar e registar decisões relevantes no [registo](docs/REGISTRY.md).

Antes de publicar, verificar PT/EN, larguras de 320 a 1280 px, teclado, consentimento e ligações. Não declarar verificações executadas sem as realizar.
