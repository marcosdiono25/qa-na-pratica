# CAPÍTULO 8 - AUTOMAÇÃO WEB (teoría)

A web é o caminho mais visível do software para o usuário final. É nela que estão os formulários, botões e links que sustentam o sistema para uma boa experiência de uso. Por isso, garantir qualidade na interface é essencial.  

A automação web tem como objetivo validar se funcionalidades no navegador estão funcionando de forma esperada. No entanto, testes de interface gráfica (UI) são mais frágeis e lentos que testes de API ou unitários. Por isso, devem ser usados de forma estratégica, priorizando fluxos críticos e representativos.  

---

## 8.1 - Estrutura de testes web

Ao estruturar uma automação web, é importante pensar em camadas. Um bom projeto deve:

- Separar lógica de teste da lógica de interação com a UI.  
- Ser reutilizável e fácil de manter.  
- Suportar múltiplos navegadores (quando necessário).  

A arquitetura mais comum é baseada no **Page Object Model (POM)**, onde cada página da aplicação é representada como uma classe, encapsulando os elementos e as ações possíveis nela.  

---

## 8.2 - Ferramentas populares

Várias ferramentas podem ser usadas para automação web. Entre as principais estão:

- **Selenium WebDriver:** pioneira, suporta vários navegadores e linguagens.  
- **Cypress:** moderno, rápido e fácil de usar, porém limitado a navegadores baseados em Chromium.  
- **Playwright:** mantido pela Microsoft, suporta múltiplos navegadores e linguagens, com recursos avançados de paralelismo.  

A escolha da ferramenta depende do contexto da equipe, do projeto e do tipo de validação necessária.  

---

## 8.3 - Estrutura de um caso de teste web

Um caso de teste automatizado web geralmente segue esta estrutura:  

1. **Setup:** abrir navegador, preparar ambiente, acessar URL inicial.  
2. **Ações:** preencher campos, clicar em botões, navegar entre páginas.  
3. **Verificação (asserts):** validar se o comportamento esperado ocorreu.  
4. **Teardown:** fechar navegador, limpar dados temporários.  

Exemplo em pseudocódigo:

    Abrir navegador
    Acessar URL de login
    Preencher campos "E-mail" e "Senha" com credenciais válidas
    Clicar no botão "Enviar"
    Validar se página inicial foi carregada
    Fechar navegador

---


---

## 8.4 - Integração com CI/CD

A automação web ganha força quando integrada a pipelines de integração contínua (CI/CD). Assim, a cada commit, os testes são executados em ambientes controlados, garantindo feedback rápido para o time.  

Ferramentas como **Jenkins, GitHub Actions, GitLab CI e Azure DevOps** permitem configurar pipelines que:  

- Instalam dependências.  
- Sobem o ambiente de teste.  
- Executam os casos automatizados.  
- Geram relatórios (HTML, Allure, Extent Reports).  

---

## 8.5 - Cenários comuns de automação web

Alguns exemplos de fluxos frequentemente automatizados:  

- Login e logout.  
- Cadastro de usuário.  
- Fluxos de compra em e-commerce (adicionar ao carrinho, checkout, pagamento).  
- Navegação entre páginas.  
- Validação de mensagens de erro.  

Esses cenários garantem que as áreas mais críticas da aplicação continuem funcionando a cada atualização.  

---

## 8.6 - Desafios e armadilhas

Automação web é poderosa, mas exige cuidado. Alguns problemas comuns:  

- **Testes quebradiços:** elementos mudam de ID/class constantemente.  
- **Execução lenta:** excesso de waits fixos e cenários longos.  
- **Dependência de dados:** testes que falham por falta de massa de dados adequada.  

A solução está em estruturar bem os testes, usar seletores confiáveis (ex: `data-test-id`) e garantir ambientes estáveis.  

---

## 8.7 - Tendências em automação web

- **Testes com inteligência artificial:** ferramentas que identificam mudanças na UI automaticamente.  
- **Headless browsers:** execução sem abrir a janela do navegador, acelerando os testes.  
- **Cloud Testing:** execução em múltiplos navegadores e dispositivos na nuvem (ex.: BrowserStack, Sauce Labs).  

---

## 8.8 - Conclusão do capítulo

A automação web é a “vitrine” da qualidade de software, pois valida o que o usuário realmente vê. Porém, deve ser usada de forma estratégica, garantindo estabilidade e rapidez sem comprometer a manutenção.


---

## 8.4 - Integração com CI/CD

A automação web ganha força quando integrada a pipelines de integração contínua (CI/CD). Assim, a cada commit, os testes são executados em ambientes controlados, garantindo feedback rápido para o time.  

Ferramentas como **Jenkins, GitHub Actions, GitLab CI e Azure DevOps** permitem configurar pipelines que:  

- Instalam dependências.  
- Sobem o ambiente de teste.  
- Executam os casos automatizados.  
- Geram relatórios (HTML, Allure, Extent Reports).  

---

## 8.5 - Cenários comuns de automação web

Alguns exemplos de fluxos frequentemente automatizados:  

- Login e logout.  
- Cadastro de usuário.  
- Fluxos de compra em e-commerce (adicionar ao carrinho, checkout, pagamento).  
- Navegação entre páginas.  
- Validação de mensagens de erro.  

Esses cenários garantem que as áreas mais críticas da aplicação continuem funcionando a cada atualização.  

---

## 8.6 - Desafios e armadilhas

Automação web é poderosa, mas exige cuidado. Alguns problemas comuns:  

- **Testes quebradiços:** elementos mudam de ID/class constantemente.  
- **Execução lenta:** excesso de waits fixos e cenários longos.  
- **Dependência de dados:** testes que falham por falta de massa de dados adequada.  

A solução está em estruturar bem os testes, usar seletores confiáveis (ex: `data-test-id`) e garantir ambientes estáveis.  

---

## 8.7 - Tendências em automação web

- **Testes com inteligência artificial:** ferramentas que identificam mudanças na UI automaticamente.  
- **Headless browsers:** execução sem abrir a janela do navegador, acelerando os testes.  
- **Cloud Testing:** execução em múltiplos navegadores e dispositivos na nuvem (ex.: BrowserStack, Sauce Labs).  

---

## 8.8 - Conclusão do capítulo

A automação web é a “vitrine” da qualidade de software, pois valida o que o usuário realmente vê. Porém, deve ser usada de forma estratégica, garantindo estabilidade e rapidez sem comprometer a manutenção.

