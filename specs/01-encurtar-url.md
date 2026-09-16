# Encurtar URL

## User Story
Como usuário autenticado, quero encurtar uma URL longa para obter um link curto que eu possa compartilhar.

### Padrão
Como um usuário autenticado
Quero submeter uma URL longa
Para que o sistema gere um link curto único que eu possa compartilhar com outras pessoas

## Critérios de Aceitação (Gherkin)

### Feature: Encurtar URL

#### Scenario: Encurtar URL válida

    Given que o usuário está autenticado e na página de encurtamento
    When o usuário submete uma URL válida
    Then o sistema gera um código curto único
    And exibe o link curto no formato `https://<domínio>/{codigo}`
    And o botão "Salvar" fica ativo permitindo que o usuário salve o registro


#### Scenario: Encurtar URL inválida

    Given que o usuário está autenticado e na página de encurtamento
    When o usuário submete uma entrada que não é uma URL válida
    Then o sistema mostra uma mensagem de validação de URL inválida
    And o botão "Salvar" permanece desativado até que a URL seja corrigida


#### Scenario: Encurtar com campo vazio

    Given que o usuário está autenticado e na página de encurtamento
    When o usuário submete o formulário com o campo de URL vazio
    Then o sistema mostra uma mensagem indicando que o campo URL é obrigatório
    And o botão "Salvar" está desativado e o foco é colocado no campo de URL
