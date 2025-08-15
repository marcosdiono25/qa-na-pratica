# CAPÍTULO 5 - CASOS DE TESTE

Depois de aprender a desenhar e planejar nossos testes, próximo passo é aprender a documentar esses testes de forma organizada. É aqui que entra os casos de teste, a espinha dorsal da vida de um QA. Um caso de teste bem escrito, garante que qualquer QA possa reproduzir o teste, verificar resultados e registrar problemas sem ambiguidades. Alem disso, ele ajuda a manter rastreabilidade com os requisitos de sistema, algo especial para garantir a qualidade do software.

---

## 5.1 - O que é caso de teste

Um caso de teste é uma descrição detalhada de uma ação ou conjunto de ações que devem ser execultadas para garantir que um requisito está sendo cumprido. 

Elementos principais de um caso de teste:
1. ID do caso de teste: um identificador único de cada caso de teste. EX.: CT-001.
2. Título: descreve de forma resumida o que será testado.
3. Requisito vinculado: qual requisito está sendo validado.
4. Pré-condições: o que precisa está preparado antes do teste.
5. Passos de execução: instruções detalhadas de como realizar o teste.
6. Dados de teste: valores ou arquivos que serão usados.
7. Resultado esperado: o comportamento correto do sistema.
8. Resultado obtido: o resultado verificado após realizar o teste.
9. Status: Passou/Falhou/Bloqueou
10. Observações: notas adicionais, como problemas ou exceções encontradas.
11. Evidências: fotos ou videos que comporove o resultado obtido.

---

## 5.2 - Um exenplo de caso de teste

Imagine que iremos testar a funcionalidade de login de uma pagina, um exemplo de caso de teste poderia ser:

- ID: CT-001
- Titulo: Login com usuário válido
- Requisito: RF-001
- Pré-condições: Usuário já cadastrado e ativo.
- Passos de execução:
    1. Acessar a página de login
    2. preencher o campo email com dados válidos.
    3. preencher o campo senha com senha válida.
    4. Clicar em entrar
- Dados de teste: E-mail: joao@exemplo.com; Senha: 12345678
- Resultado esperado: O sistema redireciona para o dashboard principal.
- Resultado obtido: [descrever após o teste]
- status: [descrever após o teste]
- Observações: [descrever após o teste, se necessário]
- Evidências: anexar apos o teste

---

## 5.3  Tipos de casos de testes

Existe diferentes formas de organizar os casos de teste:

1. Funcional
    - Validam funcionalidades do sistema.
    - Baseados em requisitos ou histórias de usuário

2. Não funcionais
    - Validam performance, segurança, usabilidade, confiabilidade.

3. Positivo e negativo
    - Positivo: test cenários corretos, onde tudo deveria funcionar.
    - Negativos: Tsta entradas incorretas e situações fora do padrão para garantoir que o sistema lide com erros corretamente.

4. Baseados em riscos
    - priorizam testes que podem causar mais impacto se falharem.

---

## 5.3 - Boas práticas de casos de teste

1. Seja claro e objetivo: Qualquer QA deve entender sem explicações claras.
2. Use uma lingauagem consistente: Nome completo, botões e tela devem ser iguais ao do sistema.
3. Evite ambiguidade: não escreva "verificar se funciona" escreva extamente o que deve acontecer.
4. Reutilize tampletes: manter uma padrão facilita a leitura e manutenção.
5. Atualize frequentimente: sistemas mudam, casos de teste tambem devem mudar.

---

## 5.4 - Ferramentas para casos de testes

Você pode documentar testes de forma manual, em planilhas ou usar ferramentas específicas de documentação de casos de testes. Exemplo:
1. Jira + Xray: vincula casos de teste a requisitos e histórias de usuário.
2. TestRail: gerencia casos de teste, executa e gera relatórios detalhados.
3. TestLink: ferramenta opensource para manter rastreabilidade.

---

## 5.5 - Conclusão do capítulo

Casos de teste são a base de qualquer trabalho de QA. Eles permitem que testes manuais sejam consistentes, rastreáveis e reproduzíveis. Com eles, qualquer equipe consegue validar requisitos, registrar resultados e oferecer dados confiáveis para melhora contínua do sistema.