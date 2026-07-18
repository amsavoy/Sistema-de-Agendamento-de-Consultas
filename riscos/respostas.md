# Etapa 3 — Definição de Estratégias de Resposta

Estratégias definidas para os riscos de prioridade **Alta** e **Média** identificados na Etapa 2, considerando as quatro respostas clássicas: **evitar**, **mitigar**, **transferir** ou **aceitar**.

## R1 — Falha/instabilidade na integração com prontuário (Alta)

**Estratégia:** Mitigar

**Justificativa:** eliminar totalmente a integração não é viável, pois ela é crítica para o produto; a resposta mais eficaz é reduzir a probabilidade e o impacto da instabilidade.

**Ações associadas:**
- Solicitar formalmente ao fornecedor a documentação atualizada da API e um canal de comunicação sobre mudanças futuras;
- Implementar camada de abstração (adapter) entre o aplicativo e o sistema externo, isolando o impacto de mudanças na API;
- Criar testes automatizados de contrato (contract testing) para detectar rapidamente quebras de integração;
- Definir um ambiente de homologação estável para validar a integração antes de cada release.

## R5 — Atraso por dependência do fornecedor externo (Alta)

**Estratégia:** Mitigar (com elemento de transferência)

**Justificativa:** a dependência em si não pode ser eliminada, mas parte do risco de indisponibilidade pode ser transferida contratualmente ao fornecedor, e o impacto técnico pode ser reduzido internamente.

**Ações associadas:**
- Negociar um SLA formal com o fornecedor, incluindo prazos de resposta a incidentes;
- Mapear um plano de contingência (ex.: fila de sincronização assíncrona) para períodos de indisponibilidade do sistema externo;
- Manter comunicação regular com o fornecedor para antecipar mudanças planejadas.

## R3 — Sobrecarga da equipe / não cumprimento de prazos (Alta)

**Estratégia:** Mitigar

**Justificativa:** o escopo e a criticidade da entrega impedem evitar o trabalho, mas é possível reduzir a probabilidade de atraso ajustando prazos e priorização.

**Ações associadas:**
- Revisar e repriorizar o backlog junto aos stakeholders, distinguindo o que é essencial para a entrega da integração crítica do que pode ser postergado;
- Avaliar reforço temporário da equipe ou redistribuição de tarefas para desafogar os pontos de maior sobrecarga;
- Ajustar o cronograma de forma transparente, comunicando novos prazos realistas em vez de manter uma data inviável.

## R2 — Mudança de requisitos no fluxo de agendamento (Média)

**Estratégia:** Aceitar (com plano de controle)

**Justificativa:** mudanças de requisito vindas de stakeholders fazem parte da natureza do projeto; não é eficiente evitá-las, mas é possível controlar seu impacto.

**Ações associadas:**
- Formalizar um processo leve de gestão de mudanças (registro, avaliação de impacto, aprovação);
- Avaliar cada nova solicitação quanto ao impacto em prazo e esforço antes de incorporá-la;
- Agrupar mudanças menores em ciclos de release definidos, evitando interrupções constantes no fluxo de desenvolvimento.

## R4 — Retrabalho por ausência de testes de regressão (Média)

**Estratégia:** Mitigar

**Justificativa:** o risco decorre diretamente da desproporção entre desenvolvedores e testers; reduzir sua probabilidade é mais viável do que eliminá-lo.

**Ações associadas:**
- Priorizar a criação de testes automatizados nas áreas mais críticas (especialmente na integração externa e no fluxo de agendamento);
- Definir critérios mínimos de teste antes de qualquer entrega, mesmo sob pressão de prazo;
- Avaliar apoio pontual de outro membro da equipe em testes exploratórios em períodos de pico.

## R6 — Desgaste com stakeholders por comunicação tardia (Média)

**Estratégia:** Mitigar

**Justificativa:** o risco é predominantemente processual e pode ser reduzido com uma rotina estruturada de comunicação, sem necessidade de ações técnicas complexas.

**Ações associadas:**
- Instituir atualizações periódicas e estruturadas de status (ex.: quinzenais), como a produzida na Etapa 4;
- Comunicar riscos e tendências assim que identificados, não apenas quando já se tornaram problemas consolidados;
- Envolver os stakeholders nas decisões de priorização, especialmente quando riscos altos exigirem ajuste de escopo ou prazo.
