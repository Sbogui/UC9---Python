# A02 — EX02 — Requisitos, regras e aceite
Objetivo: ligar necessidade a evidência observável. Ferramenta: editor e simulação em papel.
Complete três RF, duas RN e um RQ. Os IDs abaixo são espaços de trabalho, não respostas.
Não há código ou aplicação implementada nesta atividade.

## Requisitos
| ID | Descrição verificável | Necessidade atendida | Prioridade e justificativa | Regra vinculada |
|---|---|---|---|---|
| RF01 | O sistema mostra uma lista de equipamentos com código, descrição e quantidade disponível. | Consultar disponibilidade | Alta: sem saber o que há disponível, não dá para emprestar. | RN01 |
| RF02 | O sistema registra a saída de um equipamento a partir do código, da quantidade e do identificador do solicitante, e diminui a quantidade disponível. | Registrar saídas | Alta: é a operação priorizada na DEC02. | RN01, RN02 |
| RF03 | O sistema registra a devolução de um equipamento e aumenta a quantidade disponível. | Registrar devoluções | Média: depende de a saída já existir. | RN02 |
| RQ01 | Rapidez: o atendente/funcionario registra uma saída preenchendo poucos campos no máximo 3 a 4 , sem etapas extras (critério proposto, a confirmar em D03). | "Rápido" do pedido | Média: o pedido cita rapidez, mas sem critério definido. | RN02 |

## Regras do domínio
| ID | Regra proposta | Confirmada ou a confirmar? |
|---|---|---|
| RN01 | Não é permitido registrar saída com quantidade maior que a disponível. | A confirmar (proposta) |
| RN02 | A quantidade informada deve ser um número inteiro maior que zero. | A confirmar (proposta) |

## Critérios e simulações da funcionalidade prioritária (registrar saída)
| ID | RF/RQ | Condição inicial | Ação | Resultado esperado | Tipo de caso |
|---|---|---|---|---|---|
| CA01 | RF02, RQ01 | EQ-001 com 3 disponíveis | Registrar saída de 1 para P-001, preenchendo 3 campos | Mensagem "Empréstimo registrado."; EQ-001 passa a 2 disponíveis | Válido |
| CA02 | RF02, RN01 | EQ-002 com 0 disponíveis | Tentar registrar saída de 1 para P-001 | Mensagem "Quantidade indisponível."; EQ-002 continua com 0 | Inválido |
| CA03 | RF02, RN01 | EQ-003 com 5 disponíveis | Registrar saída de exatamente 5; depois tentar mais 1 | A de 5 é aceita (passa a 0); a de mais 1 é recusada | Limite |

Resultado observado na simulação em papel (não é teste de software): Os três casos seguiram o resultado esperado no "papel".
Ambiguidades descobertas: o que acontece com quantidade vazia ou 0 (RN02 cobre, mas qual mensagem?); a devolução pode ser maior que o emprestado?; o sistema guarda quem está com cada equipamento?
Decisão de correção: propor mensagem "Informe uma quantidade válida." para entrada vazia ou 0; a regra de devolução fica a confirmar com o cliente.

## Esboço de duas telas
- Tela 1 — Disponibilidade: título "Equipamentos"; lista com código, descrição e quantidade disponível; ação "Registrar saída" ao lado de cada item; destino: Tela 2.
- Tela 2 — Registrar saída: campos código (já preenchido), quantidade e identificador do solicitante (todos obrigatórios); ações "Registrar" e "Cancelar"; mensagens "Empréstimo registrado.", "Quantidade indisponível." e "Informe uma quantidade válida."; destino: volta à Tela 1.

## Dados e finalidade
| Campo | Para qual tarefa? | Exemplo sintético | Necessário ou dúvida? |
|---|---|---|---|
| Código | Identificar o equipamento | EQ-001 | Necessário |
| Descrição | Conferir o equipamento (só exibida) | Notebook didatico | Necessário |
| Quantidade | Registrar a saída e atualizar a disponibilidade | 1 | Necessário |
| Identificador do solicitante | Saber quem está com o equipamento | P-001 | Necessário (sem dados pessoais) |