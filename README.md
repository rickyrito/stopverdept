# Stopverde — Serviços Auto

Site da **Stopverde, Lda.**, oficina automóvel multimarcas na Pontinha, Odivelas. Apresenta a oficina, serviços, marcas e contactos, em português e inglês.

- Site: https://rickyrito.github.io/stopverdept/
- Repositório: https://github.com/rickyrito/stopverdept
- Site anterior: https://stopverde.webnode.pt/

## Executar localmente

Site estático em HTML, CSS e JavaScript nativo, sem dependências de desenvolvimento nem compilação. Com Python 3 instalado, executar na raiz:

```powershell
python -m http.server 8000 --bind 127.0.0.1
```

Abrir http://127.0.0.1:8000/ e http://127.0.0.1:8000/?lang=en. No Windows, pode usar-se `py` em vez de `python` se o lançador estiver disponível. Terminar com `Ctrl+C`. Ver requisitos e alternativas em [Ambiente](docs/ENVIRONMENT.md).

## Estrutura

| Local | Conteúdo |
|---|---|
| [index.html](index.html) | Página única, estilos e lógica de interação |
| [assets/](assets/) | Símbolo STOP verde, ícones e logótipos |
| [.nojekyll](.nojekyll) | Desativa o processamento Jekyll no GitHub Pages |
| [inventory.md](inventory.md) | Origem dos conteúdos e confirmações pendentes |
| [docs/](docs/) | Documentação técnica e procedimentos |
| [CLAUDE.md](CLAUDE.md) | Contexto e regras para agentes |

## Funcionalidades

- Navegação por secções e menu adaptado a telemóvel.
- Alternância PT/EN com preferência guardada no navegador.
- Apresentação da adesão à rede InterGarage e das suas marcas parceiras.
- Contacto por telefone, email, WhatsApp e Facebook; sem formulários de envio.
- Preçómetro e luzes animadas, com suporte a movimento reduzido.
- Preferências de consentimento; mapa Google apenas após aceitação funcional.

## Publicação e estado

O procedimento histórico usa GitHub Pages, branch `main`, pasta raiz. Um envio para essa branch pode publicar imediatamente. Consultar [Contribuição](docs/CONTRIBUTING.md) e [Testes](docs/TESTING.md).

Continuam pendentes a validação de textos e preços, autorizações dos logótipos, fotografias e eventual domínio próprio. As fontes Google carregam antes do consentimento; alojá-las localmente é uma melhoria identificada. O [inventário](inventory.md) mantém a lista completa.

Esta documentação descreve o código local; não comprova o estado atual do site publicado. Consultar o [índice técnico](docs/README.md) para os restantes guias.
