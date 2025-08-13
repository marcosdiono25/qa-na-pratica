# CAPÍTULO 2 - CICLO DE VIDA DE DESENVOLVIMENTO E O PAPEL DO QA EM CADA CICLO

Quando um software chega até você, pronto para usar, ele já passou por um longo caminho: ideias rabiscadas em papel, discussões de funcionalidades, desenvolvimento, testes e ajustes. Esse caminho é chamado de ciclo de vida de desenvolvimento de software (SDLC — Software Development Life Cycle).  
Entender o SDLC é fundamental para qualquer QA, porque o seu papel muda em cada etapa. Se você não souber onde nem como agir, vai perder a oportunidade de prevenir problemas antes que eles apareçam.

---

## 2.1 - MODELOS DE CICLO DE VIDA

Existem vários modelos de SDLC, e cabe a cada empresa escolher o que melhor combina com sua realidade. Os mais comuns são:  

1. **Waterfall (cascata):**  
- As etapas acontecem de forma sequencial (primeiro análise, depois desenvolvimento, depois testes).  
- Mais rígido e difícil de voltar atrás.  
- Ainda usado em projetos de governo ou onde há alta regulamentação.  
- **Desafio para o QA:** só entra no final, o que aumenta o risco de encontrar bugs tarde demais.

2. **Ágil:**  
- Entregas incrementais, trabalho em sprints curtas.  
- Mais flexível e adaptável a mudanças.  
- **Desafio para o QA:** precisa estar envolvido desde o início e testar continuamente.  

3. **Interativo/Incremental:**  
- Similar ao Ágil, mas com foco em protótipos que vão sendo melhorados.  
- **Desafio para o QA:** lidar com mudanças rápidas e testes regressivos frequentes.

4. **DevOps:**  
- Integração entre desenvolvimento e operações.  
- Deploys e testes automatizados contínuos.  
- **Desafio para o QA:** pensar em testes que rodem automaticamente sem travar o pipeline.

---

## 2.2 - FASE DO CICLO DE VIDA E PAPEL DO QA

Vamos olhar o ciclo como um todo e entender onde o QA atua.

---

### FASE 1 - Levantamento de requisitos

**O que acontece:** Reuniões com stakeholders para entender o que o sistema deve fazer.  
**Papel do QA:**  
1. Analisar se os requisitos estão claros: qualquer ambiguidade gera problema no desenvolvimento e nos testes.  
2. Propor critérios de aceite: definir de forma objetiva quando uma funcionalidade será considerada "pronta".  
3. Pensar nos riscos: antecipar cenários de falha.  

**Exemplo:**  
Se o requisito diz: "O sistema deve permitir que o usuário se cadastre". O QA deve se perguntar:  
- Com quais dados?  
- Há campos obrigatórios?  
- O que acontece se o e-mail for inválido?  
- Qual mensagem de erro?

---

### FASE 2 - Planejamento

**O que acontece:** Definição de escopo, prazos, recursos e ferramentas.  
**Papel do QA:**  
1. Estimar o esforço para os testes.  
2. Escolher ferramentas (Postman, Robot Framework, Cypress).  
3. Planejar ambientes de teste.  
4. Definir métricas (quantidade de casos de teste, cobertura, tempo estimado).

---

### FASE 3 - Design/Arquitetura

**O que acontece:** Definição técnica de como o sistema será construído.  
**Papel do QA:**  
1. Revisar fluxos e diagramas.  
2. Validar se o design permite testar claramente.  
3. Sugerir ajustes para melhorar a testabilidade.

**Exemplo:**  
Se o time planeja uma API sem documentação, o QA pode sugerir criar um Swagger para facilitar os testes.

---

### FASE 4 - Desenvolvimento

**O que acontece:** Codificação da solução.  
**Papel do QA:**  
1. Revisar o código junto com desenvolvedores.  
2. Criar scripts de testes automatizados em paralelo.  
3. Validar pequenas entregas antes do código ir para a etapa final.

---

### FASE 5 - Testes

**O que acontece:** Execução dos testes manuais e automatizados.  
**Papel do QA:**  
1. Executar casos de teste planejados.  
2. Executar testes exploratórios.  
3. Reportar bugs com clareza.  
4. Validar correções.  
5. Reexecutar testes regressivos.

---

### FASE 6 - Implementação

**O que acontece:** O sistema é colocado em produção.  
**Papel do QA:**  
1. Realizar Smoke Tests pós-deploy.  
2. Garantir que funcionalidades críticas estão ativas.  
3. Validar se os dados foram migrados corretamente (quando houver migração).

---

### FASE 7 - Manutenção

**O que acontece:** Ajustes, melhorias e correções de problemas pós-produção.  
**Papel do QA:**  
1. Reproduzir bugs reportados por usuários.  
2. Testar correções rapidamente.  
3. Garantir que novas alterações não quebrem funcionalidades existentes.

---

## 2.3 - O QA COMO PEÇA ESTRATÉGICA

Um erro comum é deixar o QA isolado para testar no final. Isso gera:  
- Mais bugs em produção  
- Mais trabalho  
- Mais custos  

Quando o QA participa desde a primeira reunião, o time ganha:  
- Menos ambiguidade  
- Menos retrabalhos  
- Produtos mais estáveis

---

## 2.4 - CONCLUSÃO DO CAPÍTULO

O QA não é um ator de uma única cena, mas alguém que percorre o palco do início ao fim.  
Se você quer ser um QA diferenciado, entenda que seu trabalho começa antes de existir qualquer linha de código.
