# 🤖 Universal CLAUDE.md Boilerplate

Um template definitivo e pragmático para domar agentes de IA autônomos (como Claude Code, Cursor, Aider e GitHub Copilot) através de **System Prompting em nível de repositório**.

## 🎯 Por que isso existe?

Agentes de inteligência artificial sofrem de um "defeito" comportamental padrão: **eles querem te agradar o mais rápido possível**. Sem limites rígidos, isso resulta em:
- **Overengineering:** Criação de interfaces prematuras e abstrações desnecessárias.
- **Alucinações:** Tentativas de adivinhar o código em vez de ler a estrutura real.
- **Efeito Destrutivo:** Reescrever arquivos inteiros apenas para adicionar uma linha de código.

Este boilerplate inverte o controle. Em vez de apenas descrever o projeto, ele **dita como a IA deve se comportar**, forçando-a a assumir a postura de um Engenheiro de Software Sênior focado em entregas pragmáticas (MVP) e na manutenção da sanidade do código.

---

## 🧠 Entendendo o Boilerplate (O "Porquê" de cada seção)

### 1. MANDATORY WORKFLOW (Non-Negotiable)
**O que é:** As leis absolutas do repositório.
**Por que está aqui:** IAs tendem a pular etapas de planejamento. A lista de "Red Flags" (desculpas comuns que a IA usa para pular processos, como *"É só uma alteração simples"*) bloqueia racionalizações. Exigir o uso de ferramentas de mapeamento (como Graphify ou AST) antes de ler arquivos brutos economiza milhares de tokens e previne que a IA se perca no contexto.

### 2. AI AGENT BEHAVIOR (Postura)
**O que é:** O manual de conduta do "Sênior".
**Por que está aqui:** Para aplicar o princípio KISS (Keep It Simple, Stupid).
- **Modificações Cirúrgicas:** Impede que a IA mude a formatação de funções adjacentes que já estavam funcionando.
- **Self-QA Obrigatório:** Quebra o ciclo frustrante de *"caminho do arquivo errado"* ou *"tipo any implícito"*. A IA é instruída a fazer o próprio *code review* e checar tipagens estritas antes de te devolver a resposta.

### 3. PROJECT OVERVIEW & STACK
**O que é:** O contexto técnico.
**Por que está aqui:** Para a IA não precisar adivinhar se você está usando React ou Vue, Prisma ou TypeORM, PostgreSQL ou MongoDB. Manter isso enxuto garante que o contexto base consuma o mínimo de tokens possível em cada requisição.

### 4. ARCHITECTURE & RULES
**O que é:** As barreiras arquitetônicas.
**Por que está aqui:** Impede que a IA quebre o padrão do projeto. Se a regra diz *"Controllers apenas lidam com HTTP, regras de negócio vão para Services"*, a IA não vai jogar uma query complexa de banco de dados diretamente na rota, mantendo o Clean Code sem você precisar microgerenciar.

### 5. CORE COMMANDS
**O que é:** O cinto de utilidades da CLI.
**Por que está aqui:** Agentes como o Claude Code podem executar comandos de terminal. Ao fornecer os comandos de build e linting, você permite que a IA faça o fluxo completo: escreve o código -> roda o linter -> corrige os próprios erros -> avisa que terminou.

---

## 🚀 Como usar

1. Copie o arquivo `CLAUDE.md` deste repositório.
2. Cole na raiz do seu projeto novo e renomeie para `CLAUDE.md` (ou o nome suportado pela sua IDE/Agente).
3. Preencha as seções **3, 4 e 5** com os detalhes do seu projeto (leva menos de 5 minutos).
4. Inicie o seu assistente de IA. Ele já nascerá com a mentalidade correta para o projeto.
