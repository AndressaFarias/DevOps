# U-Curve

Essa é uma lava louça DevOps – e por quê as U-Curve são importantes para você 

Publicado 12 de agosto de 2019 por Brian Kelly 

 

Introdução U-Curve 

Teoria descrita no livro de Donald G. Reinertsen The Principles of Product Development Flow (Os princípios do fluo de desenvolvimento de produtos). 

 

 

U-Curve é quando são combinados os custos de não fazer algo (para acumular mais tarefas da mesma natureza) com o custo de realmente fazer a tarefa. É usado para encontrar o tamanho ideal de lote para itens de trabalho. 

A U-Curve para lavar louça manualmente. 

Os custos para lavar a louça a moda antiga, para lavar completamente um único prato, precisamos: 

A tarefa que estava sendo executada deve ser interrompida e então optamos por lavar os pratos; 

Pegar água quente, detergente e pano-de-prato; 

Esfregar o prato com água e sabão; 

Enxague o prato limpo; 

Seque o prato com o pano-de-prato. 

Este conjunto de tarefas representa o Transaction Cost (custo de transação) para lavar a louça manualmente. Se você lava apenas um prato ou todo os pratos de sua cozinha, as mesmas tarefas são necessárias. A principal diferença é o número de pratos que você limpa de cada vez, chamado de batch size (tamanho do lote). 

Como levaria muitos minutos para lavar um único prato, torna-se ineficiente fazer a limpeza a cada prato sujo, então deixamos acumular alguns pratos e fazemos a limpeza quando tiver uma quantidade maior. 

 

O gráfico acima ilustra o custo de lavar a louça na pia (o custo da transação, em vermelho) e o custo de manutenção (o custo da louça se acumulando, em cinza). A curva de custo geral (em roxo) é criada adicionando o custo da transação e mantendo os valores de custo juntos, e cria um gráfico em formato de "U". O tamanho ideal do lote para lavar a louça à mão é, portanto, onde o "U" está no seu ponto mais baixo. 

Otimizando a lavagem de ouça manual 

Se a louça é lavada uma de cada vez, o transaction cost (custo da transação) é muito alto, pois há muita preparação e trabalho necessários para cada lavagem. 

Se esperarmos até o final da semana para fazer alguma coisa, o custo da transação cairá substancialmente, pois não passaremos uma semana inteira lavando pratos. No entanto, muitos pratos se acumulam e isso acarreta um alto custo de manutenção (holding cot - poucos pratos limpos estão disponíveis, a cozinha parece bagunçada, há menos espaço livre no balcão para a preparação de alimentos etc.). 

Os seres humanos são realmente muito bons em otimizar inconscientemente o custo geral em um sistema como este. Eles criam rotinas de lavagem de pratos que equilibram o custo transacional de lavá-los com os efeitos negativos de deixar uma pilha de pratos sujos na pia da cozinha. 

O melhor que um humano com um pano de prato e sabão em suas mãos pode esperar, no entanto, é operar no ponto mais baixo da curva em U existente. Em outras palavras, eles não podem reduzir radicalmente seus custos gerais sem alterar fundamentalmente o sistema. 

Lavagem de Louça Manual e ... hum... Software. 

Prometi vincular essa analogia ao software e ao DevOps. Veja como cada conceito de lavar pratos se traduz em tecnologia: 

Pratos sujos: novos recursos e correções do produto que foram codificados, mas ainda não foram liberados (release); 

Pratos limpos: novos recursos e correções do produto que foram liberados e estão nas mãos dos usuários; 

Custo de transação: o processo usado para criar uma versão de software e implantá-la em produção; 

Custo de manutenção (holding cost): o custo de não receber feedback dos usuários sobre novos recursos, mantendo código não liberado (e potencialmente não muito valioso), sem saber se os recursos realmente funcionarão em produção etc. 

No mundo do software, lavar a louça manualmente é como liberar produtos usando esforço humano e automação mínima. Executar build manualmente; implantar alterações de infraestrutura efetuando login diretamente nos servidores e digitando comandos; compilação manual de entradas do ChangeLog e assim por diante: esses são os equivalentes de software de “lavar a louça manualmente”. 

