# QA-testes
Teste Prático QA Testing BeTalent

| **Funcionalidade** | **Contexto**                      | **Cenário**                                                                                                                                      | **Dados utilizados**                          | **Situação do teste** | **Evidência**          | **Severidade** | **Tipo de Teste** | **Ambiente**       | **Prioridade** | **Automatizado?** | **Comportamento inesperado** |
|--------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|-----------------------|------------------------|----------------|--------------------|--------------------|----------------|-------------------|---------------------------|
| Login              | **Dado** um usuário padrão         | **E** acesso a página de login<br>**E** digito meu username (`standard_user`)<br>**E** digito minha senha<br>**Quando** eu clicar em "Login"<br>**Então** devo ser redirecionada para a página inicial | Username: `standard_user`<br>Senha: `secret_sauce` | Passou                | [Link para evidência](#) | Alta           | Funcional         | Homologação        | Crítico        | Sim               | -                         |
| Login              | **Dado** um usuário bloqueado      | **E** acesso a página de login<br>**E** digito meu username (`locked_out_user`)<br>**E** digito minha senha<br>**Quando** eu clicar em "Login"<br>**Então** NÃO devo ser redirecionada para a página inicial<br>**E** deve aparecer uma mensagem dizendo: "Epic sadface: Sorry, this user has been locked out." | Username: `locked_out_user`<br>Senha: `secret_sauce` | Passou                | [Link para evidência](#) | Alta           | Funcional         | Homologação        | Alto           | Sim               | -                         |
| Login              | **Dado** um usuário problemático   | **E** acesso a página de login<br>**E** digito meu username (`problem_user`)<br>**E** digito minha senha<br>**Quando** eu clicar em "Login"<br>**Então** devo ser redirecionada para a página inicial | Username: `problem_user`<br>Senha: `secret_sauce` | Em progresso          | [Link para evidência](#) | Média          | Interface         | Homologação        | Normal         | Não               | Problema visual          |
| Login              | **Dado** um usuário com falha de desempenho | **E** acesso a página de login<br>**E** digito meu username (`performance_glitch_user`)<br>**E** digito minha senha<br>**Quando** eu clicar em "Login"<br>**Então** devo ser redirecionada para a página inicial | Username: `performance_glitch_user`<br>Senha: `secret_sauce` | Não passou           | [Link para evidência](#) | Alta           | Desempenho        | Local               | Alto           | Não               | Lentidão no carregamento |
| Login              | **Dado** um usuário com erro       | **E** acesso a página de login<br>**E** digito meu username (`error_user`)<br>**E** digito minha senha<br>**Quando** eu clicar em "Login"<br>**Então** devo ser redirecionada para a página inicial | Username: `error_user`<br>Senha: `secret_sauce` | Passou                | [Link para evidência](#) | Alta           | Funcional         | Produção           | Crítico        | Sim               | -                         |
| Login              | **Dado** um usuário visual         | **E** acesso a página de login<br>**E** digito meu username (`visual_user`)<br>**E** digito minha senha<br>**Quando** eu clicar em "Login"<br>**Então** devo ser redirecionada para a página inicial | Username: `visual_user`<br>Senha: `secret_sauce` | Passou                | [Link para evidência](#) | Média          | Interface         | Homologação        | Normal         | Não               | Problema de layout        |
| Ordenação e Filtragem de Produtos  | **Dado** que estou na página de produtos | **E** há produtos listados com preços diferentes<br>**Quando** eu selecionar "Preço: Menor para Maior" na opção de ordenação<br>**Então** os produtos devem ser exibidos em ordem crescente de preço |                       |                       |                       |                |                    |                    |                |                   |                           |
| Ordenação e Filtragem de Produtos  | **Dado** que estou na página de produtos | **E** há diferentes categorias de produtos disponíveis<br>**Quando** eu selecionar a categoria "Eletrônicos"<br>**Então** apenas os produtos da categoria "Eletrônicos" devem ser exibidos |                       |                       |                       |                |                    |                    |                |                   |                           |
| Fluxo Completo de Compra           | **Dado** que tenho itens no carrinho   | **E** estou na página do carrinho<br>**Quando** eu clicar em "Checkout"<br>**E** preencher as informações obrigatórias de envio e pagamento<br>**E** confirmar a compra<br>**Então** devo ver uma mensagem de confirmação da compra |                       |                       |                       |                |                    |                    |                |                   |                           |
| Fluxo Completo de Compra           | **Dado** que tenho itens no carrinho   | **E** estou na página do checkout<br>**Quando** eu deixar campos obrigatórios em branco e tentar prosseguir<br>**Então** uma mensagem de erro deve ser exibida, indicando os campos obrigatórios |                       |                       |                       |                |                    |                    |                |                   |                           |
| Remoção de Itens do Carrinho       | **Dado** que tenho mais de um item no carrinho | **Quando** eu clicar no botão "Remover" ao lado de um item específico<br>**Então** esse item deve ser removido do carrinho |                       |                       |                       |                |                    |                    |                |                   |                           |
| Remoção de Itens do Carrinho       | **Dado** que tenho vários itens no carrinho | **Quando** eu clicar no botão "Remover Todos"<br>**Então** o carrinho deve ser esvaziado, e uma mensagem "Seu carrinho está vazio" deve ser exibida |                       |                       |                       |                |                    |                    |                |                   |                           |
| Navegação entre Páginas            | **Dado** que estou na página inicial   | **Quando** eu clicar no link "Produtos"<br>**Então** devo ser redirecionada para a página de produtos |                       |                       |                       |                |                    |                    |                |                   |                           |
| Navegação entre Páginas            | **Dado** que estou na página de produtos | **Quando** eu clicar no ícone do carrinho no topo da página<br>**Então** devo ser redirecionada para a página do carrinho |                       |                       |                       |                |                    |                    |                |                   |                           |
| Logout                             | **Dado** que estou autenticada no sistema | **Quando** eu clicar no botão "Logout"<br>**Então** devo ser redirecionada para a página de login<br>**E** minha sessão deve ser encerrada |                       |                       |                       |                |                    |                    |                |                   |                           |
| Logout                             | **Dado** que não estou autenticada     | **Quando** eu tentar acessar a funcionalidade de logout diretamente pela URL<br>**Então** devo ser redirecionada para a página de login |                       |                       |                       |                |                    |                    |                |                   |                           |
