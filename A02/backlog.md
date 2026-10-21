# A02 — EX03 — Organização do trabalho
Ferramentas: editor, IDE, terminal PowerShell e Git local quando disponível.
Use papéis da equipe, não dados pessoais. Alterne autor e revisor durante a aula.

## Backlog e quadro
Estados: A fazer / Em andamento / Em revisão / Concluído.
Prioridade expressa valor/urgência; dependência indica o que precisa existir antes.
| ID | Ação pequena | Requisito | Prioridade | Depende de | Responsável | Revisor | Estado | Evidência de conclusão |
|---|---|---|---|---|---|---|---|---|
| T01 | Definir quais campos a lista de equipamentos mostra (código, descrição, quantidade) | RF01 | Alta | nenhuma | Analista de requisitos | Revisor | A fazer | Tela 1 descrita no requisitos.md com os três campos |
| T02 | Descrever a tela de registrar saída (campos, ações e mensagens) | RF02 | Alta | T01 | Redator de telas | Analista de requisitos | A fazer | Tela 2 descrita, com mensagens de sucesso e de erro |
| T03 | Escrever as regras de validação de quantidade (RN01 e RN02) | RF02 | Alta | T02 | Analista de requisitos | Redator de telas | A fazer | RN01 e RN02 no requisitos.md, com CA01 a CA03 ligados |
| T04 | Descrever o registro de devolução e a regra de quantidade devolvida | RF03 | Média | T02 | Redator de telas | Analista de requisitos | A fazer | Passos da devolução escritos e dúvida sobre devolução maior que o emprestado registrada |
| T05 | Definir como observar "rapidez" (ex.: número de campos para registrar) | RQ01 | Média | marcada "a confirmar" | Analista de requisitos | Revisor | A fazer | RQ01 com critério observável e marcado como proposta |

## Plano de versionamento
- Pasta nova de trabalho e raiz Git (sem expor nome de usuário): UC9---Python
- Ferramenta/versão observada: git version 2.54.0.windows.1
- Arquivos que serão revisados antes do primeiro commit em A04: briefing.md, requisitos.md, backlog.md, evidencias.md
- Arquivos que não devem entrar no histórico: .venv/, __pycache__/, .env, dados-reais/ e qualquer arquivo com dados pessoais
- Como conferir estado e alterações: git status --short
- Quem revisa e qual evidência deve existir: o "revisor" do "papel" confere os arquivos e registra a observação no evidencias.md
- Pendência de instalação/permissão, se houver: nenhuma
- Plano de cópia de segurança autorizado pela instituição (Git local não substitui backup): a confirmar

Concluído: cinco tarefas rastreáveis, papéis, dependências e evidências; estado Git confirmado ou pendência explícita.
Dica: “fazer sistema” é amplo; que pequena entrega outra pessoa consegue verificar?
