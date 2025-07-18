# Copilot Instructions for AI Agents

## Visão Geral do Projeto
- Este projeto é uma landing page de hotéis desenvolvida com HTML5, CSS3 e Bootstrap 5.
- O foco é responsividade, layout visual moderno e integração dinâmica de dados de estados/cidades do Brasil via API do IBGE.
- Não há backend próprio: o formulário envia dados para um arquivo PHP (`processador.php`), mas o processamento não está incluso neste repositório.

## Estrutura de Pastas
- `index.html`: página principal, contém todo o HTML, scripts e pontos de integração.
- `css/`: estilos customizados (pode estar vazio ou ser usado para overrides do Bootstrap).
- `img/`: imagens usadas no carrossel e seções visuais.
- `js/`: scripts customizados (atualmente, scripts estão embutidos no HTML).

## Padrões e Convenções
- Use Bootstrap 5 para todos os componentes visuais e grid.
- Scripts JavaScript devem ser adicionados ao final do `index.html` (antes do fechamento do `</body>`).
- Para selects de estados/cidades, utilize a API pública do IBGE:
  - Estados: `https://servicodados.ibge.gov.br/api/v1/localidades/estados`
  - Cidades: `https://servicodados.ibge.gov.br/api/v1/localidades/estados/{UF}/municipios`
- O select de cidades é populado dinamicamente ao selecionar um estado.
- O formulário de cadastro deve conter campos de nome, email, gênero, estado e cidade.
- Utilize `value=""` no primeiro `<option>` de selects para garantir validação adequada.

## Fluxo de Desenvolvimento
- Não há build system, testes automatizados ou dependências além do Bootstrap CDN.
- Para desenvolvimento, basta abrir o `index.html` em um navegador.
- Imagens devem ser adicionadas à pasta `img/` e referenciadas via caminho relativo.
- Scripts externos devem ser adicionados via CDN.

## Exemplos de Integração
- Para adicionar um novo campo ao formulário, siga o padrão dos campos existentes.
- Para customizar estilos, adicione regras em `css/` e referencie no HTML.
- Para alterar o carrossel, edite o bloco `<div id="carouselExampleControls" ...>`.

## Observações
- Não inclua lógicas de backend ou frameworks JS avançados.
- Mantenha o código limpo, comentado e com identação consistente.
- O projeto é didático e serve como base para estudos de front-end responsivo.

---
Seções ou padrões não documentados? Adicione exemplos claros neste arquivo para facilitar a colaboração de agentes de IA.
