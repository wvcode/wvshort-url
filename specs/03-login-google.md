# Login social (Google)

## User Story

Como usuário, quero fazer login com minha conta Google para acessar e gerenciar minhas URLs encurtadas.

### Padrão

Como um usuário
Quero autenticar-me usando minha conta Google
Para que eu possa acessar e gerenciar minhas URLs encurtadas sem criar uma senha adicional

## Critérios de Aceitação (Gherkin)

### Feature: Login via Google
  
#### Scenario: Login bem-sucedido com Google
    Given que o usuário está na página de login
    When o usuário clica em "Entrar com Google" e conclui o fluxo OAuth com sucesso
    Then o usuário é autenticado e redirecionado para o painel
    And uma conta de usuário é criada se ainda não existir

#### Scenario: Falha no login com Google
    Given que o usuário está na página de login
    When o usuário cancela ou o OAuth falha
    Then o sistema mostra uma mensagem de erro informando que a autenticação falhou
