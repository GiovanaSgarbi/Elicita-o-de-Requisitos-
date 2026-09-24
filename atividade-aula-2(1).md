# Aula 2 — Histórias de usuário e priorização MoSCoW

**Sistema:** aplicativo de delivery de comida.

## História 1 — Linha do tempo do pedido

**Como** cliente que fez uma compra, **quero** ver as etapas já concluídas e a etapa atual do meu pedido, **para** entender o que aconteceu depois da confirmação.

**Critérios de aceitação**

1. **Dado** que um pedido foi confirmado, **quando** acesso a tela de acompanhamento, **então** vejo a etapa “pedido recebido” com a hora em que ela ocorreu.
2. **Dado** que o restaurante iniciou o preparo, **quando** abro a linha do tempo do pedido, **então** vejo “em preparo” como etapa atual e “pedido recebido” como etapa anterior.
3. **Dado** que a entrega foi concluída, **quando** consulto o histórico desse pedido, **então** vejo as etapas anteriores e a etapa final “entregue”, cada uma com seu horário.

## História 2 — Pausar um produto do cardápio

**Como** responsável pelo restaurante, **quero** pausar a venda de um produto que acabou, **para** não receber novos pedidos desse produto enquanto ele estiver em falta.

**Critérios de aceitação**

1. **Dado** que estou no painel do restaurante, **quando** pauso um produto ativo, **então** sua situação muda para “indisponível” no meu painel e no cardápio visto pelos clientes.
2. **Dado** que o produto está indisponível, **quando** um cliente tenta finalizar um carrinho que ainda contém esse produto, **então** o aplicativo informa a falta e solicita que ele retire o produto antes de confirmar o pedido.
3. **Dado** que o produto voltou a estar disponível, **quando** retiro a pausa no painel, **então** ele volta a poder ser incluído em novos pedidos.

## História 3 — Ocorrência durante a entrega

**Como** entregador responsável por um pedido, **quero** informar um imprevisto e anexar uma foto, **para** dar contexto à equipe de suporte sem precisar explicar tudo novamente.

**Critérios de aceitação**

1. **Dado** que estou com uma entrega ativa, **quando** seleciono “Informar imprevisto”, **então** posso escolher o motivo, escrever uma observação e anexar uma foto.
2. **Dado** que preenchi o motivo e a observação, **quando** envio o formulário, **então** recebo um número de protocolo vinculado ao pedido.
3. **Dado** que registrei um imprevisto, **quando** abro novamente os detalhes da entrega, **então** consigo consultar o protocolo e o estado do atendimento.

## Ordem pelo MoSCoW

| Prioridade | História | Razão |
| --- | --- | --- |
| **Must have** | Pausar um produto do cardápio | É preciso bloquear a compra de itens que o restaurante não consegue fornecer. |
| **Should have** | Linha do tempo do pedido | O cliente consegue acompanhar a compra sem depender de mensagens ou ligações, mas o fluxo de venda pode funcionar antes dessa melhoria. |
| **Could have** | Ocorrência durante a entrega | O registro no aplicativo ajuda o suporte; numa primeira versão, o entregador pode usar um canal de atendimento já disponível. |

Cada história trata de uma necessidade específica e possui situações observáveis para verificar se foi atendida.
