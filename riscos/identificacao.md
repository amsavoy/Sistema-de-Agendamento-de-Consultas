# Etapa 1 — Identificação de Riscos

## Contexto do projeto

Projeto de desenvolvimento de um aplicativo móvel para agendamento de consultas médicas, em fase intermediária, com funcionalidades de cadastro de usuários, gestão de agenda médica, agendamento de consultas, notificações e integração com um sistema externo de prontuário. Equipe composta por 4 desenvolvedores e 1 tester. A integração externa é crítica para a entrega.

A identificação a seguir foi apoiada por uma IA Generativa (LLM), a partir do cenário descrito, e revisada para refletir os desafios já relatados (instabilidade na integração externa, mudanças de requisitos e sobrecarga da equipe), além de riscos correlatos que costumam se manifestar no mesmo tipo de contexto.

## Lista de Riscos Identificados

| ID | Risco | Categoria |
|----|-------|-----------|
| R1 | Falha ou instabilidade na integração com o sistema externo de prontuário | Técnico / Integração |
| R2 | Mudança de requisitos no fluxo de agendamento durante o desenvolvimento | Escopo |
| R3 | Sobrecarga da equipe de desenvolvimento e não cumprimento de prazos | Recursos / Cronograma |
| R4 | Retrabalho por ausência de testes de regressão sob pressão de prazo | Qualidade |
| R5 | Atraso na entrega por dependência de um fornecedor externo (sistema de prontuário) | Fornecedor / Terceiros |
| R6 | Desgaste na relação com stakeholders por comunicação tardia ou incompleta sobre problemas | Comunicação / Stakeholders |

## Descrição e Contexto de Cada Risco

**R1 — Falha ou instabilidade na integração com o sistema externo de prontuário**
Descrição: a API do sistema externo carece de documentação clara e sofreu mudanças recentes, o que já causou instabilidade nas chamadas de integração.
Contexto em que pode ocorrer: durante o desenvolvimento e testes dos módulos que dependem da troca de dados com o prontuário — por exemplo, ao sincronizar um agendamento recém-criado ou ao consultar o histórico do paciente.

**R2 — Mudança de requisitos no fluxo de agendamento**
Descrição: stakeholders solicitaram novas validações e regras de negócio para o fluxo de agendamento já em desenvolvimento.
Contexto em que pode ocorrer: em qualquer momento em que o fluxo de agendamento já implementado precise ser revisitado para acomodar uma regra que não estava no escopo original, gerando retrabalho em código e testes.

**R3 — Sobrecarga da equipe de desenvolvimento**
Descrição: a equipe (4 desenvolvedores e 1 tester) relatou aumento de carga de trabalho, colocando em risco o cumprimento dos prazos estimados inicialmente.
Contexto em que pode ocorrer: quando a soma das demandas de correção da integração externa, adequação a novos requisitos e desenvolvimento das funcionalidades pendentes ultrapassa a capacidade da equipe no período restante do cronograma.

**R4 — Retrabalho por ausência de testes de regressão sob pressão de prazo**
Descrição: com apenas 1 tester para 4 desenvolvedores e prazos apertados, há risco de cobertura de testes insuficiente ao acomodar mudanças de requisitos e correções na integração.
Contexto em que pode ocorrer: em ciclos de entrega acelerados, especialmente após alterações no fluxo de agendamento ou ajustes na integração externa, quando a validação completa é sacrificada para ganhar tempo.

**R5 — Atraso na entrega por dependência de fornecedor externo**
Descrição: como a integração com o prontuário é crítica e depende de um sistema fora do controle da equipe, mudanças ou indisponibilidades do lado do fornecedor impactam diretamente o cronograma do projeto.
Contexto em que pode ocorrer: sempre que o fornecedor externo alterar sua API, tiver instabilidade em produção, ou não fornecer suporte/documentação em tempo hábil para a equipe se adaptar.

**R6 — Desgaste na relação com stakeholders por comunicação tardia**
Descrição: se os problemas técnicos e de cronograma não forem comunicados de forma clara e proativa, os stakeholders podem perder confiança na condução do projeto.
Contexto em que pode ocorrer: quando atrasos, mudanças de escopo ou instabilidades técnicas se acumulam sem um canal estruturado de atualização, levando a surpresas negativas em vez de decisões conjuntas e informadas.
