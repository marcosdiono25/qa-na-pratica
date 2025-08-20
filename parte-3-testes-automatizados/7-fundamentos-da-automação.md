# CAPÍTULO 7 - FUNDAMENTOS DA AUTOMAÇÃO

Automação é o processo de usar ferramentas e scripts para validar o software de forma repetitiva, confiável e escalável.  
Ao contrário dos testes manuais, onde o QA executa os testes passo a passo, na automação os casos de teste são traduzidos em código e podem ser executados inúmeras vezes sem intervenção humana.  

Mas é importante entender: **a automação não substitui os testes manuais, eles se complementam**.  
Enquanto os testes manuais permitem explorar, investigar e encontrar falhas inesperadas, a automação garante estabilidade nos fluxos repetitivos e críticos do sistema.  

Muitos acham que automatizar tudo é o caminho, mas isso é um mito. O verdadeiro valor da automação está em liberar tempo do QA para pensar estrategicamente, garantindo que o time de desenvolvimento entregue produtos com mais qualidade e confiança.

---

## 7.1 - Benefícios e desafios da automação

Automação traz ganhos reais, mas também apresenta armadilhas se mal planejada.  

**Benefícios principais:**
1. Execução rápida e repetível, ideal para testes de regressão.
2. Aumento de confiabilidade: menos erros humanos.
3. Redução de custos a longo prazo.
4. Integração em pipelines de Integração Contínua/Entrega Contínua (CI/CD).
5. Visibilidade em tempo real da qualidade do software.

**Desafios da automação:**
1. Custo inicial de implementação (ferramentas, treinamento, infraestrutura).
2. Scripts frágeis que quebram com pequenas mudanças no sistema. 
3. Tempo de manutenção dos testes.
4. Dependência de ambientes de teste estáveis e dados consistentes.

Automação é um investimento: no início pode parecer custoso, mas com o tempo entrega ganhos significativos em velocidade e qualidade.

---

## 7.2 - O que automatizar e o que não automatizar

Nem todos os testes precisam ou devem ser automatizados. O segredo é escolher bem os cenários.  

**O que automatizar:**
1. Testes repetitivos (regressão).
2. Casos críticos para o negócio.
3. Smoke tests (verificação inicial do sistema).
4. Sanity tests (verificação de novas funcionalidades).

**O que não automatizar:**
1. Funcionalidades em constantes mudanças.
2. Testes exploratórios (que exigem criatividade e intuição).
3. Testes que dependem fortemente da percepção humana (usabilidade, estética).

Automatizar sem critério gera retrabalho, aumenta a complexidade e não entrega valor.

---

## 7.3 - Pirâmide de testes

Um dos modelos mais conhecidos em QA é a **pirâmide de testes** criada por Mike Cohn. Ela mostra a proporção ideal de cada tipo de teste:

- **Base (70%): Testes unitários** → garantem que pequenas partes do código funcionem isoladamente.  
- **Meio (20%): Testes de API/serviço** → verificam a comunicação entre componentes.  
- **Topo (10%): Testes de UI** → validam o sistema na perspectiva do usuário.  

Quanto mais próximo da base, mais rápidos, baratos e estáveis são os testes. Já os de UI, embora fundamentais, são mais lentos e frágeis.  
A pirâmide ajuda a equilibrar esforço, custo e cobertura.

---

## 7.4 - Ciclo de vida da automação

A automação não é apenas escrever scripts, é um processo estruturado:

1. **Análise de requisitos:** identificar cenários relevantes.  
2. **Definição das estratégias:** ferramentas, frameworks, arquitetura.  
3. **Implementação dos testes:** escrita dos scripts com boas práticas.  
4. **Integração em pipelines:** garantir execução contínua.  
5. **Monitoramento e manutenção:** revisar e atualizar o código conforme o sistema evolui.  

Automação é viva: precisa ser cuidada para não se tornar um fardo.

---

## 7.5 - Ferramentas e frameworks populares

A escolha da ferramenta depende do contexto, linguagem e tipo de sistema:  

- **Web:** Selenium (clássico e flexível), Cypress (rápido e moderno), Playwright (suporte a múltiplos browsers e linguagens).  
- **Mobile:** Appium (Android/iOS multiplataforma), Detox (React Native).  
- **API:** Postman/Newman, RestAssured, Karate.  

O mais importante não é a ferramenta em si, mas como ela é usada: organização do projeto, boas práticas de escrita e integração com o fluxo de desenvolvimento.

---

## 7.6 - Boas práticas de automação

Automação mal feita custa caro. Algumas boas práticas são essenciais:

1. **Escreva testes independentes:** um não deve depender do resultado do outro.  
2. **Nomenclatura clara:** o nome do teste deve explicar o que está sendo validado.  
3. **Page Object Model (POM):** separar a lógica de teste da lógica de infraestrutura.  
4. **Dados de teste confiáveis:** uso de mocks, stubs ou bancos dedicados.  
5. **Evite sleeps fixos:** prefira waits dinâmicos para sincronização.  

Essas práticas aumentam a durabilidade e reduzem a manutenção.

---

## 7.7 - Métricas e qualidade de automação

Automação só faz sentido se gerar valor mensurável. Algumas métricas importantes:

- **Cobertura de testes automatizados:** porcentagem de casos críticos cobertos.  
- **Tempo médio de execução:** quanto tempo o pipeline leva para rodar todos os testes.  
- **Taxa de falhas falsas (Flaky tests):** indicadores de instabilidades.  
- **Defeitos encontrados x defeitos escapados:** eficiência real da automação.  

Mais do que a quantidade de testes, importa a qualidade dos testes escritos.

---

## 7.8 - Futuro da automação

O cenário de automação evolui rápido. Algumas tendências:

- **IA aplicada em testes:** ferramentas que identificam cenários automaticamente.  
- **Automação baseada em modelos (Model-Based Testing).**  
- **Testes Low-code/No-code:** permitem que profissionais não técnicos automatizem fluxos básicos.  
- **Shift-Left Testing:** testes cada vez mais cedo no ciclo de desenvolvimento.  

O QA do futuro será um profissional estratégico que combina habilidades técnicas, análise crítica e visão de negócios.

---

## 7.9 - Conclusão do capítulo

Fundamentos da automação não é apenas sobre "aprender ferramentas", mas sobre **estratégia, disciplina e boas escolhas**.  
Compreender o que, como e quando automatizar é a chave para colher os verdadeiros benefícios dessa prática.
