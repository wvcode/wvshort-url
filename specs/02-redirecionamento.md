# Redirecionar para URL real

## User Story

Como qualquer usuário, ao acessar um link curto, quero ser redirecionado para a URL original.

### Padrão

Como um visitante (ou usuário autenticado)
Quando acessar um link curto
Quero ser redirecionado para a URL original correspondente

## Critérios de Aceitação (Gherkin)

### Feature: Redirecionamento de URL curta
  
#### Scenario: Redirecionar código existente
    Given que existe um mapeamento do `{codigo}` para uma URL original
    When qualquer usuário acessa `GET /{codigo}`
    Then o servidor responde com redirecionamento 301 para a URL original
    And a contagem de cliques do registro é incrementada

### Scenario: Código inexistente
    Given que não existe mapeamento para `{codigo}`
    When qualquer usuário acessa `GET /{codigo}`
    Then o servidor responde com 404 Not Found e página/JSON de erro apropriada
