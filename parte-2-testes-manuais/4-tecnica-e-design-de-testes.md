# CAPÍTULO 4 - TÉCNICAS E DESIGN DE TESTES (TESTES MANUAIS)

Quando falamos em testes manuais, muitas pessoas pensam em apenas clicar em botões e ver se funciona.  
Mas a realidade é muito mais estratégica: testar manualmente exige planejamento, raciocínio crítico e conhecimento das técnicas de design de teste.  
Este capítulo vai mostrar como transformar testes manuais em algo estruturado, eficiente e confiável.

---

## 4.1 - Introdução aos testes manuais

Os testes manuais ainda são essenciais, mesmo com toda a automação disponível. Eles permitem:
- Descobrir problemas que scripts automáticos não conseguem prever.
- Validar a experiência do usuário final.
- Entender o comportamento do sistema em cenários inesperados.

Mas, para que sejam eficazes, é preciso planejar e desenhar os testes de forma consciente, utilizando técnicas que garantam qualidade e uma cobertura adequada.  
Testar sem planejar é como construir uma casa sem planta: pode até funcionar, mas a chance de erro é enorme.

---

## 4.2 - Design de teste

O design de teste é o processo de criar casos de teste que cobrem requisitos, fluxos e cenários críticos, evitando testes aleatórios ou repetitivos.

**Etapas do design de teste:**
1. **Analisar requisitos:** entender exatamente o que o sistema deve fazer.  
2. **Identificar funcionalidades críticas:** aquelas que impactam diretamente o usuário.  
3. **Criar cenários de teste:** simular situações reais de uso.  
4. **Priorizar cenários de teste:** nem tudo precisa ser testado imediatamente; priorize os de risco maior.  
5. **Revisar cobertura:** garantir que todos os requisitos tenham pelo menos um caso de teste cobrindo.

---

## 4.3 - Técnicas de teste

Existem diversas técnicas que ajudam a organizar os testes e garantir cobertura. As principais são:

### Teste de caixa-preta

- Foco no resultado esperado, sem se preocupar com o código interno.
- Baseado nos requisitos e especificações do sistema.

**Exemplos:**
- Validar login com usuário válido e inválido.  
- Testar envio de formulário com campos obrigatórios e opcionais.

---

### Teste de caixa-branca

- Foco no código e na lógica interna.
- Mais usado por quem tem conhecimento técnico, mas QAs experientes também podem executar.

**Exemplos:**
- Verificar se todos os caminhos de um algoritmo são executados.  
- Testar validações internas que impactam o usuário final.

---

### Teste exploratório

- Baseado na curiosidade e experiência do QA.
- Permite descobrir falhas que casos de teste não cobrem.

**Técnicas:**
- Navegar fora do fluxo normal do sistema.  
- Inserir dados inesperados.  
- Combinar ações em sequências incomuns.

---

### Teste baseado em risco

- Prioriza o que tem maior impacto ou maior chance de falhas.
- Útil quando o tempo é limitado.

**Exemplos:**
- Funcionalidades de pagamento e segurança têm prioridade maior que recursos secundários.

---

## 4.4 - Boas práticas de teste manual

1. **Documentar tudo:** registre casos de teste, resultados e observações.  
2. **Ser claro e objetivo:** descreva os passos de forma que qualquer outro QA possa reproduzir.  
3. **Manter rastreabilidade:** vincule cada caso de teste a um requisito específico.  
4. **Reutilizar casos de teste:** cenários bem feitos podem ser aplicados em diferentes versões do sistema.  
5. **Revisar e melhorar constantemente:** teste é um processo evolutivo, não algo estático.

---

## 4.5 - Conclusão do capítulo

Testes manuais não são apenas clicar e observar.  
Eles exigem estratégia, conhecimento e raciocínio crítico.  

Quando aplicamos técnicas de design de teste corretamente, conseguimos:
- Garantir cobertura de funcionalidades importantes.  
- Reduzir retrabalho.  
- Descobrir falhas que passariam despercebidas.
