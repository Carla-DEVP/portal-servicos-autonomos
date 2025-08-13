# Documento Stage-Gate — Portal de Serviços Autônomos — ENTEC 2025.1

## Metadados
- **Projeto:** Portal de Serviços Autônomos — ENTEC 2025.1  
- **Versão:** 1.0  
- **Data:** 13/08/2025  
- **Elaboração:** Carla de Medeiros — Project Manager (PM)  
- **Patrocinador:** Prof. Renato Atouguia — Diretor do Projeto  

---

## 1. Objetivo do Documento
Estabelecer o processo Stage-Gate a ser adotado pelo projeto, definindo fases (stages), pontos de decisão (gates), papéis, artefatos obrigatórios, critérios de aprovação e fluxo de governança.  
Este documento também reconhece retroativamente marcos já atingidos (MVP e aprovações) para manter a rastreabilidade.

---

## 2. Princípios de Governança
- **Foco em MVP e incrementos:** evolução por ciclos curtos com entregáveis verificáveis.  
- **Decisão baseada em evidências:** gates avaliam artefatos, indicadores e riscos.  
- **Integração end-to-end:** Front-end, Back-end e Banco de Dados avançam de forma coordenada.  
- **Transparência:** uso de GitHub (Issues/Projects) para status, decisões e documentação em `/docs`.  
- **Simplicidade operacional:** decisões técnicas priorizam manutenção e desempenho (ex.: arquivos em sistema de arquivos; banco guarda apenas referência/URL).

---

## 3. Papéis e Responsabilidades

| Papel                     | Responsável          | Responsabilidades no Stage-Gate |
|----------------------------|--------------------|--------------------------------|
| Sponsor / Gatekeeper Líder | Prof. Renato Atouguia | Conduz decisão nos Gates; aprova escopo e mudanças relevantes |
| Project Manager (PM)       | Carla de Medeiros   | Planeja o ciclo, agenda Gate Reviews, garante artefatos e integração |
| Front-end                  | André Caíque        | Protótipos, UI responsiva, busca/filtros, ranking/mosaico/patrocinados |
| Back-end                   | Felipe Delfino      | APIs REST, autenticação, integração com BD e armazenamento de arquivos |
| Banco de Dados             | Monyelly Salvino    | MER, chaves/relacionamentos, desempenho/consistência |
| Equipe (coletivo)          | Todos               | Evidências para gates, testes integrados, mitigação de riscos |

**Gatekeepers:** Sponsor + PM (obrigatórios); especialistas técnicos participam conforme o Gate.

---

## 4. Macroprocesso Stage-Gate do Projeto

**Visão Geral dos Stages:**
1. Stage 0 — Iniciação & Ideação (retroativo)  
2. Stage 1 — Planejamento Detalhado (retroativo)  
3. Stage 2 — Desenvolvimento do MVP (retroativo)  
4. Stage 3 — Extensões do MVP (em curso)  
5. Stage 4 — Estabilização, Testes & Preparação de Entrega  
6. Stage 5 — Encerramento & Lições Aprendidas  

Cada stage termina em um Gate com checagem formal de critérios.

---

## 5. Stages e Gates (definição formal)

### 🟦 Stage 0 — Iniciação & Ideação (retroativo — concluído em 27/05/2025)
- **Objetivo:** Formalizar o projeto (TAP), propósito, escopo inicial e papéis.  
- **Principais atividades:** elaborar TAP; definir modelo P2P; metas de MVP; papéis; marcos.  
- **Artefatos obrigatórios:**
  - TAP aprovado (v1.0, 27/05/2025)  
  - Lista inicial de marcos (TAP/PGP)  
- **Gate 0 — Aprovação de Iniciação**  
  - Critérios de saída: TAP aprovado; papéis definidos; marcos iniciais publicados.  
  - Decisão: ✅ Aprovado (retroativo) — evidências em TAP e ata 27/05/2025.

### 🟦 Stage 1 — Planejamento Detalhado (retroativo — concluído ~29/05 a 03/06/2025)
- **Objetivo:** detalhar escopo e arquitetura do MVP.  
- **Atividades:** protótipos, contratos de API, MER, Plano de Gerenciamento (PGP).  
- **Artefatos:**
  - PGP (v1.0, 27/05/2025)  
  - Protótipos base/fluxos (referência GetNinjas/OLX Serviços)  
  - Contratos de API (def.)  
  - MER (Pessoa Física foco)  
