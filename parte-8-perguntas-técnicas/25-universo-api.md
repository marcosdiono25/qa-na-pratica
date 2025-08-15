# 25 Perguntas e Respostas sobre Testes de API para Entrevistas de QA

## 1. O que é um teste de API e por que ele é importante?
**Resposta:**  
Testes de API validam se os endpoints expostos pelo back-end estão funcionando conforme esperado, retornando dados corretos, nos formatos corretos e com o desempenho adequado.  
Eles são importantes porque as APIs geralmente são o “coração” de sistemas modernos — uma falha nelas pode impactar não só o front-end, mas também integrações com outros sistemas e parceiros.  
Além disso, testar APIs permite detectar problemas antes que a camada visual seja implementada, acelerando a entrega de qualidade.

---

## 2. Quais são os principais tipos de testes que você realiza em APIs?
**Resposta:**  
- **Funcionais:** Validam se cada endpoint cumpre seu objetivo (ex.: criar usuário, listar produtos).  
- **Validação de dados:** Checar se o formato do retorno (JSON/XML) e os campos estão corretos.  
- **Testes de status HTTP:** Garantir que erros e sucessos retornem códigos adequados (200, 400, 404, 500).  
- **Segurança:** Autenticação, autorização, proteção contra ataques como SQL Injection e XSS via payloads maliciosos.  
- **Performance:** Testar tempo de resposta e estabilidade sob carga.  
- **Contratos:** Garantir que a API siga o contrato definido no Swagger/OpenAPI.

---

## 3. Como você valida a estrutura e o conteúdo de uma resposta da API?
**Resposta:**  
Uso ferramentas como Postman, Insomnia ou bibliotecas de teste (ex.: Chai, Jest) para validar:  
- **Tipo de dado** (string, number, array, object).  
- **Campos obrigatórios** (ex.: `id`, `createdAt`).  
- **Valores esperados** (ex.: `status = active`).  
Também uso JSON Schema Validation para garantir que a resposta siga o padrão acordado, o que ajuda a detectar mudanças não autorizadas no contrato.

---

## 4. Como você aborda testes de segurança em APIs?
**Resposta:**  
Valido autenticação (ex.: OAuth2, JWT) e autorização (perfis de usuário e permissões).  
Testo endpoints privados sem token para garantir que estão protegidos.  
Faço injeções de SQL/NoSQL e envio payloads inválidos para verificar se a API filtra corretamente os dados.  
Também checo se tokens expiram no tempo correto e se dados sensíveis nunca são enviados em texto puro.

---

## 5. Qual a diferença entre testes manuais e automatizados de API e quando usar cada um?
**Resposta:**  
- **Manuais:** Ótimos para testes exploratórios, validação rápida de novos endpoints ou investigações pontuais.  
- **Automatizados:** Essenciais para regressão, garantindo que endpoints existentes continuem funcionando a cada nova entrega.  
Normalmente, começo manual para entender o endpoint e depois crio scripts automatizados para mantê-lo monitorado no CI/CD.

---

## 6. Como você realiza testes de performance em APIs?
**Resposta:**  
Uso ferramentas como JMeter, k6 ou Gatling para simular múltiplas requisições simultâneas e medir tempo médio de resposta, throughput e taxa de erro.  
Também faço testes de stress para ver como a API se comporta sob carga extrema e de soak test para avaliar estabilidade em longos períodos.  
Esses testes ajudam a identificar gargalos como queries lentas ou falta de otimização no código.

---

## 7. Como você lida com versionamento de APIs nos testes?
**Resposta:**  
Crio suítes de teste separadas para cada versão (v1, v2, etc.) e valido mudanças de contrato.  
Também testo backward compatibility quando uma versão antiga ainda está ativa, para garantir que clientes antigos não quebrem.  
Documentar e manter claro qual suite cobre qual versão evita confusões e falhas em produção.

---

## 8. Como você integra testes de API em um pipeline de CI/CD?
**Resposta:**  
Uso bibliotecas de teste (ex.: Newman para Postman, Jest, Pytest) e configuro execução automática a cada commit ou deploy.  
Se algum teste falhar, o pipeline bloqueia a entrega.  
Também gero relatórios HTML ou no formato JUnit para fácil visualização no sistema de integração (Jenkins, GitLab, GitHub Actions).

---

## 9. Como você testa cenários de erro em APIs?
**Resposta:**  
Envio dados inválidos, parâmetros faltando e formatos incorretos para validar respostas.  
Por exemplo: enviar `string` onde se espera `number`, IDs inexistentes ou campos extras não suportados.  
Espero que a API retorne mensagens de erro claras e códigos HTTP adequados (ex.: 400 para requisição inválida, 404 para recurso não encontrado).

---

## 10. Como você garante que mudanças na API não quebrem integrações existentes?
**Resposta:**  
Mantenho testes de contrato sempre atualizados e automatizados.  
Quando há mudanças, executo testes em ambientes de homologação antes do deploy em produção.  
Também costumo configurar monitoramento de API (ex.: com Postman Monitors ou ferramentas de APM) para detectar falhas em tempo real e agir rapidamente.
