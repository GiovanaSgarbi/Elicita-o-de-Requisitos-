# Aula 3 — Requisitos não funcionais

O contexto é um aplicativo de delivery. Os nove requisitos abaixo usam características do modelo de qualidade da **ISO/IEC 25010:2023**. Os valores de tempo e disponibilidade são metas definidas para este exercício.

## História 1 — Cliente avalia um pedido entregue

| Código | Requisito não funcional | Característica |
| --- | --- | --- |
| RNF-01 | O formulário de avaliação deve manter texto, botões e campo de nota legíveis em telas de celular com largura a partir de 320 pixels, sem rolagem horizontal. | Capacidade de interação |
| RNF-02 | Ao receber uma avaliação com comentário, o sistema deve tratar o texto informado pelo cliente de forma a impedir a execução de scripts na página do restaurante. | Segurança |
| RNF-03 | Em condições normais de rede, 95% dos envios de avaliações devem receber confirmação ou mensagem de erro em até 3 segundos. | Eficiência de desempenho |

## História 2 — Cliente salva um cartão

| Código | Requisito não funcional | Característica |
| --- | --- | --- |
| RNF-04 | Os dados transmitidos entre o aplicativo e o serviço de pagamento devem trafegar por uma conexão criptografada. | Segurança |
| RNF-05 | Se uma tentativa de cadastro for repetida por falha de conexão, o sistema deve evitar que o mesmo cartão apareça duas vezes na lista da conta. | Confiabilidade |
| RNF-06 | A lista de cartões salvos deve ser exibida em até 2 segundos em pelo menos 95% das consultas com até dez cartões por conta. | Eficiência de desempenho |

## História 3 — Restaurante vê o resumo de vendas

| Código | Requisito não funcional | Característica |
| --- | --- | --- |
| RNF-07 | Os valores monetários do resumo devem usar a moeda brasileira e apresentar claramente o período a que os números se referem. | Capacidade de interação |
| RNF-08 | Após o encerramento do dia, as informações do resumo devem permanecer disponíveis em pelo menos 99,5% das consultas mensais, exceto durante manutenção programada. | Confiabilidade |
| RNF-09 | Após 15 minutos sem atividade, o painel deve encerrar a sessão e solicitar nova autenticação antes de voltar a mostrar os dados financeiros. | Segurança |

**Referência:** [ISO/IEC 25010:2023 — modelo de qualidade do produto](https://www.iso.org/standard/78176.html).
