# Aula 4 — Requisitos do sistema e fontes para elicitação

**Cenário:** venda por telefone ou pessoalmente, com vendedores, administrador e equipe de estoque. As fontes descritas são as que eu procuraria durante a elicitação. Nenhuma entrevista ou consulta foi realizada para escrever este exercício.

## Processo 1 — Registro de pedidos pelos vendedores

### R01 — Identificar o comprador

**Requisito:** O sistema deve permitir que o vendedor associe cada novo pedido a um cliente cadastrado ou registre os dados de contato de um cliente novo.

- **Fonte 1:** Conversa com vendedores que atendem por telefone. **Humana; operacional; classe de usuário: vendedor.**
- **Fonte 2:** Fichas atuais de clientes e pedidos. **Não humana; documentação.**

### R02 — Informar a forma de entrega

**Requisito:** O sistema deve registrar, para cada pedido, se o cliente vai retirar os produtos ou recebê-los no endereço informado.

- **Fonte 1:** Conversa com a equipe que organiza as entregas. **Humana; operacional; classe de usuário: funcionário da expedição.**
- **Fonte 2:** Procedimento de entrega e retirada adotado pela empresa. **Não humana; documentação.**

### R03 — Registrar a escolha de pagamento

**Requisito:** O sistema deve permitir que o vendedor selecione uma forma de pagamento dentre as modalidades autorizadas pela empresa antes de confirmar o pedido.

- **Fonte 1:** Entrevista com quem define as condições de venda. **Humana; tático; classe de usuário: gestor comercial.**
- **Fonte 2:** Política comercial com as formas de pagamento aceitas. **Não humana; documentação.**

## Processo 2 — Cadastro e remoção de produtos pelo administrador

### R04 — Organizar o catálogo

**Requisito:** O sistema deve permitir que o administrador cadastre um produto com código, nome, categoria e preço.

- **Fonte 1:** Entrevista com o administrador que mantém a lista de produtos. **Humana; tático; classe de usuário: administrador.**
- **Fonte 2:** Catálogo atual usado pela equipe comercial. **Não humana; documentação.**

### R05 — Conferir código repetido

**Requisito:** O sistema deve alertar o administrador quando ele tentar cadastrar um produto com um código já utilizado e impedir a duplicação desse código.

- **Fonte 1:** Entrevista com o administrador sobre como identifica produtos parecidos. **Humana; tático; classe de usuário: administrador.**
- **Fonte 2:** Planilha ou relação de códigos já utilizados. **Não humana; documentação.**

### R06 — Retirar produto da venda

**Requisito:** O sistema deve permitir que o administrador desative um produto do catálogo de novas vendas, mantendo sua identificação nos pedidos antigos.

- **Fonte 1:** Entrevista com o administrador sobre produtos que saíram de linha. **Humana; tático; classe de usuário: administrador.**
- **Fonte 2:** Histórico de pedidos e catálogo de produtos antigos. **Não humana; documentação.**

## Processo 3 — Controle das quantidades em estoque

### R07 — Registrar recebimento

**Requisito:** O sistema deve permitir que o estoquista registre a entrada de mercadorias com produto, quantidade recebida e número do documento de recebimento.

- **Fonte 1:** Observação do trabalho de conferência das mercadorias. **Humana; operacional; classe de usuário: estoquista.**
- **Fonte 2:** Documentos e registros de entrada de mercadorias. **Não humana; documentação.**

### R08 — Registrar saída por pedido

**Requisito:** O sistema deve registrar a quantidade de cada produto retirada do estoque para atender a um pedido e vinculá-la ao número desse pedido.

- **Fonte 1:** Entrevista com quem separa os produtos vendidos. **Humana; operacional; classe de usuário: estoquista.**
- **Fonte 2:** Listas atuais de separação de pedidos. **Não humana; documentação.**

### R09 — Avisar sobre quantidade baixa

**Requisito:** O sistema deve indicar ao responsável pelo estoque quais produtos atingiram ou ficaram abaixo do limite mínimo configurado para reposição.

- **Fonte 1:** Entrevista com quem planeja as reposições. **Humana; tático; classe de usuário: responsável pelo estoque.**
- **Fonte 2:** Regras ou planilhas usadas atualmente para definir quantidades mínimas. **Não humana; documentação.**