- **Gate 1 — Aval do Planejamento**  
  - Critérios: PGP aprovado; protótipos revistos; APIs e MER definidos; riscos mapeados.  
  - Decisão: ✅ Aprovado (retroativo) — evidências em PGP e atas 27/05 e 17/06.

### 🟦 Stage 2 — Desenvolvimento do MVP (retroativo — concluído em 20–24/06/2025)
- **Objetivo:** construir e integrar o MVP funcional.  
- **Atividades:** desenvolvimento Front/Back/BD; integração; testes básicos; demo.  
- **Artefatos:**
  - MVP integrado (20/06/2025)  
  - Evidência de integração (ata 17/06)  
  - Apresentação do MVP (ata 30/06)  
- **Gate 2 — Aceite do MVP**
  - Critérios: busca/listagem inicial; cadastro e autenticação; BD funcional; responsividade básica; integração valida.  
  - Decisão: ✅ Aprovado (retroativo) — atas 17/06 e 30/06.

### 🟦 Stage 3 — Extensões do MVP (em curso, a partir de 30/06/2025)
- **Objetivo:** evoluir o produto com funcionalidades priorizadas.  
- **Atividades:**
  - Barra de busca aprimorada, segmentações por categoria, mosaico inicial  
  - Ranking de prestadores e espaço para patrocinados  
  - Categorias e chave estrangeira no BD (Monyelly)  
  - Decisões técnicas: arquivos no sistema de arquivos; BD guarda referência (ata 08/08)  
  - Protótipos Lovable.dev aprovados (ata 08/08)  
- **Artefatos:**
  - Protótipos atualizados (aprovados)  
  - Especificação de ranking/patrocinados  
  - Modelo de dados com categorias/foreign key  
  - Política de armazenamento de arquivos  
- **Gate 3 — Pronto para Incremento**
  - Critérios: protótipos aprovados; estórias detalhadas; impacto no MER validado; estratégia de armazenamento documentada; riscos atualizados.  
  - Decisão (08/08/2025): ✅ Aprovado — seguir para implementação incremental.

### 🟦 Stage 4 — Estabilização, Testes & Preparação de Entrega (a definir)
- **Objetivo:** garantir qualidade, desempenho e prontidão de release.  
- **Atividades:** testes funcionais, integração, usabilidade; hardening de segurança; documentação de uso; estratégia de deploy; checklist de conformidade.  
- **Artefatos:**
  - Plano e relatório de testes  
  - Guia de operação/usuário  
  - Plano de Deploy & Rollback  
  - Métricas de desempenho e segurança  
- **Gate 4 — Go/No-Go de Release**
  - Critérios: taxa de aprovação de testes ≥ 90%; critérios de aceite atendidos (PGP 4.3); riscos em nível aceitável; rollback definido; documentação completa em /docs.  
  - Decisão: ☐ Aprovado ☐ Condicional ☐ Reprovado

### 🟦 Stage 5 — Encerramento & Lições Aprendidas (a definir)
- **Objetivo:** fechar o ciclo com documentação e melhoria contínua.  
- **Atividades:** entrega final; fechamento de issues; Ata de Lições Aprendidas; atualização de riscos; relatório final.  
- **Artefatos:**
  - Ata de Lições Aprendidas (/docs/atas/)  
  - Relatório de Encerramento  
  - Métricas finais e retrospectiva  
- **Gate 5 — Encerramento do Ciclo**
  - Critérios: todas as entregas aceitas; documentação completa; indicadores consolidados; aprovação do Sponsor.  
  - Decisão: ☐ Aprovado ☐ Condicional ☐ Reprovado

---

## 6. Critérios de Decisão (Checklist por Gate)

| Item       | Descrição                           | Evidência                   | OK |
|------------|-----------------------------------|-----------------------------|----|
| Escopo     | Itens do escopo daquele Stage concluídos | Issues/PRs/protótipos      | ☐  |
| Qualidade  | Critérios de aceite atendidos (PGP §4.3) | Plano/Relatório de Testes | ☐  |
| Integração | Front-end, Back-end e BD integrados | Demo/Logs/Postman          | ☐  |
| Riscos     | Atualizados e mitigados             | Registro de Riscos         | ☐  |
| Cronograma | Marcos cumpridos                     | GitHub Projects            | ☐  |
| Técnica    | Decisões técnicas registradas       | ADR/Atas                   | ☐  |
| Aprovação  | Gatekeepers registraram decisão      | Ata do Gate                | ☐  |

