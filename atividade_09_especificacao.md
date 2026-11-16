# Especificação de Caso de Uso — Solicitar Empréstimo

## 1. Identificação
- **Sistema:** Sistema de Empréstimo de Livros
- **Caso de uso:** Solicitar empréstimo
- **Ator principal:** Leitor
- **Ator participante:** Bibliotecário
- **Ator secundário:** Sistema de Notificações

## 2. Descrição
Permite que o leitor solicite o empréstimo de um livro disponível no catálogo. O bibliotecário confere o cadastro do leitor e a disponibilidade do exemplar. Após o registro, o sistema envia uma confirmação ao leitor por meio do Sistema de Notificações.

## 3. Gatilho
O leitor escolhe um livro no catálogo e solicita seu empréstimo.

## 4. Pré-condições
1. O leitor deve possuir cadastro ativo na biblioteca.
2. O livro deve estar cadastrado no sistema.
3. O leitor não pode estar impedido de realizar empréstimos.

## 5. Pós-condições
- **Sucesso:** empréstimo registrado, exemplar marcado como emprestado e confirmação enviada ao leitor.
- **Falha:** empréstimo não é registrado e a disponibilidade do exemplar permanece inalterada.

## 6. Fluxo principal
1. O leitor acessa o catálogo de livros.
2. O leitor seleciona o livro desejado.
3. O leitor solicita o empréstimo.
4. O sistema verifica o cadastro e a situação do leitor.
5. O sistema verifica se o exemplar está disponível.
6. O bibliotecário confirma a solicitação.
7. O sistema registra o empréstimo e atualiza a situação do exemplar.
8. O sistema aciona o Sistema de Notificações.
9. O leitor recebe a confirmação do empréstimo.
10. O caso de uso é encerrado.

## 7. Fluxo alternativo — Livro indisponível
- **Quando:** no passo 5 do fluxo principal, o exemplar não está disponível.
- **Passos:**
  1. O sistema identifica que o livro está emprestado ou indisponível.
  2. O sistema informa a indisponibilidade ao leitor.
  3. O leitor pode escolher outro livro ou desistir.
- **Retorno:** se escolher outro livro, o fluxo retorna ao passo 2; se desistir, o caso de uso é encerrado sem empréstimo.

## 8. Exceção — Leitor com cadastro irregular
- **Quando:** no passo 4 do fluxo principal, o sistema identifica cadastro inativo ou bloqueio por pendência.
- **Passos:**
  1. O sistema interrompe a solicitação.
  2. O sistema informa ao bibliotecário o motivo do impedimento.
  3. O bibliotecário orienta o leitor a regularizar a situação.
- **Retorno:** após a regularização, o leitor pode iniciar novamente a solicitação a partir do passo 1. Se não houver regularização, o caso de uso termina sem empréstimo.

## 9. Atores do sistema
| Ator | Descrição |
|---|---|
| Leitor | Consulta o catálogo e solicita empréstimos. |
| Bibliotecário | Confere o cadastro, valida a solicitação e registra devoluções. |
| Sistema de Notificações | Envia ao leitor a confirmação do empréstimo ou da devolução. |

## 10. Outros casos de uso do diagrama
- **Consultar catálogo:** permite ao leitor pesquisar livros disponíveis.
- **Registrar devolução:** permite ao bibliotecário registrar a devolução de um livro.
- **Enviar confirmação:** serviço realizado pelo Sistema de Notificações após uma operação concluída.
