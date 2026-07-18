# Etapa 2 — Análise dos Riscos

## Metodologia

A análise qualitativa foi conduzida avaliando cada risco em duas dimensões — **probabilidade** de ocorrência e **impacto** no projeto — em escala de 1 (baixo) a 5 (alto). O produto das duas dimensões gera um **score de exposição ao risco**, usado para priorização:

- Score 1–6: prioridade **Baixa**
- Score 7–14: prioridade **Média**
- Score 15–25: prioridade **Alta**

## Matriz de Probabilidade x Impacto

| ID | Risco | Probabilidade (1-5) | Impacto (1-5) | Score | Prioridade |
|----|-------|:---:|:---:|:---:|:---:|
| R1 | Falha/instabilidade na integração com prontuário | 5 | 5 | 25 | Alta |
| R5 | Atraso por dependência do fornecedor externo | 4 | 5 | 20 | Alta |
| R3 | Sobrecarga da equipe / não cumprimento de prazos | 4 | 4 | 16 | Alta |
| R2 | Mudança de requisitos no fluxo de agendamento | 4 | 3 | 12 | Média |
| R4 | Retrabalho por ausência de testes de regressão | 3 | 4 | 12 | Média |
| R6 | Desgaste com stakeholders por comunicação tardia | 3 | 3 | 9 | Média |

## Análise Estruturada, Impactos e Fatores Condicionantes

**R1 — Falha/instabilidade na integração com prontuário (Score 25 — Alta)**
Impacto: compromete diretamente uma funcionalidade crítica do sistema; pode gerar dados inconsistentes entre o aplicativo e o prontuário do paciente, além de atrasar a entrega geral do projeto.
Fatores condicionantes: ausência de documentação de API atualizada; mudanças unilaterais do fornecedor sem aviso prévio; falta de ambiente de testes estável para a integração.

**R5 — Atraso por dependência do fornecedor externo (Score 20 — Alta)**
Impacto: qualquer indisponibilidade ou mudança não planejada do lado do fornecedor bloqueia o avanço da equipe, já que a integração é crítica para a entrega.
Fatores condicionantes: baixo nível de controle e visibilidade sobre o roadmap do fornecedor; ausência de acordo de nível de serviço (SLA) formal ou canal direto de suporte técnico.

**R3 — Sobrecarga da equipe / não cumprimento de prazos (Score 16 — Alta)**
Impacto: risco de queda na qualidade das entregas, atrasos em cascata em outras funcionalidades e possível desgaste da equipe.
Fatores condicionantes: acúmulo simultâneo de correções na integração, adequação a novos requisitos e desenvolvimento de funcionalidades pendentes, sem realocação de recursos ou revisão de prazos.

**R2 — Mudança de requisitos no fluxo de agendamento (Score 12 — Média)**
Impacto: retrabalho em código já implementado, possível necessidade de revalidar regras de negócio e testes associados.
Fatores condicionantes: processo de gestão de mudanças pouco formalizado; requisitos de negócio ainda amadurecendo junto aos stakeholders durante o desenvolvimento.

**R4 — Retrabalho por ausência de testes de regressão (Score 12 — Média)**
Impacto: bugs podem chegar a produção, gerando retrabalho e possível perda de confiança dos usuários finais e stakeholders.
Fatores condicionantes: proporção de 1 tester para 4 desenvolvedores; pressão de prazo reduzindo o tempo dedicado a testes completos após mudanças.

**R6 — Desgaste com stakeholders por comunicação tardia (Score 9 — Média)**
Impacto: perda de confiança na condução do projeto, decisões tomadas sem informação adequada, maior resistência a negociações futuras de prazo ou escopo.
Fatores condicionantes: ausência de um ritual formal de comunicação de status; tendência a só comunicar problemas quando já estão consolidados, em vez de sinalizar tendências cedo.

## Observação Metodológica

Os valores de probabilidade e impacto foram atribuídos com base nas evidências descritas no cenário (instabilidade já relatada, criticidade explícita da integração, relato direto de sobrecarga da equipe) e em julgamento qualitativo típico de projetos de software com características semelhantes. Em um contexto real, esses valores devem ser revisados periodicamente com a equipe e ajustados conforme novas evidências surgirem.
