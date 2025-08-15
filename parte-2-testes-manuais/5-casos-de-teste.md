# CAPÍTULO 5 - CASOS DE TESTE

Depois de aprender a desenhar e planejar nossos testes, o próximo passo é aprender a documentá-los de forma organizada. É aqui que entram os casos de teste, a espinha dorsal da vida de um QA. Um caso de teste bem escrito garante que qualquer QA possa reproduzir o teste, verificar resultados e registrar problemas sem ambiguidades. Além disso, ele ajuda a manter a rastreabilidade com os requisitos do sistema, algo essencial para garantir a qualidade do software.

---

## 5.1 - O que é caso de teste

Um caso de teste é uma descrição detalhada de uma ação ou conjunto de ações que devem ser executadas para garantir que um requisito está sendo cumprido.  

**Elementos principais de um caso de teste:**
1. **ID do caso de teste:** um identificador único de cada caso de teste, ex.: CT-001.  
2. **Título:** descreve de forma resumida o que será testado.  
3. **Requisito vinculado:** qual requisito está sendo validado.  
4. **Pré-condições:** o que precisa estar preparado antes do teste.  
5. **Passos de execução:** instruções detalhadas de como realizar o teste.  
6. **Dados de teste:** valores ou arquivos que serão usados.  
7. **Resultado esperado:** o comportamento correto do sistema.  
8. **Resultado obtido:** o resultado verificado após realizar o teste.  
9. **Status:** Passou/Falhou/Bloqueou  
10. **Observações:** notas adicionais, como problemas ou exceções encontradas.  
11. **Evidências:** fotos ou vídeos que comprovem o resultado obtido.  

---

## 5.2 - Um exemplo de caso de teste

Imagine que iremos testar a funcionalidade de login de uma página. Um exemplo de caso de teste poderia ser:

- **ID:** CT-001  
- **Título:** Login com usuário válido  
- **Requisito:** RF-001  
- **Pré-condições:** Usuário já cadastrado e ativo.  
- **Passos de execução:**  
    1. Acessar a página de login  
    2. Preencher o campo email com dados válidos  
    3. Preencher o campo senha com senha válida  
    4. Clicar em entrar  
- **Dados de teste:** E-mail: joao@exemplo.com; Senha: 12345678  
- **Resultado esperado:** O sistema redireciona para o dashboard principal.  
- **Resultado obtido:** [descrever após o teste]  
- **Status:** [descrever após o teste]  
- **Observações:** [descrever após o teste, se necessário]  
- **Evidências:** anexar após o teste  

---

## 5.3 - Tipos de casos de teste

Existem diferentes formas de organizar os casos de teste:

1. **Funcional**  
    - Validam funcionalidades do sistema.  
    - Baseados em requisitos ou histórias de usuário  

2. **Não funcionais**  
    - Validam performance, segurança, usabilidade, confiabilidade  

3. **Positivo e negativo**  
    - Positivo: testa cenários corretos, onde tudo deveria funcionar  
    - Negativo: testa entradas incorretas e situações fora do padrão para garantir que o sistema lide com erros corretamente  

4. **Baseados em riscos**  
    - Priorizam testes que podem causar mais impacto se falharem  

---

## 5.4 - Boas práticas de casos de teste

1. **Seja claro e objetivo:** qualquer QA deve entender o teste sem explicações adicionais  
2. **Use uma linguagem consistente:** nomes completos, botões e telas devem ser iguais aos do sistema  
3. **Evite ambiguidade:** não escreva "verificar se funciona"; escreva exatamente o que deve acontecer  
4. **Reutilize templates:** manter um padrão facilita a leitura e manutenção  
5. **Atualize frequentemente:** sistemas mudam, e casos de teste também devem mudar  

---

## 5.5 - Ferramentas para casos de teste

Você pode documentar testes de forma manual, em planilhas ou usar ferramentas específicas de documentação de casos de teste. Exemplo:  

1. **Jira + Xray:** vincula casos de teste a requisitos e histórias de usuário  
2. **TestRail:** gerencia casos de teste, executa e gera relatórios detalhados  
3. **TestLink:** ferramenta open source para manter rastreabilidade  

---

## 5.6 - Conclusão do capítulo

Casos de teste são a base de qualquer trabalho de QA. Eles permitem que testes manuais sejam consistentes, rastreáveis e reproduzíveis. Com eles, qualquer equipe consegue validar requisitos, registrar resultados e oferecer dados confiáveis para a melhoria contínua do sistema.
