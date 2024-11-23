# QA-testes
Teste Prático QA Testing BeTalent

# Plano de Testes

## Testes Realizados

| **Funcionalidade Testada** | **Caso de Teste**                                                                                   | **Resultado Esperado**                                                                                         | **Situação do Teste** | **Bug Encontrado**                 | **Evidência**       | **Severidade** | **Sugestão UX/UI**               | **Risco** |
|----------------------------|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------|------------------------------------|---------------------|----------------|------------------------------------|-----------|
| Login                      | **Dado** um usuário padrão<br>**E** acesso a página de login<br>**E** digito meu username `standard_user`<br>**E** digito minha senha `secret_sauce`<br>**Quando** eu clicar em "Login"<br>**Então** devo ser redirecionado para a página inicial | Usuário redirecionado com sucesso à página inicial                                                            | Passou                | Nenhum                             | [Imagem](#)         | Alta           | Exibir mensagens mais claras para falha de login | Baixo     |
| Ordenação e Filtragem      | **Dado** um usuário autenticado<br>**Quando** selecionar o filtro "Name (A to Z)"<br>**Então** os produtos devem ser exibidos em ordem alfabética crescente | Produtos exibidos corretamente em ordem crescente                                                            | Passou                | Nenhum                             | [Imagem](#)         | Média          | Aumentar contraste no botão de ordenação | Baixo     |
| Ordenação e Filtragem      | **Dado** um usuário autenticado<br>**Quando** selecionar o filtro "Price (low to high)"<br>**Então** os produtos devem ser exibidos em ordem de preço crescente | Produtos exibidos corretamente em ordem de preço crescente                                                   | Passou                | Nenhum                             | [Imagem](#)         | Média          | Melhorar visibilidade do filtro | Baixo     |
| Fluxo de Compra            | **Dado** um usuário com itens no carrinho<br>**Quando** finalizar a compra<br>**Então** deve ver uma mensagem confirmando a finalização | Mensagem de confirmação exibida                                                                              | Não passou            | Erro ao salvar informações de envio | [Imagem](#)         | Alta           | Fornecer feedback ao usuário sobre erros de envio | Alto      |
| Remoção de Itens do Carrinho | **Dado** um usuário autenticado<br>**E** com itens no carrinho<br>**Quando** clicar em "Remover"<br>**Então** o item deve ser removido do carrinho | Item removido corretamente do carrinho                                                                       | Passou                | Nenhum                             | [Imagem](#)         | Baixa          | Adicionar mensagem de confirmação visual ao remover item | Baixo     |
| Navegação Entre Páginas    | **Dado** um usuário autenticado<br>**Quando** clicar em "Próxima Página"<br>**Então** deve ser levado à próxima página sem erros | Página carregada corretamente                                                                                | Passou                | Nenhum                             | [Imagem](#)         | Média          | Adicionar animações suaves para transições | Baixo     |
| Logout                     | **Dado** um usuário autenticado<br>**Quando** clicar em "Logout"<br>**Então** deve ser redirecionado para a página de login e a sessão deve ser encerrada | Usuário deslogado e redirecionado para a página inicial                                                       | Passou                | Nenhum                             | [Imagem](#)         | Baixa          | Exibir mensagem de sucesso ao fazer logout | Baixo     |

---

## Lista Consolidada de Bugs

| **ID** | **Descrição do Bug**                                | **Funcionalidade**         | **Passos para Reproduzir**                 | **Impacto** | **Severidade** | **Status** |
|--------|-----------------------------------------------------|----------------------------|--------------------------------------------|-------------|----------------|------------|
| 001    | Erro ao salvar informações de envio durante compra | Fluxo de Compra            | Adicione itens ao carrinho, finalize a compra, insira informações de envio e clique em "Finalizar". | Alto        | Alta           | Aberto     |

---

## Análise de Riscos

| **Risco**                                         | **Impacto** | **Probabilidade** | **Ação de Mitigação**                                               |
|--------------------------------------------------|-------------|--------------------|----------------------------------------------------------------------|
| Falha ao salvar informações de envio             | Alto        | Alta               | Realizar testes automatizados para validação do fluxo completo de compra |
| Erros de UX nas mensagens de erro                | Médio       | Média              | Revisar textos com equipe de design e usabilidade                   |
| Bugs críticos em navegadores específicos         | Alto        | Média              | Realizar testes cross-browser em navegadores mais usados            |

---

## Melhorias UX/UI

- Aumentar contraste em elementos críticos, como botões de filtro.
- Fornecer mensagens claras para falhas (ex.: falha de login ou envio de dados).
- Adicionar animações suaves nas transições de páginas para melhorar a experiência do usuário.

---

Espero que essa estrutura em Markdown atenda ao que você precisa. Caso precise de mais ajustes ou melhorias, é só pedir! 😊
