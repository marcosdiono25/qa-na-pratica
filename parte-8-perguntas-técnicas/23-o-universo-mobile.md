# 23 Perguntas e Respostas sobre Testes Mobile para Entrevistas de QA

## 1. Quais são os principais desafios em testes mobile em comparação aos testes web?
**Resposta:**  
A principal diferença está na complexidade do ecossistema mobile. No web, normalmente testamos em navegadores padronizados e com menos variações de hardware. Já no mobile, lidamos com fragmentação de dispositivos, múltiplos sistemas operacionais, versões diferentes e limitações físicas como bateria, memória e poder de processamento. Além disso, fatores como variação de rede (Wi-Fi, 4G, 5G, offline), sensores (GPS, giroscópio, câmera) e o contexto de uso (luz do sol, movimentação, multitarefa) afetam diretamente a experiência. Por isso, o teste mobile exige um olhar mais amplo e um planejamento muito bem alinhado com o perfil real do usuário.

---

## 2. Como você lida com a fragmentação de dispositivos no Android e iOS?
**Resposta:**  
Eu começo estudando dados reais de uso — seja via Google Analytics, Firebase ou ferramentas internas da empresa — para entender quais dispositivos, resoluções e versões de sistema são mais usados pelo nosso público. Com essa matriz em mãos, defino um conjunto prioritário de dispositivos para testes manuais e automatizados.  
No caso do Android, priorizo modelos que representem diferentes tamanhos de tela, fabricantes e versões do sistema. No iOS, normalmente foco nas duas ou três versões mais recentes do iOS e modelos de iPhone com tamanhos de tela distintos. Também complemento com emuladores e simuladores para cenários menos críticos, mas que ajudam a ampliar a cobertura.

---

## 3. Quais tipos de testes são críticos para garantir a qualidade de um aplicativo mobile?
**Resposta:**  
Um app mobile de qualidade depende de múltiplas camadas de teste:  
- **Funcionais:** Confirmar que cada funcionalidade faz exatamente o que foi especificado.  
- **Usabilidade:** Garantir que a navegação seja intuitiva, fluida e adaptada ao contexto de uso.  
- **Performance:** Medir tempo de resposta, consumo de memória, FPS e uso de bateria.  
- **Segurança:** Validar criptografia de dados, permissões e prevenção de ataques como man-in-the-middle.  
- **Compatibilidade:** Testar em diferentes versões de SO, dispositivos e tamanhos de tela.  
- **Conectividade:** Verificar funcionamento em Wi-Fi, 4G/5G, modo avião e cenários offline.  
Essa combinação garante que o aplicativo não só funcione, mas funcione bem e de forma consistente.

---

## 4. Você prefere testar em dispositivos reais ou em emuladores/simuladores? Por quê?
**Resposta:**  
Eu defendo uma abordagem híbrida. Emuladores e simuladores são excelentes para o desenvolvimento inicial e testes automatizados, pois oferecem velocidade, custo reduzido e fácil configuração. Porém, eles não simulam fielmente condições reais, como atraso de rede, consumo de bateria, resposta dos sensores e performance sob carga real.  
Por isso, para validação final e testes de usabilidade, desempenho e recursos nativos, sempre uso dispositivos reais. É neles que o usuário final vai interagir, então precisamos garantir que a experiência real seja satisfatória.

---

## 5. Como você valida a usabilidade de um aplicativo mobile?
**Resposta:**  
Valido usabilidade a partir de três frentes:  
1. **Testes exploratórios:** Caminho pelo app como se fosse um usuário comum, buscando fricções, fluxos confusos ou excesso de cliques para tarefas simples.  
2. **Feedback real:** Envolvo beta testers ou grupos de usuários representativos para coletar impressões autênticas.  
3. **Guias oficiais:** Comparo com boas práticas do Material Design (Android) e Human Interface Guidelines (iOS) para garantir consistência visual e interação padronizada.  
Além disso, considero o contexto: um aplicativo que será usado na rua precisa ter botões maiores e menos dependência de digitação, por exemplo.

---

## 6. Como você realiza testes de conectividade e cenários offline?
**Resposta:**  
Testo conectividade simulando mudanças de rede durante o uso — por exemplo, iniciar no Wi-Fi, mudar para 4G e depois forçar modo avião. Avalio se as ações pendentes são salvas localmente e sincronizadas corretamente quando a conexão retorna.  
Também verifico como o app informa o usuário sobre perda de conexão. Uma boa experiência não apenas funciona offline quando possível, mas também comunica de forma clara quando algo não pode ser feito.

---

## 7. Como você realiza testes de performance em mobile?
**Resposta:**  
Uso ferramentas como Android Profiler, Xcode Instruments e Firebase Performance para monitorar tempo de inicialização, FPS, uso de CPU, memória e bateria.  
Executo testes repetidos em diferentes dispositivos para identificar padrões e gargalos. Também testo sob condições adversas — como baixo espaço de armazenamento ou várias apps abertas — porque é assim que muitos usuários reais operam o celular.  
O objetivo é entregar um aplicativo rápido, estável e eficiente mesmo em cenários menos ideais.

---

## 8. Quais são as boas práticas para automatizar testes mobile?
**Resposta:**  
- **Escolha correta da ferramenta:** Appium para testes cross-platform, Espresso e XCUITest para nativos.  
- **Scripts modulares:** Evitar código duplicado e facilitar manutenção.  
- **Integração contínua:** Executar testes automaticamente a cada build.  
- **Cobertura equilibrada:** Automatizar o que é estável e repetitivo, mas manter testes manuais para cenários exploratórios.  
- **Ambientes realistas:** Executar automação também em dispositivos físicos via serviços como BrowserStack.  
Seguindo essas práticas, a automação se torna uma aliada real e não apenas um gargalo de manutenção.

---

## 9. Como você testa permissões e integrações com recursos nativos (GPS, câmera, notificações)?
**Resposta:**  
Crio cenários positivos e negativos: aceitando e negando permissões durante o uso e via configurações do sistema.  
Valido como o app reage quando um recurso está indisponível — por exemplo, GPS desligado, câmera em uso por outro app, notificações bloqueadas.  
Também testo casos de reautorização, para garantir que a experiência seja fluida quando o usuário mudar as permissões depois da instalação.

---

## 10. Qual a importância de testar atualizações de aplicativos mobile?
**Resposta:**  
Muitas vezes o usuário não instala o app do zero — ele apenas atualiza. Isso significa que dados antigos, configurações salvas e permissões pré-existentes precisam funcionar perfeitamente após a atualização.  
Testar esse cenário evita problemas de migração de banco de dados, incompatibilidades de versão e falhas que só ocorrem em upgrades. É uma prática essencial para garantir que cada nova versão seja bem recebida e não gere frustração.
