# 24 Perguntas e Respostas sobre Testes Web para Entrevistas de QA

## 1. Quais são os principais desafios em testes web?
**Resposta:**  
Testes web trazem desafios como compatibilidade entre navegadores (Chrome, Firefox, Edge, Safari), diferentes motores de renderização e variações no suporte a padrões web.  
Além disso, o comportamento pode mudar com diferentes tamanhos de tela e densidades de pixels (desktop, tablet, mobile). Também é necessário considerar aspectos como segurança contra ataques XSS/CSRF, performance em conexões lentas e estabilidade frente a atualizações frequentes de navegadores.

---

## 2. Como você garante a compatibilidade entre diferentes navegadores e dispositivos?
**Resposta:**  
Começo identificando os navegadores e sistemas mais usados pelo público-alvo via analytics. Depois, defino uma matriz de teste que cobre:  
- **Principais navegadores** em suas versões atuais e anteriores.  
- **Diferentes sistemas operacionais** (Windows, macOS, Linux, iOS, Android).  
- **Tamanhos de tela e breakpoints responsivos**.  
Uso uma combinação de testes manuais e ferramentas como BrowserStack ou LambdaTest para ampliar a cobertura sem precisar de um laboratório físico enorme.

---

## 3. Quais tipos de testes são mais críticos para garantir a qualidade de uma aplicação web?
**Resposta:**  
Para uma aplicação web de qualidade, considero críticos:  
- **Funcionais:** Garantir que cada recurso funcione conforme o especificado.  
- **UI/UX:** Testar responsividade, consistência visual e experiência de navegação.  
- **Performance:** Avaliar tempo de carregamento, interatividade e estabilidade.  
- **Segurança:** Testar contra injeções, XSS, CSRF, má configuração de headers e autenticação.  
- **Acessibilidade:** Garantir conformidade com WCAG, uso por leitores de tela, navegação via teclado.  
- **Compatibilidade:** Cobrir variações de browsers, SO e dispositivos.  

---

## 4. Como você realiza testes de responsividade?
**Resposta:**  
Uso tanto inspeção via DevTools para simular breakpoints quanto testes em dispositivos reais para validar toque, rolagem e adaptação de elementos.  
Verifico se imagens e textos se ajustam corretamente, se elementos clicáveis permanecem acessíveis e se o layout não quebra em resoluções menos comuns.  
Também testo em orientação retrato e paisagem, já que alguns problemas só aparecem quando o usuário rotaciona o dispositivo.

---

## 5. Qual sua abordagem para testes de performance em aplicações web?
**Resposta:**  
Uso ferramentas como Lighthouse, WebPageTest e Chrome DevTools para medir métricas-chave: LCP (Largest Contentful Paint), FID (First Input Delay) e CLS (Cumulative Layout Shift).  
Além disso, monitoro consumo de memória, número de requisições e tamanho total dos assets.  
Faço testes em redes lentas (3G/4G) e sob alto uso de CPU para garantir boa experiência mesmo em máquinas menos potentes.  
A meta é reduzir tempo de carregamento, evitar bloqueios de renderização e manter a interface fluida.

---

## 6. Como você realiza testes de segurança em aplicações web?
**Resposta:**  
Valido entrada de dados contra injeção de código (XSS, SQL Injection), verifico proteção contra CSRF e uso de HTTPS com configurações corretas.  
Também analiso se tokens de sessão são gerados e armazenados de forma segura, e se senhas são tratadas com criptografia adequada.  
Em alguns casos, uso ferramentas como OWASP ZAP ou Burp Suite para simular ataques e identificar vulnerabilidades antes que cheguem aos usuários.

---

## 7. Qual a importância dos testes de acessibilidade e como você os realiza?
**Resposta:**  
A acessibilidade garante que pessoas com diferentes limitações possam usar a aplicação. Além de ser questão legal em alguns países, é um diferencial de qualidade.  
Uso ferramentas como Axe e Lighthouse Accessibility para checagens automáticas, mas também faço testes manuais: navegação apenas via teclado, validação de contraste de cores e uso de leitores de tela como NVDA e VoiceOver.  
Também reviso a semântica do HTML e uso de ARIA attributes para melhorar a experiência de usuários com necessidades especiais.

---

## 8. Como você garante qualidade em aplicações com alta interatividade (SPA/PWA)?
**Resposta:**  
Para SPAs e PWAs, foco em testes de roteamento, carregamento dinâmico de dados e comportamento offline.  
Valido cache e atualizações via Service Workers, garantindo que o conteúdo exibido seja atualizado corretamente.  
Também testo transições de estado, reatividade da UI e possíveis problemas de memória que podem surgir pelo uso intenso de JavaScript.

---

## 9. Como você aborda a automação de testes web?
**Resposta:**  
Uso ferramentas como Cypress ou Playwright para testes de ponta a ponta, Selenium para casos mais complexos e Jest para testes unitários de front-end.  
Estruturo os scripts de forma modular, evitando acoplamento excessivo à UI, o que facilita manutenção.  
Integro a automação em pipelines de CI/CD, garantindo que cada nova entrega passe por testes automáticos antes de ir para produção.  
Automatizo o que é repetitivo e estável, mantendo testes manuais para cenários exploratórios e críticos.

---

## 10. Como você testa aplicações web em diferentes condições de rede?
**Resposta:**  
Simulo redes lentas e instáveis usando DevTools ou ferramentas de proxy, para validar comportamento de carregamento e tratamento de erros.  
Verifico se mensagens ao usuário são claras quando há falhas de conexão e se o sistema retoma corretamente as operações quando a rede volta.  
Esse tipo de teste é crucial para usuários que acessam via redes móveis ou em regiões com infraestrutura limitada.
