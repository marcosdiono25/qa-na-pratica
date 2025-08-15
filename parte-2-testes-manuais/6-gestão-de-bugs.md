# CAPÍTULO 6 - GESTÃO DE BUGS

Encontrar um bug é apenas o começo. A parte mais importante do trabalho de um QA é como registrar, comunicar e acompanhar esse problema, garantindo que ele seja resolvido da maneira correta.  
Este capítulo vai mostrar como registrar bugs de forma eficiente, transformando cada erro em uma oportunidade para melhoria do sistema. 

---

## 6.1 - O que é um bug

Um bug é qualquer comportamento do sistema que se desvia do esperado.  
Pode ser causado por erro no desenvolvimento, falha de requisito, má comunicação ou cenário não previsto.

**Exemplos de bugs comuns:**
- Botões que não funcionam  
- Campos que aceitam valores inválidos  
- Erros de cálculo ou exibição de informação  
- Quebra de layout em telas específicas  

> **Lembre-se:** bug não é culpa de ninguém individualmente; é um sintoma do sistema que precisa ser corrigido.

---

## 6.2 - Ciclo de vida de um bug

Todo bug possui um ciclo de vida até ser resolvido. Entender esse ciclo ajuda a acompanhar e priorizar correções.

1. **Novo:** bug encontrado e registrado pelo QA.  
2. **Aberto:** bug confirmado e aguardando análise do time de desenvolvimento.  
3. **Em progresso:** bug está sendo corrigido.  
4. **Resolvido / pronto para teste:** desenvolvedor corrigiu e está aguardando validação do QA.  
5. **Fechado:** QA validou a correção e o bug não ocorreu novamente.  
6. **Reaberto:** o bug reapareceu ou não foi corrigido corretamente.

---

## 6.3 - Como registrar um bug

Um bug precisa ser claro e rastreável.  
Os principais campos de registro incluem:

1. **ID do bug:** identificador único. Ex.: BUG-001  
2. **Título:** descrição resumida do problema  
3. **Descrição detalhada:** explicação clara do que aconteceu  
4. **Passos para reproduzir:** instruções que permitam ao desenvolvedor replicar o bug  
5. **Resultado esperado:** como o sistema deveria se comportar  
6. **Resultado real:** o que de fato ocorreu  
7. **Severidade:** impacto do bug (Crítico, Alto, Médio ou Baixo)  
8. **Prioridade:** urgência da correção (Alta, Média ou Baixa)  
9. **Ambiente:** navegador, sistema operacional, versão do sistema  
10. **Evidências:** vídeos ou capturas de tela que comprovem o bug

---

## 6.4 - Exemplo de bug documentado

**ID:** BUG-001  
**Título:** Botão "Enviar" permanece desabilitado no login  

**Descrição:**  
Ao acessar a página de login, mesmo preenchendo corretamente os campos **"E-mail"** e **"Senha"** com informações válidas, o botão **"Enviar"** permanece desabilitado, impedindo o usuário de acessar as funcionalidades do sistema.

**Passos para reproduzir:**  
1. Acessar a página de login  
2. Inserir no campo **E-mail**: `joaodostestes@exemplo.com`  
3. Inserir no campo **Senha**: `12345678admin`  
4. Tentar clicar no botão **"Enviar"**  

**Resultado esperado:**  
O botão **"Enviar"** deve ser habilitado e, ao clicar, o usuário deve ser redirecionado para a **Tela Home**.

**Resultado real:**  
O botão **"Enviar"** permanece desabilitado, impedindo o acesso ao sistema.

**Severidade:** Crítico  
**Prioridade:** Alta  

**Ambiente:**  
- Navegador: Chrome  
- Versão: 126  
- Sistema: Windows 10  

**Evidências:** Anexar capturas de tela ou vídeo.

---

## 6.5 - Boas práticas na gestão de bugs

1. **Seja objetivo e factual:** evite opiniões ou julgamentos pessoais.  
2. **Priorize corretamente:** bugs críticos que afetam usuários devem ser tratados primeiro.  
3. **Use ferramentas de rastreabilidade:** Jira, Trello, Redmine ou TestRail ajudam no acompanhamento.  
4. **Comunique-se com o time:** descreva claramente o problema e esteja disponível para esclarecimentos.  
5. **Valide a correção:** nunca feche um bug sem testar a solução.

---

## 6.6 - Conclusão do capítulo

A gestão de bugs é tão importante quanto encontrá-los.  
Um QA eficiente sabe registrar, acompanhar e priorizar cada problema, garantindo que o software entregue qualidade e confiabilidade ao usuário final.
