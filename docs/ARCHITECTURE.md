# Arquitetura do sistema

## Visão geral

Site institucional de página única servido como ficheiros estáticos. O [HTML principal](../index.html) inclui CSS num bloco `style` e JavaScript num bloco `script` no final. Não existem backend, base de dados, API própria, autenticação, framework ou dependências de desenvolvimento declaradas.

O navegador obtém a página e os [recursos locais](../assets/). As fontes vêm do Google Fonts na abertura; o mapa Google só recebe o endereço de carregamento após consentimento funcional. As ações de contacto usam ligações para serviços externos ou aplicações do dispositivo.

## Organização da página

| Âncora | Responsabilidade |
|---|---|
| `#inicio` | Apresentação, símbolo e chamadas para contacto |
| `#sobre` | Quem somos e valores |
| `#servicos` | Oito serviços, com ícones e numeração |
| `#precos` | Preçómetro, luzes e preços «Sob consulta» |
| `#parceiros` | Adesão à rede InterGarage, marcas parceiras da rede, seguradoras e parcerias diretas |
| `#contactos` | Contactos, horário e mapa |

Existem ainda faixa de contacto, rodapé, botão WhatsApp, banner e janela de consentimento.

## Interações

- **Ano:** preenche o rodapé com a data do dispositivo.
- **Menu:** sincroniza abertura, ícone e atributos ARIA; fecha ao navegar, clicar fora, premir Escape ou regressar à largura de computador.
- **Animações:** `IntersectionObserver` ativa preçómetro e luzes uma vez, com alternativa sem observador. O CSS trata movimento reduzido.
- **Tradução:** guarda o português do HTML e aplica o objeto `EN` por `data-i18n` e `data-i18n-attr`. Atualiza também língua do documento, título, descrição e rótulos.
- **Consentimento:** gere banner, janela, foco e carregamento/remoção do mapa. Fechar a janela sem escolher não equivale a aceitar.

## Estado no navegador

| Local | Valor | Utilização |
|---|---|---|
| URL `lang` | `pt` ou `en` | Prioridade na escolha inicial |
| `localStorage` `stopverde-lang` | `pt` ou `en` | Escolha pelo botão PT/EN |
| `localStorage` `stopverde-consent` | JSON com `v: 1`, `functional` e `date` | Consentimento e data ISO |

Sem parâmetro ou preferência válidos, usa-se PT se alguma língua do navegador começar por `pt`; caso contrário, EN. O armazenamento está protegido por `try/catch`; a persistência pode falhar quando bloqueada pelo navegador. Não há sincronização entre dispositivos nem prazo de expiração explícito para o consentimento.

As traduções usam `innerHTML`: o dicionário deve conter apenas conteúdo estático controlado pelo projeto, sem entradas não confiáveis.

## Publicação e limites

O procedimento histórico usa GitHub Pages, `main`, raiz, com [.nojekyll](../.nojekyll). Preservar caminhos relativos para o subdiretório público. A configuração remota não foi consultada nesta revisão.

Um único ficheiro simplifica o alojamento, mas exige cuidado com traduções, contactos repetidos e alterações globais. Separar CSS e JavaScript pode ser avaliado se a manutenção o justificar; não é requisito atual. Ver [decisões](REGISTRY.md).
