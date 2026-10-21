# A02 — EX01 — Briefing da equipe
Use dados inventados. Preencha os campos; não trate lacunas como decisões.
Ferramenta: editor de texto/Markdown. Não há programa para executar.

## Pedido recebido
Precisamos controlar empréstimos de equipamentos, consultar disponibilidade e registrar saídas e devoluções. O cliente pediu rapidez e segurança, ainda sem critérios definidos.

## Problema e resultado desejado
- Problema observado no cenário: não há controle claro de quais equipamentos estão disponíveis, quem está com eles e quando voltam.
- Quem utilizará (papel, não nome real): atendente da "loja" (a confirmar).
- Resultado desejado: consultar a disponibilidade e registrar saídas e devoluções de equipamentos de forma rápida e segura.
- Dentro do escopo inicial:
    consultar disponibilidade de equipamentos (código, descrição, quantidade);
    registrar saída (empréstimo);
    registrar devolução.
- Fora do escopo inicial:
    compra e manutenção de equipamentos;
    cobrança, multas ou notificações;
    banco de dados e dados pessoais além de um identificador do solicitante.

## Perguntas ao cliente
| ID | Pergunta | Impacto da resposta | Resposta ou "a confirmar" |
|---|---|---|---|
| D01 | Quem ira pegar o equipamento emprestado e quem fara o registro? | Define os usuários do sistema e se é preciso identificar o solicitante | a confirmar |
| D02 | Qual o prazo do empréstimo e o que acontece se atrasar? | Define a regra de devolução e se haverá alerta | a confirmar |
| D03 | O que você entende por "rápido" e "seguro"? | Define requisitos de qualidade que dá para observar (tempo de registro, quem acessa) | a confirmar |

## Decisões
| ID | Decisão/hipótese | Estado (proposta/confirmada) | Evidência da confirmação |
|---|---|---|---|
| DEC01 | Identificar o solicitante só por um código (ex: P-001), sem dados pessoais | proposta | confirmar qual meios de contato é realmente necessário |
| DEC02 | Priorizar o registro de saída antes da devolução | proposta | confirmar qual operação é mais urgente |

## Revisão
O revisor consegue separar pedido, hipótese e decisão? Registre observação e melhoria.
Concluído quando problema, escopo, três dúvidas e decisões pendentes estão claros.
Dica: pergunte qual informação mudaria o comportamento do futuro aplicativo.