Por que as filas são realmente más 

Uma grande pilha de louça suja representa uma fila crescente. Em qualquer sistema - seja ele informatizado ou humano - as filas são inimigas do fluxo saudável. As filas aumentam rapidamente os atrasos na entrega e são indicadores iniciais de problemas futuros de desempenho. Elas também inibem loops de feedback . 

Infelizmente, longas filas também causam comportamentos improdutivos em humanos. Quanto mais a fila cresce, mais difícil fica a argumentação e mais sentimentos negativos podem ser criados. Grite para os engenheiros de controle de qualidade encarregados de testar uma nova versão de seu produto no mercado depois de anos de desenvolvimento: "Não consigo acompanhar todas as alterações que temos que testar nesta versão imensa!" 

Filas longas fazem com que os humanos temam gradualmente as transações necessárias para reduzir seu comprimento, o que leva ao adiamento das transações, o que leva a uma fila cada vez maior. Em termos de lavagem de louça, uma enorme pilha de louça suja faz com que as pessoas evitem gastar uma ou duas horas necessárias para limpá-las. 

Filas longas (ou grandes pilhas de pratos) também tendem a aumentar a importância cerimonial das transações. À medida que o medo de grandes transações aumenta, tendemos a criar rotinas e tradições para acomodar o risco, o tempo e o esforço incorridos, permitindo que essas filas aumentem. Começamos a atender às necessidades da transação e não às necessidades de nossos usuários. 

Por exemplo, assim como as pessoas que habitualmente deixam muita louça se acumular podem nomear uma manhã de fim de semana como seu "horário semanal de lavar louça", uma equipe com processos complicados de liberação manual pode facilmente criar um cronograma de liberação deliberadamente infrequente com ainda mais  manuais e processos baseado em humanos, perpetuando a situação atual e codificando-a na cultura de sua equipe. 

Com um processo totalmente manual, os humanos tendem a avançar ainda mais na U-Curve, executando transações com menos frequência e levando a lotes cada vez maiores. Quando você ouvir frases como "Não inicie a grande fase de testes por mais um dia, porque há mais uma correção de erro que gostaríamos de fazer primeiro ...", você está testemunhando esse fenômeno em ação. 

Introdução à automação: a máquina de lavar louça clássica 

O uso de máquina de lavar não são a otimização definitiva para o nosso problema de louça suja.  É provável que o tamanho do lote esteja próximo ao ponto ideal na parte inferior da U-Curve. 

Como o uso da máquina de lavar faz isso? 

O medo da transação é drasticamente reduzido:  para um ser humano o esforço para preencher uma máquina de lava-louça para lavar uma única peça ou sua capacidade máxima, exige o mesmo esforço. Isso faz com que seja executado com mais frequência, diminuindo o tamanho do lote, reduzindo o custo geral. 

Custo da transação é óbvio: É improvável que uma máquina de lavar louça opere com apena um prato ou com sua capacidade máxima. É mais conveniente executá-la quando estiver quase cheia. 

Embora o custo de transação seja alto, várias horas para um ciclo completo, os seres humanos estão liberados enquanto a máquina está executando sua função. Isso elimina o custo de oportunidade associado à lavagem manual da louça. 

Tamanho do lote é limitado (Batch size is limited): Só é possível colocar tantos pratos quantos forem a capacidade da máquina. 

Risco de quebras é reduzido: É mais provável que você derrube e quebre a louça ao lavar à mão. Uma máquina de lavar louça reduz muito esse risco. 

 

 

Máquinas de Lavar Louça e Software 

Em termos de software, introduzir uma máquina de lavar louça na cozinha é como automatizar algumas partes de um processo de liberação que eram manuais e propensas a erros do operador, mas mantendo as mesmas etapas básicas de antes. 

Isso faz com que a frequência de liberações de produtos aumente o suficiente para que o tamanho do lote se torne ideal, mas as linhas e curvas no gráfico permanecem as mesmas. Em outras palavras, é como automatizar o suficiente para tornar as versões menos assustadoras, mas sem realmente mover a agulha de otimização . 

É aí que o DevOps entra. 

 

Apresentando: A máquina de lavar louça DevOps 