**Opções de decisão:** ✅ Aprovar | ➕ Aprovar com Condições | 🔁 Re-trabalhar e Reapresentar | ⛔ Encerrar

---

## 7. Artefatos Obrigatórios por Stage

| Stage | Artefatos Mínimos |
|-------|------------------|
| 0     | TAP; Marcos; Papéis |
| 1     | PGP; Protótipos; Contratos de API; MER |
| 2     | MVP integrado; Plano/relatório de testes básicos |
| 3     | Protótipos aprovados (Lovable.dev); Política de armazenamento; Especificações de ranking/patrocinados; MER atualizado (categorias) |
| 4     | Plano/Relatório de Testes; Guia do Usuário/Operação; Plano de Deploy & Rollback; Métricas |
| 5     | Ata de Lições Aprendidas; Relatório de Encerramento |

---

## 8. Mecanismos de Monitoramento e Controle
- **Kanban:** GitHub Projects — colunas A Fazer → Em Andamento → Concluído  
- **Ritos:** Reunião semanal + Gate Reviews nas datas-marco  
- **Métricas-chave:** % estórias concluídas por sprint; taxa de aprovação de testes; lead time de PR; defeitos pós-gate  
- **Registro de Decisões (Decision Log):** resoluções de arquitetura e aprovações de protótipos

---

## 9. Calendário-Referência de Gates

| Gate | Janela / Data       | Referência |
|------|-------------------|------------|
| Gate 0 (Iniciação) | 27/05/2025 | TAP v1.0 (ata 27/05) |
| Gate 1 (Planejamento) | 29/05–03/06/2025 | PGP + protótipos + APIs + MER |
| Gate 2 (MVP) | 20–24/06/2025 | MVP integrado (atas 17/06 e 30/06) |
| Gate 3 (Extensões) | 08/08/2025 | Protótipos aprovados; decisão de armazenamento |
| Gate 4 (Release) | A definir | Após implementação de ranking/patrocinados/categorias |
| Gate 5 (Encerramento) | A definir | Após entrega e documentação final |

---

## 10. Riscos e Controles (síntese)
- **Atrasos por disponibilidade da equipe:** acompanhamento semanal; priorizar itens de gate  
- **Integração entre frentes:** contratos claros; testes de integração contínuos  
- **Inexperiência técnica:** dividir tarefas, revisar PRs, registrar decisões; apoio do Sponsor  
- **Desempenho/armazenamento:** arquivos no sistema de arquivos; BD só referência (decisão registrada em 08/08)  

---

## 11. Critérios de Aceite (PGP §4.3)
Uma entrega do Stage é considerada apta ao Gate quando:
- ✅ Cumpre checklist de gate  
- ✅ Está documentada em `/docs` do repositório  
- ✅ Passa em revisão técnica cruzada entre membros  
- ✅ Evidências (prints, links de PR, protótipos) estão anexadas à Ata do Gate  

---

## 12. Fluxo Operacional do Gate
1. PM agenda Gate Review  
2. Equipe apresenta evidências  
3. Gatekeepers deliberam  
4. Registrar decisão e condições (se houver)  
5. Atualizar Issues/Projects e documentação  

---

## 13. Anexos (Modelos)
**A. Template — Ata de Gate**
**B. Template — Decision Log (ADR simples)**
**C. Checklist — Pronto para Gate**
- Artefatos obrigatórios anexados  
- Testes executados e evidenciados  
- Riscos atualizados  
- Documentação em `/docs`  
- Demonstração preparada  

---

## 14. Aprovação deste Documento

| Nome               | Cargo              | Assinatura |
|-------------------|------------------|------------|
| Carla de Medeiros  | Project Manager   | ————————  |
| Prof. Renato Atouguia | Diretor do Projeto | ———————— |

---

## 15. Histórico de Versões

| Versão | Data       | Descrição                             |
|--------|------------|---------------------------------------|
| 1.0    | 13/08/2025 | Versão inicial do Processo Stage-Gate |

