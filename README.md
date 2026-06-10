# Planejamento-Agil-SLDC-2

# Planejamento Ágil - Projeto QuadroVerse

## 1. Nome do projeto e descrição do problema
**Projeto:** QuadroVerse
**Descrição:** O projeto visa criar uma plataforma digital para que quadrinistas e criadores de HQs independentes possam publicar suas obras, além de contar com um dashboard de gestão para acompanhar métricas de leitura e monetização. O problema a ser resolvido é a fragmentação de ferramentas que os artistas independentes enfrentam para gerenciar e lucrar com suas publicações.

## 2. Objetivo da primeira entrega ou sprint
**Objetivo:** Entregar o MVP (Produto Mínimo Viável) do Dashboard do Criador, permitindo que o usuário faça o cadastro na plataforma, realize o upload de uma HQ em formato de imagem/PDF e visualize a obra no seu painel.

## 3. Definição dos papéis da equipe
* **Product Owner (PO):** Responsável por priorizar as funcionalidades do dashboard e garantir o alinhamento com as necessidades dos quadrinistas.
* **Scrum Master:** Responsável por facilitar as daily meetings, remover impedimentos técnicos da equipe e garantir que o quadro Kanban esteja atualizado.
* **Time de Desenvolvimento:** Responsável pela implementação do banco de dados, interface (UI/UX) e lógica de upload dos arquivos.

## 4. Backlog inicial
1. Issue #1: Criar modelagem do banco de dados para Usuários e HQs.
2. Issue #2: Desenvolver a tela de Login e Cadastro de artistas.
3. Issue #3: Criar a interface inicial do Dashboard de gestão.
4. Issue #4: Implementar a funcionalidade de Upload de arquivos (HQs).
5. Issue #5: Desenvolver a listagem de HQs publicadas no painel do artista.

## 5. Critérios de aceite (Exemplo para 3 issues)
* **Issue #2 (Login/Cadastro):** 
  * O sistema deve validar e-mails duplicados.
  * Senhas devem ter no mínimo 8 caracteres.
  * Em caso de sucesso, redirecionar para a rota /dashboard.
* **Issue #4 (Upload de HQs):** 
  * O sistema deve aceitar apenas extensões .pdf, .png e .jpg.
  * O tamanho máximo do arquivo deve ser de 50MB.
  * Deve exibir uma barra de progresso durante o envio.
* **Issue #5 (Listagem no Painel):**
  * O grid deve ser responsivo (adaptável para mobile e desktop).
  * Cada HQ deve exibir uma miniatura (thumbnail) da capa.

## 6. Proposta de quadro Kanban
* **Backlog:** Tarefas levantadas mas não priorizadas para agora.
* **To Do:** Tarefas prontas para iniciar na Sprint.
* **In Progress (WIP: 3):** Tarefas em desenvolvimento ativo. Limite de 3 tarefas simultâneas para evitar gargalos.
* **Code Review / Test (WIP: 2):** Tarefas aguardando revisão de código por outro membro da equipe.
* **Done:** Tarefas finalizadas que atendem à Definition of Done.

## 7. Estratégia de Git Flow adaptado
* **main:** Branch principal, contendo apenas código estável e pronto para produção.
* **develop:** Branch de integração contínua, onde as features são testadas juntas antes de ir para a main.
* **Padrão de branches:**
  * feature/nome-da-funcionalidade (ex: feature/tela-de-login)
  * bugfix/nome-do-bug (ex: bugfix/erro-upload-pdf)
  * hotfix/erro-critico-producao
* **Regra para Pull Requests (PRs):** Todo PR apontado para a branch develop ou main exige aprovação de pelo menos 1 membro da equipe antes do merge, e o código não deve conter conflitos.

## 8. Definition of Done (DoD) do projeto
Uma tarefa só é considerada "Pronta" (Done) quando:
* O código atende a todos os Critérios de Aceite da Issue.
* Passou por Code Review (Pull Request aprovado).
* Não quebra o layout em dispositivos móveis (responsividade).
* O código foi integrado à branch `develop` sem erros.

## 9. Principais riscos ou gargalos previstos
* **Armazenamento:** O upload de imagens pesadas das HQs pode estourar o limite de armazenamento em nuvem gratuito rapidamente.
* **Curva de aprendizado:** Dificuldades da equipe com a ferramenta escolhida para a criação do dashboard, podendo atrasar a entrega das issues de interface.
