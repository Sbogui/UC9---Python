# A02 — EX04 — Evidências e revisão
Dados exclusivamente sintéticos. Não incluir credenciais, dados pessoais nem caminhos com nome de usuário.

## Entrega
- Briefing: `briefing.md` preenchido com pedido recebido, problema, papel do usuário (atendente da "loja", a confirmar), escopo (dentro/fora), três dúvidas ao cliente (D01 a D03) e duas decisões propostas (DEC01 e DEC02).
- Requisitos, regras e critérios: `requisitos.md` com três requisitos funcionais (RF01 a RF03: consultar disponibilidade, registrar saída e registrar devolução), um requisito de qualidade (RQ01, rapidez), duas regras propostas (RN01 e RN02) e três critérios de aceite (CA01 válido, CA02 inválido, CA03 fronteira).
- Esboços de telas: Tela 1 (lista de equipamentos) e Tela 2 (registrar saída), descritas em texto no `requisitos.md`.
- Backlog e plano de versionamento: `backlog.md` com cinco tarefas (T01 a T05), cada uma ligada a um requisito, com prioridade, dependência, papel responsável, revisor e evidência de conclusão.

## Ferramentas
- IDE e pasta de trabalho conferidas: VS Code, com a pasta `UC9---Python` aberta e os documentos organizados em `A01` e `A02`.
- Versão de Git observada: git version 2.54.0.windows.1
- Comando executado e resultado (remover caminhos pessoais):
  - `git add .` e `git commit`: commits criados com sucesso. Os avisos de `LF will be replaced by CRLF` são normais no Windows e não impediram nada.
  - `git push`: primeiro falhou por falta de branch upstream; depois foi recusado pelo GitHub (erro GH007, e-mail privado) e resolvido ao configurar o e-mail noreply do GitHub com `git config --global user.email`.
  - M A02/backlog.md | origin  https://github.com/Sbogui/UC9---Python.git (fetch) | origin  https://github.com/Sbogui/UC9---Python.git (push)
- Raiz Git conferida: C:/Users/-/OneDrive/Desktop/ProjetosVSCode/UC9---Python
- Instalação pendente ou sucesso confirmado: Git instalado e funcionando; commit e push executados com sucesso.

### Registro de transparência sobre o uso do Git
O enunciado da Atividade 3 e o `guia-ferramentas.md` orientam que, nesta aula, não se executem push nem configuração global e que o primeiro commit revisado fica para a A04. A dupla já realizou commit, push para o repositório remoto e `git config --global user.email`, antes dessa etapa. Isso é registrado aqui para que o professor tenha conhecimento. O push foi feito para um repositório pessoal de estudo, e os arquivos enviados contêm somente dados sintéticos (EQ-001, P-001 e semelhantes), sem dados pessoais, credenciais ou arquivos internos. O motivo foi organizar os trabalhos da UC9 em um único repositório. Se o professor preferir, a dupla pode manter os arquivos só localmente nas próximas aulas e seguir a revisão do primeiro commit na A04.

## Simulação em papel
- Critério: CA01 (RF02 e RQ01), saída válida.
- Entrada: equipamento EQ-001 com 3 unidades disponíveis; solicitante P-001; quantidade 1.
- Ação: registrar a saída preenchendo os três campos (código, quantidade e identificador do solicitante).
- Resultado esperado: mensagem "Empréstimo registrado." e EQ-001 passa a 2 disponíveis.
- Resultado da simulação: no papel, o resultado seguiu o esperado. Isso não é teste de software aprovado, pois não há código executável.
- Dúvida encontrada: o que acontece com quantidade vazia ou 0? A RN02 cobre o caso, mas faltava definir a mensagem; propôs-se "Informe uma quantidade válida.". Também ficou a dúvida se a devolução pode ser maior que o emprestado.

## Revisão por pares
- Trecho antes: "D01: Quem ira pegar o equipamento emprestado e quem fara o registro?"
- Sugestão com justificativa: acentuar "irá" e "fará", e na DEC01 trocar "qual meios de contato" por "quais meios de contato". Justificativa: erros de escrita podem confundir quem lê o briefing e atrapalham o entendimento da pergunta.
- Decisão do autor: aceitar a sugestão.
- Trecho depois: "D01: Quem irá pegar o equipamento emprestado e quem fará o registro?"
- Observação: 

## Auditoria
Para cada situação: texto/ID, escolha, justificativa e evidência que investigaria.
O azul indica registro, não acerto. A correção ocorre depois com o professor.

## Reflexão individual
- O que consigo explicar: 
- Em que preciso de apoio: 
- Próximo passo para A03 (raciocínio no papel; ambiente virtual e primeiro commit em A04): 