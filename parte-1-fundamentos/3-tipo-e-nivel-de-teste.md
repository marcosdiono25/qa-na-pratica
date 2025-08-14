# CAPÍTULO 3 - TIPOS E NÍVEIS DE TESTE

Quando começamos na área de QA, é comum ouvirmos a frase: "teste tudo e qualquer coisa que encontrar um bug".  
Mas a realidade é muito diferente: para ser um QA eficiente, é preciso entender os diferentes níveis de teste, quando aplicá-los e qual é o seu propósito.  
Um teste mal planejado pode ser tão prejudicial quanto não testar nada.

---

## 3.1 - Tipos de testes

Os tipos de testes podem ser divididos em duas grandes categorias: **funcionais** e **não funcionais**.

---

### Teste funcional

Os testes funcionais verificam se o sistema faz exatamente o que deveria fazer, de acordo com os requisitos especificados.  
Ou seja, aqui você garante que cada função cumpre seu papel.

**Exemplos:**
- O login só permite acesso com e-mail e senha corretos.
- O botão de "Enviar Formulário" realmente envia os dados para o servidor.
- O sistema calcula corretamente o valor total dos produtos no carrinho de compras.

Ferramentas comuns: Selenium, Cypress, Postman (para API) e até testes manuais bem estruturados.

**Dica prática:**  
Sempre que for testar uma funcionalidade, pergunte:  
_"Se eu fosse o usuário, isso faria sentido? Está funcionando como prometido?"_

---

### Teste não funcional

Diferente dos testes funcionais, os testes não funcionais não verificam **o que** o sistema faz, mas **como** ele se comporta.  
Eles avaliam características como performance, segurança, usabilidade e escalabilidade.

**Exemplos:**
- A aplicação suporta 1.000 usuários simultâneos sem travar.
- O sistema responde em menos de 2 segundos ao buscar um registro.
- Os dados do usuário estão protegidos com criptografia.
- Uma pessoa com deficiência consegue navegar pelo site facilmente.

Ferramentas comuns: JMeter, K6, OWASP ZAP, Lighthouse.

**Dica prática:**  
Se algo não impacta diretamente uma função, mas afeta a experiência do usuário ou a estabilidade do sistema, é um candidato a teste não funcional.

---

### Teste exploratório

O teste exploratório não está oficialmente em "funcional" ou "não funcional".  
Aqui, o QA usa sua experiência, curiosidade e intuição para encontrar falhas que não estão nos roteiros formais de teste.

**Exemplo:**  
Um QA pode tentar inserir caracteres estranhos nos campos de um formulário ou clicar em botões em ordem inesperada para ver o que acontece.

---

## 3.2 - Níveis de teste

Além de saber **o que** testar, é fundamental saber **em que nível** o teste deve ser feito.  
Os níveis mais comuns são:

1. **Teste unitário**  
- **O que é:** Testa pequenas unidades do sistema, normalmente funções ou métodos isolados.  
- **Quem faz:** Desenvolvedores ou, às vezes, QAs com conhecimento em automação.  
- **Exemplo:** Verificar se uma função que calcula descontos retorna valores corretos para diferentes entradas.

2. **Teste de integração**  
- **O que é:** Avalia se diferentes módulos do sistema funcionam bem juntos.  
- **Exemplo:** O módulo de cadastro de usuário enviando dados corretamente para o módulo de autenticação e o banco de dados.

3. **Teste de sistema**  
- **O que é:** Testa o sistema como um todo, verificando se todos os módulos juntos cumprem os requisitos.  
- **Exemplo:** Testar todo o fluxo de compra no e-commerce: login, adicionar produto, calcular total, aplicar cupom e finalizar pedido.

4. **Teste de aceitação**  
- **O que é:** Validado pelo usuário final ou stakeholders para garantir que o sistema atende às expectativas.  
- **Exemplo:** Um cliente acessando a plataforma e confirmando que o fluxo de compra está funcionando como imaginava.

**Dica prática:**  
Quanto mais cedo você conseguir testar os níveis menores (unitário e integração), menos problemas chegarão no sistema completo — e menor será o retrabalho.

---

## 3.3 - Conclusão do capítulo

Aprendemos e devemos sempre manter a mentalidade de que:

- **Funcional:** Verifica o que o sistema faz.  
- **Não funcional:** Verifica como o sistema se comporta.  
- **Exploratório:** Verifica o sistema de forma livre, antecipando problemas que ninguém pensou.  
- **Níveis de teste:** Unitário → Integração → Sistema → Aceitação.
