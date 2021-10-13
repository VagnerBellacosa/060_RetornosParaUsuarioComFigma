# Tutorial do Diagrama de Sequência: Guia completo com exemplos

Atualizado em: 29 January 2021

Este tutorial de diagrama de seqüência é para ajudá-lo a entender melhor os diagramas de seqüência; para explicar tudo o que você precisa saber, desde como [desenhar um diagrama de seqüência](https://creately.com/diagram-type/sequence-diagram) até os erros comuns que você deve evitar ao desenhar um.

Existem 3 tipos de diagramas de interação; diagramas de seqüência, diagramas de comunicação, e diagramas de temporização. Estes diagramas são usados para ilustrar as interações entre as peças dentro de um sistema. Entre os três, os diagramas de seqüência são preferidos tanto pelos desenvolvedores quanto pelos leitores por sua simplicidade.

Neste tutorial de diagrama de seqüência você vai aprender sobre;

- [O que é um Diagrama de Sequência](https://creately.com/blog/pt/diagrama/tutorial-do-diagrama-de-sequencia/#Oquee)
- [Notas do Diagrama de Sequência](https://creately.com/blog/pt/diagrama/tutorial-do-diagrama-de-sequencia/#Notas)
- [Diagrama de Sequência Melhores Práticas](https://creately.com/blog/pt/diagrama/tutorial-do-diagrama-de-sequencia/#Melhor)
- [Como desenhar um diagrama de seqüência](https://creately.com/blog/pt/diagrama/tutorial-do-diagrama-de-sequencia/#Desenho)
- [Diagrama de Sequência Erros Comuns](https://creately.com/blog/pt/diagrama/tutorial-do-diagrama-de-sequencia/#Comum)
- [Modelos de Diagramas de Sequência e Exemplos](https://creately.com/blog/pt/diagrama/tutorial-do-diagrama-de-sequencia/#Modelos)
- [Tutorial do Diagrama de Sequência – Apresentação do SlideShare](https://creately.com/blog/pt/diagrama/tutorial-do-diagrama-de-sequencia/#SlideShare)
- [Feedback sobre o Tutorial do Diagrama de Sequência](https://creately.com/blog/pt/diagrama/tutorial-do-diagrama-de-sequencia/#Feedback)

### O que é um Diagrama de Sequência?

Os diagramas de seqüência, comumente usados pelos desenvolvedores, modelam as interações entre objetos em um único caso de uso. Eles ilustram como as diferentes partes de um sistema interagem entre si para realizar uma função, e a ordem em que as interações ocorrem quando um determinado caso de uso é executado.

Em palavras mais simples, um diagrama de seqüência mostra diferentes partes de um sistema trabalhando em uma ‘seqüência’ para se fazer algo.

### Notações do diagrama de sequência

Um diagrama de seqüência é estruturado de tal forma que representa uma linha de tempo que começa no topo e desce gradualmente para marcar a seqüência de interações. Cada objeto tem uma coluna e as mensagens trocadas entre eles são representadas por setas.

**Uma rápida visão geral das várias partes de um diagrama de sequência**

**Notação de linha de vida**![Diagrama de sequência - LifelineA](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Sequence-diagram-Lifeline.png)

Um diagrama de sequência é composto por várias dessas notações de linha de vida que devem ser organizadas horizontalmente na parte superior do diagrama. Duas notações de linha de vida não devem se sobrepor. Eles representam os diferentes objetos ou partes que interagem entre si no sistema durante a sequência.

Uma notação de linha de vida com um símbolo de elemento de ator é usada quando o diagrama de sequência específico pertence a um caso de uso.

![linha de vida com um símbolo de elemento de ator](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/lifeline-with-an-actor-element-symbol.png)

Uma linha de vida com um elemento de entidade representa os dados do sistema. Por exemplo, em uma aplicação de atendimento ao cliente, a entidade Cliente administraria todos os dados relacionados a um cliente.

![Linha de vida da entidade](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Entity-Lifeline.png)

Uma linha de vida com um elemento de fronteira indica um limite do sistema / elemento de software em um sistema; por exemplo, telas de interface do usuário, gateways de banco de dados ou menus com os quais os usuários interagem, são fronteiras.

![Linha de Vida Limite](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Boundary-Lifeline.png)

E uma linha de vida com um elemento de controlo indica uma entidade ou gestor de controlo. Ele organiza e programa as interações entre os limites e entidades e serve como mediador entre eles.

![img](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Control-Lifeline.png)

**Barras de Activação**

A barra de ativação é a caixa colocada na linha de vida. É usado para indicar que um objeto está ativo (ou instanciado) durante uma interação entre dois objetos. O comprimento do retângulo indica a duração dos objetos que permanecem ativos.

Em um diagrama de seqüência, uma interação entre dois objetos ocorre quando um objeto envia uma mensagem para outro. O uso da barra de ativação nas linhas de vida do chamador da mensagem (o objeto que envia a mensagem) e do receptor da mensagem (o objeto que recebe a mensagem) indica que ambos estão ativos/está instanciados durante a troca da mensagem.

![Diagrama de Sequência - Barras de Ativação](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Sequence-Diagram-Activation-Bars.png)

**Setas de Mensagem**

Uma seta do Chamador de Mensagem para o Receptor de Mensagem especifica uma mensagem em um diagrama de seqüência. Uma mensagem pode fluir em qualquer direção; da esquerda para a direita, da direita para a esquerda ou de volta para o próprio autor da mensagem. Enquanto você pode descrever a mensagem que está sendo enviada de um objeto para outro na seta, com diferentes pontas de seta você pode indicar o tipo de mensagem que está sendo enviada ou recebida.

A seta de mensagem vem com uma descrição, que é conhecida como uma assinatura de mensagem, sobre ela. O formato para esta assinatura de mensagem está abaixo. Todas as partes excepto o nome_da_mensagem são opcionais.

*atributo = nome_da_mensagem (argumentos): tipo_de_retorno*

- *Mensagem síncrona*

Como mostrado no exemplo das barras de ativação, uma mensagem síncrona é usada quando o remetente espera que o receptor processe a mensagem e retorne antes de continuar com outra mensagem. A ponta de seta usada para indicar este tipo de mensagem é sólida, como a que está abaixo.

![Seta de Mensagem Síncrona ](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Synchronous-Message.png)

- *Mensagem assíncrona*

Uma mensagem assíncrona é usada quando o chamador da mensagem não espera que o receptor processe a mensagem e volte antes de enviar outras mensagens para outros objetos dentro do sistema. A ponta de seta usada para mostrar este tipo de mensagem é uma seta de linha como mostrado no exemplo abaixo

![Exemplo de mensagem assíncrona](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Asynchronous-Message-example.png)

- *Mensagem de retorno*

Uma mensagem de retorno é usada para indicar que o receptor da mensagem terminou o processamento da mensagem e está devolvendo o controle para o autor da chamada da mensagem. As mensagens de retorno são peças opcionais de notação, para uma barra de ativação que é acionada por uma mensagem síncrona implica sempre uma mensagem de retorno.

Dica: Você pode evitar bagunçar seus diagramas minimizando o uso de mensagens de retorno, pois o valor de retorno pode ser especificado na própria seta da mensagem inicial.

![Exemplo de mensagem de retorno](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Return-Message-Example.png)

- *Mensagem de criação de participante*

Os objectos não vivem necessariamente durante toda a duração da sequência de eventos. Objetos ou participantes podem ser criados de acordo com a mensagem que está sendo enviada.

A notação “dropped participant box” pode ser usada quando você precisa mostrar que o participante em particular não existia até que a chamada de criação seja enviada. Se o participante criado faz algo imediatamente após criação, você deve adicionar uma caixa de ativação logo abaixo da caixa do participante.

![Exemplo de criação de participante](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Participant-creation-example.png)

- *Mensagem de destruição participante*

Da mesma forma, os participantes quando não são mais necessários também podem ser excluídos de um diagrama de seqüência. Isto é feito adicionando um ‘X’ no final da linha de vida do referido participante.

![Mensagem de Destruição da Participação](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Participation-Destruction-Message.png)

- *Mensagem reflexiva*

Quando um objeto envia uma mensagem para si mesmo, ele é chamado de mensagem reflexiva. É indicado com uma seta de mensagem que começa e termina na mesma linha de vida, como mostrado no exemplo abaixo.

![Mensagem reflexiva ](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Reflexive-message.png)

**Comente**

[os diagramas UML](https://creately.com/pt/lp/ferramenta-de-diagrama-uml/) geralmente permitem a anotação de comentários em todos os [tipos de diagramas UML](https://creately.com/blog/diagrams/uml-diagram-types-examples/). O objeto de comentário é um retângulo com um canto dobrado, como mostrado abaixo. O comentário pode ser ligado ao objeto relacionado com uma linha tracejada.

![Comente o exemplo do objeto](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Comment-object-example.png)

Nota: Veja o Diagrama de Sequência Melhores Práticas para aprender sobre fragmentos de sequência.

### Práticas recomendadas de diagrama de sequência

- ***\*Gerir interacções complexas com fragmentos de sequência\****

Um fragmento de sequência é representado como uma caixa que emoldura uma secção de interacções entre objectos (como mostrado nos exemplos abaixo) num diagrama de sequência.

É usado para mostrar interações complexas, como fluxos e loops alternativos de uma forma mais estruturada. No canto superior esquerdo do fragmento, encontra-se um operador. Este – o operador do fragmento – especifica que tipo de fragmento é.

*Alternativas*

O fragmento de combinação alternativa é usado quando é necessário fazer uma escolha entre duas ou mais sequências de mensagens. Ele modela a lógica do “if-then-else”.

O fragmento alternativo é representado por um grande retângulo ou um frame; ele é especificado mencionando ‘alt’ dentro da caixa de nome do frame (a.k.a. fragment operator).

Para mostrar duas ou mais alternativas, o retângulo maior é então dividido no que é chamado de operandos de interação usando uma linha tracejada, como mostrado no exemplo do diagrama de seqüência acima. Cada operando tem um guarda para testar e é colocado no canto superior esquerdo do operando.

![Exemplo de fragmento alternativo - tutorial diagrama de seqüência ](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Alternative-fragment-example-1.png)

*Opções*

O fragmento de combinação de opções é usado para indicar uma seqüência que só ocorrerá sob uma determinada condição, caso contrário, a seqüência não ocorrerá. Ele modela a afirmação “if-then”.

Similar ao fragmento alternativo, o fragmento de opção também é representado com uma moldura retangular onde ‘opt’ é colocado dentro da caixa de nome.

Ao contrário do fragmento alternativo, um fragmento de opção não é dividido em dois ou mais operandos. A proteção da opção é colocada no canto superior esquerdo.

*(Encontre um diagrama de seqüência de exemplo com um fragmento de opção na seção Modelos de Diagramas de Sequência e Exemplos).*

*Loops*

O fragmento de loop é usado para representar uma sequência repetitiva. Coloque as palavras ‘loop’ na caixa do nome e a condição de guarda perto do canto superior esquerdo do quadro.

Além do teste booleano, o guarda em um fragmento de laço pode ter duas outras condições especiais testadas contra. Estas são iterações mínimas (escritas como *minint = [o número]* e máximas (escritas como maxint = [o número]).

Se for uma proteção de iterações mínimas, o loop deve executar não menos que o número mencionado, e se for uma proteção de iterações máximas, o loop não deve executar mais do que o número indicado.

(Encontre um exemplo de um fragmento de laço abaixo nos modelos de diagrama de seqüência e na seção de exemplo)

*Fragmento de referência*

Você pode usar o fragmento de referência para gerenciar o tamanho de grandes diagramas de seqüência. Ele permite reutilizar parte de um diagrama de seqüência em outro, ou em outras palavras, você pode referenciar parte de um diagrama em outro diagrama usando o fragmento de ref.

Para especificar o fragmento de referência, você tem que mencionar ‘ref’ na caixa de nome do quadro e o nome do diagrama de seqüência que está sendo referido dentro do quadro.

![Exemplo de fragmento de referência](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Reference-fragment-example.png)

*Para mais fragmentos de seqüência, consulte* *Além do Básico de Diagramas de Sequência:* [*Parte 1*](https://creately.com/blog/diagrams/beyond-the-basics-of-sequence-diagrams-part-1/)*,* [*Parte 2*](https://creately.com/blog/diagrams/beyond-the-basics-of-sequence-diagrams-part-2/) *e* [*Parte 3*](https://creately.com/blog/diagrams/beyond-the-basics-of-sequence-diagrams-part-3/)*.*

- **Desenhe diagramas de seqüência menores que capturem a essência do caso de uso**

Em vez de bagunçar seu diagrama de seqüência com vários objetos e grupos de mensagens que irão confundir o leitor, desenhe alguns diagramas de sequência mais pequenos que expliquem adequadamente o que o seu sistema faz. Certifique-se de que o diagrama cabe em uma única página e deixe espaço para notas explicativas também.

Também em vez de desenhar dezenas de diagramas de seqüência, descubra o que é comum entre os cenários e concentre-se nisso. E se o código é expressivo e pode ficar por si só, não há necessidade de desenhar um diagrama de sequência em primeiro lugar.

### Como desenhar um diagrama de seqüência

Um [diagrama de seqüência](https://creately.com/pt/lp/sequencia-diagrama-em-linha) representa o cenário ou fluxo de eventos em um único caso de uso. O fluxo de mensagens do diagrama de seqüência é baseado na narrativa do caso particular de uso.

Em seguida, antes de começar a desenhar o diagrama de seqüência ou decidir quais interações devem ser incluídas nele, você precisa [desenhar o diagrama de caso de uso](https://creately.com/diagram-type/use-case) e pronto uma descrição abrangente do que o caso de uso particular, faz.

![Como desenhar um diagrama de seqüência Um diagrama de seqüência representa o cenário ou fluxo de eventos em um único caso de uso. O fluxo de mensagens do diagrama de seqüências é baseado na narrativa do caso de uso específico. Então, antes de começar a desenhar o diagrama de seqüência ou decidir quais interações devem ser incluídas nele, você precisa preparar uma descrição abrangente do que o caso de uso em particular faz. ](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Use-case-example.png)

A partir do exemplo de diagrama de caso de uso acima de ‘Create New Online Library Account’, vamos focar no caso de uso chamado ‘Create New User Account’ para desenhar o nosso exemplo de diagrama de sequência.

Antes de desenhar o diagrama de seqüência, é necessário identificar os objetos ou atores que estariam envolvidos na criação de uma nova conta de usuário. Estes seriam;

- Bibliotecário
- Sistema de Gestão de Bibliotecas Online
- Base de dados de credenciais do usuário
- Sistema de e-mail

Uma vez identificados os objetos, é então importante escrever uma descrição detalhada sobre o que o caso de uso faz. A partir desta descrição, você pode facilmente descobrir as interações (que devem ir no diagrama de seqüência) que ocorreriam entre os objetos acima, uma vez que o caso de uso é executado. Aqui estão as etapas que ocorrem no caso de uso chamado ‘Criar nova conta de usuário da biblioteca’.

- O bibliotecário solicita ao sistema a criação de uma nova conta de biblioteca online
- O bibliotecário então seleciona o tipo de conta de usuário da biblioteca
- O bibliotecário introduz os dados do utilizador
- Os detalhes do usuário são verificados usando o Banco de Dados de Credenciais do usuário
- A nova conta de usuário da biblioteca é criada
- Um resumo dos detalhes da nova conta é então enviado por e-mail para o usuário

A partir de cada uma destas etapas, você pode facilmente especificar quais mensagens devem ser trocadas entre os objetos no diagrama de seqüência. Quando estiver claro, você pode ir em frente e começar a desenhar o diagrama de seqüência. O diagrama de sequência abaixo mostra como os objectos no sistema de gestão de bibliotecas online interagem entre si para executar a função ‘Create New Library User Account’.

![Como desenhar um diagrama de sequência - tutorial do diagrama de sequência](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/How-to-draw-a-sequence-diagram.png)

### Diagrama de Sequência Erros Comuns

Ao desenhar diagramas de sequência, os desenhadores tendem a cometer estes erros comuns. Ao evitar estes erros, você pode garantir a qualidade do seu diagrama.

- A acrescentar demasiados detalhes. Isto desorganiza o diagrama e torna a leitura difícil.

- Diagramas de seqüência obsoletos e desatualizados que são irrelevantes quando comparados com as interfaces, arquiteturas reais, etc. do sistema. Não se esqueça de substituí-los ou modificá-los.

- Não deixando espaço em branco entre o texto do caso de uso e a seta de mensagem; isto dificulta a leitura do diagrama por qualquer pessoa.

- Não considerando cuidadosamente as origens das setas de mensagem.

Veja estes erros comuns explicados em detalhe no Guia do Diagrama de Sequência: [Erros comuns a evitar ao desenhar diagramas sequenciais](https://creately.com/blog/diagrams/10-common-mistakes-to-avoid-in-sequence-diagrams/).

### Modelos de Diagramas de Sequência e Exemplos

A seguir estão alguns [exemplos de diagramas de seqüência](https://creately.com/diagram-community/examples/t/sequence-diagram) e modelos que são desenhados usando Creately. [Crie diagramas de seqüência online](https://creately.com/diagram-type/sequence-diagram) usando a ferramenta online da Creately. Clique no modelo para abri-lo no editor.

*Diagrama de sequência de um sistema de exame online*

[![Exame Online - Modelo de Diagrama de Sequência](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/New-Online-Examination-Sequence-Diagram-Template.png)](https://creately.com/creately-start?tempID=imd2m8tw1)

Clique na imagem para editá-la online

*Diagrama de Sequência Exemplo de um Sistema de Gestão Escolar*[![Sistema de Gestão Escolar - Modelo de Diagrama de Sequência ](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/New-School-Management-System-Sequence-Diagram-Template-1.png)](https://creately.com/creately-start?tempID=imcvynir1)

*Exemplo de um fragmento de combinação de opções*[![Exemplo de um fragmento de opção](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/Example-of-an-option-fragment.png)](https://creately.com/creately-start?tempID=iy020p1n1)*Exemplo de uma sequência de loops*[![ Loops - Exemplo de Diagrama de Sequência](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2017/01/New-Loops-Sequence-Diagram-Example-1.png)](https://creately.com/creately-start?tempID=io1a1c3h1)*Aqui estão mais alguns* [*modelos de diagramas de seqüência e exemplos* ](https://creately.com/diagram-community/popular/t/sequence-diagram)*que você pode editar imediatamente.*

### Tutorial do Diagrama de Sequência – Apresentação do SlideShare



[Guia do diagrama de sequência Power Point (PPT)](https://www.slideshare.net/creately/the-ultimate-sequence-diagram-guide) do [Creately](https://www.slideshare.net/creately)

### Feedback sobre o Tutorial do Diagrama de Sequência

Este tutorial de diagrama de seqüência cobre tudo que você precisa saber sobre diagramas de seqüência e desenhá-los. Se você tiver alguma sugestão ou dúvida sobre o tutorial do diagrama de seqüência, sinta-se à vontade para deixar um comentário.