Existe uma utopia de lavar louça que podemos alcançar, onde: 

Os pratos nunca se acumulam; 

Os pratos são limpos assim que estão sujos; 

Nunca nos preocupamos com o esforço necessário para lavar a louça; 

Não precisamos otimizar o número de pratos a serem limpos de cada vez; 

A lavagem da louça se torna um processo invisível e automático que nos libera para focar em outras coisas. 

Podemos alcançar essa grande visão da cozinha com um uso inteligente da tecnologia e focando essa tecnologia em fornecer de forma confiável o que mais valorizamos: um fluxo constante de pratos limpos 

 

Para isso, construímos uma nova máquina de lavar louça robótica que opera de maneira muito diferente das tradicionais: sempre tem água quente e sabão prontos, pega a louça suja assim que aparecem na pia, limpa e seca rapidamente, e finalmente, coloca-os no lugar correto na prateleira. 

Se muitos pratos sujos aparecerem de uma só vez, um pequeno exército de nossas novas máquinas de lavar louça robóticas aparece magicamente, e cada uma pega um prato e limpa a pilha inteira simultaneamente. Pratos sujos nunca se acumulam e pratos limpos voltam às prateleiras quase que imediatamente. 

Ao investir nessa tecnologia para alterar a forma como a louça é limpa, nossa curva de transações cai significativamente e, portanto , alteramos radicalmente o formato da nossa U-Curve para lavar a louça para tornar o ponto mais baixo (o mais ideal) ainda mais baixo, além de reduzir o tamanho do lote necessário para alcançar essas economias de custo. 

 

Building de uma Máquina de Lavar Louça DevOps 

Qual é o equivalente em software deste maravilhoso nirvana para lavar louça? É composto de várias partes: DevOps , CI / CD , pipelines , desenvolvimento baseado em tronco , mapeamento de fluxo de valor , infraestrutura como código e muito mais. É o conjunto de itens necessários para que as alterações sejam feitas na base de código do produto e nas mãos dos usuários assim que estiverem prontos: 

Uma equipe que entrega pequenos trechos de trabalho com muita frequência e evita filiais de longa duração; 

Um sistema de integração contínua (CI) confiável e escalável que cria e testa automaticamente qualquer nova alteração de código; 

Testes automatizados, rápidos, confiáveis e com cobertura suficiente; 

Um sistema de entrega contínua (CD) que obtém automaticamente o novo código em execução em produção; 

Infraestrutura elástica, programável e confiável; 

Equipes de desenvolvedores e operadores que colaboram efetivamente e concordam em como manter todo o sistema - e o produto implementado - íntegro e responsivo 

Independentemente dos termos que você pode usar para descrever todas as opções acima (vamos agrupá-las todas sob o termo "DevOps" por enquanto), elas são o equivalente em software da nossa incrível máquina de lavar louça robótica. Usados adequadamente, eles levam a pequenos lotes, filas insignificantes e um custo geral bastante reduzido. 

A implantação de pequenas alterações com frequência também é uma excelente maneira de reduzir o risco de quebras em produção. Quantos erros podem ocultar dentro de 10 linhas de código? E com cerca de 10.000? A probabilidade de ocorrência de problemas aumenta drasticamente à medida que o tamanho dos lotes aumenta, portanto, adotar uma abordagem de implantação de pequenos lotes de alta frequência é um modelo muito mais seguro do que tentar liberar muitos meses de alterações de uma só vez. 

Por fim, pequenas alterações em lotes e implantações de alta frequência também são um indicador muito preciso de equipes de alto desempenho; 

 

Vá em frente e construa essas máquinas de lavar louça 

Agora que você está armado com o entendimento da U-Curve e as relações econômicas entre tamanho de lote, custo de transação, custo de manutenção e risco, pode até começar a ver as U-Curves aparecerem em outras áreas de sua vida e trabalho. 

E talvez na próxima vez em que você esteja em uma reunião de equipe decidindo quando liberar manualmente uma tonelada de recursos que estão na fila há semanas, imagine grandes pilhas de louça suja em uma pia e comece a inventar maneiras incríveis de lavá-las. 

 

 