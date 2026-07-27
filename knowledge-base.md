# 📚 Base de Conhecimento: Convenções do Fluxo de Desenvolvimento

Este documento reúne as regras oficiais do time de desenvolvimento e serve como fonte única de verdade para o Dev Agent Assistant.

## 1. Padrões de Branches, Commits e Merge Requests

### 1.1. Nomenclatura de Branches
O nome da branch sempre deve incluir o número da TASK correspondente e seguir o formato:
`[tipo]/[numero-da-task]-[breve-descricao-hifenizada]`

Tipos de branch aceitos:
*   `feature/` -> Nova funcionalidade
*   `bugfix/` -> Correção de bug em desenvolvimento/homologação
*   `incident/` -> Correção de incidente ou problema operacional
*   `hotfix/` -> Correção urgente em ambiente de produção
*   `refactor/` -> Refatoração de código (sem alteração na regra de negócio)
*   `chore/` -> Ajustes técnicos, alterações em pipelines, configurações, atualização de dependências, etc.

*Exemplo:* `feature/141393-visualizacao-comprimida-tickets`

### 1.2. Mensagens de Commit
As mensagens de commit devem seguir as convenções de Conventional Commits, vinculando o ID da tarefa:
`[tipo]([numero-da-task]): [breve descrição em português e letras minúsculas]`

Mapeamento de tipos para Commits:
*   `feature/` vira `feat`
*   `bugfix/` e `incident/` viram `fix`
*   `hotfix/` vira `hotfix`
*   `refactor/` vira `refactor`
*   `chore/` vira `chore`

*Exemplo:* `feat(141393): adiciona visualizacao comprimida`

### 1.3. Título de Merge Request (MR)
O título do Merge Request deve seguir o formato:
`[[numero-da-task]] [Título da tarefa com maiúscula inicial]`

*Exemplo:* `[141393] Visualização comprimida tickets`

---

## 2. Checklist Manual de Validação (Antes do Merge)
Ao criar a descrição de um Merge Request, o agente deve incluir este checklist para o desenvolvedor marcar manualmente:

- [ ] Realizei testes manuais do fluxo principal e caminhos alternativos/erros.
- [ ] Removi códigos temporários (como `console.log`, `print`, `TODO`s ou trechos de código comentados).
- [ ] Mapeei e comuniquei alterações em variáveis de ambiente ou migrations de banco de dados (se houver).
- [ ] Realizei uma auto-revisão do código em busca de clareza e legibilidade.

---

## 3. Limite de Atuação
O agente não deve criar novas convenções. Se uma pergunta não puder ser respondida com base nas regras acima, o agente deve responder:
*"Desculpe, mas não tenho essa convenção registrada na minha base de conhecimento. Por favor, consulte o Tech Lead ou a documentação oficial da equipe."*
