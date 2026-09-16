# Salvar URLs encurtadas

## User Story

Como usuário autenticado, quero salvar e ver minhas URLs encurtadas para gerenciá-las.

### Padrão

Como um usuário autenticado
Quero que cada encurtamento seja persistido associado à minha conta
Para que eu possa consultar, editar ou remover meus links encurtados posteriormente

## Critérios de Aceitação (Gherkin)

### Feature: Salvar URLs encurtadas
  
#### Scenario: Salvar após encurtar
    Given que o usuário autenticado encurtou uma URL com sucesso
    When o encurtamento é finalizado
    Then o registro é salvo associado ao usuário com: URL original, código curto, data de criação e contagem de cliques inicial 0

#### Scenario: Visualizar lista de URLs salvas
    Given que o usuário está autenticado
    When o usuário acessa "Minhas URLs"
    Then o sistema mostra a lista de URLs encurtadas salvas do usuário com metadata (original, curto, criação, cliques)
