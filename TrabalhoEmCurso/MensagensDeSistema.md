# Mensagens de Sistema

[By **Plínio Ventura**](https://www.ateomomento.com.br/author/plinio-ventura/) On **7 jul, 2015** Last updated **3 jan, 2021** [ 11](https://www.ateomomento.com.br/mensagens-de-sistema/#comments)

 **Share**

![Mensagens de Sistema](https://www.ateomomento.com.br/wp-content/uploads/2015/01/relacionaneto-dependencia-entre-classes-erro-compilacao-visual-studio.png)

Mensagens de sistema é algo **extremamente importante**, mas quase sempre relegado a “perfumaria”.

Do ponto de vista de orientação do usuário e até mesmo do desenvolvedor, é uma bussola!

## Placas de Trânsito

Imagine-se dirigindo um carro numa rodovia e em três placas de sinalização ha os seguintes dizeres: “Para retornar vire ao lado”, “Proibido andar muito rápido, sujeito a multa” e “Belo Horizonte – quase chegando”. São orientações, sim, mas da forma como estão escritas **elas instruem mais ou confundem mais?**

![placa-transito](https://www.ateomomento.com.br/wp-content/uploads/2015/07/placa-transito.jpg)

Rapidamente, vamos analisar cada uma das mensagens:

- “Para retornar vire ao lado”: qual lado (direita ou esquerda)?
- “Proibido andar muito rápido, sujeito a multa”: quanto é “muito rápido” (80 km ou 110 km, por exemplo)?
- “Belo Horizonte – quase chegando”: quanto é “quase chegando” (50 km ou 100 km, por exemplo)?





Vamos considerar, após reavaliação, uma nova versão de cada uma das orientações das placas:

- “Para retornar vire à esquerda”
- “Velocidade máxima: 80 km/h. Fiscalização eletrônica”
- “Belo Horizonte – 100 km”

Alguma dúvida sobre a clareza das mensagens após a reavaliação? É notório o quanto a segunda versão de cada placa/mensagem é mais clara que a primeira.

## Mensagens de Sistema

Em software o uso de mensagens incoerentes e nebulosas é algo (infelizmente) muito comum, que gera duras consequências **no dia a dia dos usuários e profissionais de TI** envolvidos no uso e suporte às aplicações.

Mensagens como “Ocorreu um erro e o sistema será encerrado”, “Registro inválido”, “Erro fatal. Acione o suporte do sistema” ou “STOP 0xC000021A” são encontradas todos os dias.

As mensagens de um software **são avisos com o objetivo de orientar o usuário sobre algo que ocorreu**, para que **alguma ação** seja tomada (e preferencialmente, com um indicativo de qual ação deve ser tomada).

Sendo assim, clareza, detalhamento e objetividade são fundamentais para mensagens que mostrem corretamente o que houve.





## **Tipos de Mensagem**

Existem alguns tipos de mensagens utilizadas, mas abordarei os quatro que considero mais importantes e quase que unicamente utilizados: **Alerta, Erro, Informação** e **Confirmação.**

### **Alerta**

Serve para alertar o usuário sobre algo que ocorreu, que não está previsto no [Fluxo Principal](https://www.ateomomento.com.br/caso-de-uso-fluxo-principal/) mas estava previsto num [Fluxo Alternativo](https://www.ateomomento.com.br/caso-de-uso-fluxo-alternativo/). Previsto significa contemplado pelo negócio realizado pelo software, como um **resultado da realização de uma regra de negócio**. Erro e Alerta são tipos de mensagem diferentes.

Uma mensagem como “*Não foi possível realizar o cálculo do valor da compra pois não foi informado o número do cartão de crédito. Para compras com este meio de pagamento o número do cartão é obrigatório.*” trata-se de uma exceção “de negócio” – para uma compra com cartão a regra de negócio define a obrigatoriedade dos dados do cartão. Mas não é uma “exception” de software, não é um erro do sistema, é uma exceção num cenário de negócio, **prevista pelo negócio**.

Tradicionalmente utiliza-se o **ícone de um triangulo amarelo com um ponto de exclamação dentro**.

![Mensagens de Sistema - Alerta](https://www.ateomomento.com.br/wp-content/uploads/2015/05/mensagem-sistema-alerta.png)

### **Erro**

Serve para alertar o usuário sobre algo que ocorreu, que não está previsto no [Fluxo Principal](https://www.ateomomento.com.br/caso-de-uso-fluxo-principal/) mas pode estar previsto num [Fluxo de Exceção](https://www.ateomomento.com.br/caso-de-uso-fluxo-de-excecao/).

Uma mensagem como “*Ocorreu um problema ao realizar o login no sistema. O sistema de segurança detectou uma anomalia no usuário e senha informados e não é possível realizar a autenticação. Procure com urgência o departamento de segurança.*” trata-se de uma exceção no sistema, algo não previsto em qualquer cenário. Se fosse algo como “usuário ou senha inválidos”, “login expirado”, “usuário bloqueado” não seria um erro, seria um alerta, pois são situações contempladas no negócio.

Ou seja, algo está errado mesmo, não é uma exceção prevista que realizou-se.

Tradicionalmente utiliza-se o ícone de um **círculo vermelho com um “x” dentro**.

![Mensagens de Sistema - Erro](https://www.ateomomento.com.br/wp-content/uploads/2015/05/mensagem-sistema-erro.png)

### **Informação**

Serve para informar o usuário sobre algo que ocorreu, que está previsto no [Fluxo Principal](https://www.ateomomento.com.br/caso-de-uso-fluxo-principal/) ou num [Fluxo Alternativo](https://www.ateomomento.com.br/caso-de-uso-fluxo-alternativo/). É como um status de algo que ocorreu, de caráter informativo apenas.

Uma mensagem como “*A compra foi realizada com sucesso e sua nota fiscal foi enviada para o e-mail informado no cadastro. Agradecemos a preferência e estamos à disposição para realizar um excelente pós-venda a você.*” trata-se de algo dentro da normalidade, previsto pelo negócio.

Tradicionalmente utiliza-se o **ícone de um círculo azul com um ponto de exclamação dentro**.

![Mensagens de Sistema - Informação](https://www.ateomomento.com.br/wp-content/uploads/2015/05/mensagem-sistema-informacao.png)

### **Confirmação**

Serve para questionar o usuário sobre alguma **decisão a ser tomada** na operação do sistema, que está previsto no [Fluxo Principal](https://www.ateomomento.com.br/caso-de-uso-fluxo-principal/) ou num [Fluxo Alternativo](https://www.ateomomento.com.br/caso-de-uso-fluxo-alternativo/). Geralmente utiliza opções como “Sim” (confirma a ação), “Não” (não confirma a ação) e “Cancelar” (retorna o estado anterior à geração da mensagem), mas pode ter outros comandos.

Uma mensagem como “*Deseja realmente cancelar sua conta de usuário e não mais ser usuário do nosso serviço de e-mail?*” trata-se de algo dentro da normalidade, previsto pelo negócio, mas que a partir da decisão tomada pelo usuário poderá acontecer mais de uma coisa.

Tradicionalmente utiliza-se o **ícone de um círculo azul (ou um “balão”) com um ponto de interrogação dentro**.

![Mensagens de Sistema - Confirmação](https://www.ateomomento.com.br/wp-content/uploads/2015/05/mensagem-sistema-confirmacao.png)

As mensagens de **Alerta, Erro** e **Informação** estão ilustradas em caixas de mensagem, pois estão sendo utilizadas num software com interface gráfica.

É importante ficar claro que as mesmas mensagens destes três tipos **podem ser utilizadas em logs do sistema** ou então em **execução via linha de comando**, caso seja pertinente. As de **Confirmação**, obviamente não se aplicam a logs, mas se aplicam também à execução via linha de comando.





## Mensagens ruins são bugs

A seguir, um quadro contido no livro [Software Testing](https://www.amazon.com/Software-Testing-2nd-Ron-Patton/dp/0672327988), de Ron Patton.

![Mensagens de Sistema - Bugs](https://www.ateomomento.com.br/wp-content/uploads/2015/07/mensagens-de-sistemas-bug-ron-patton.png)

Vemos que ele diz que **as mensagens são uma das partes mais negligenciadas** na produção de software. E afirma que Programadores, que não são escritores treinados, tipicamente são quem escrevem estas mensagens.

De fato Programadores não são escritores treinados, mas **quem for responsável** pela definição das mensagens, tem que refletir mais sobre o conteúdo. E, ainda, mensagens ruins são consideradas defeitos (bugs) no software, pois vão totalmente contra as boas práticas de usabilidade.

## **Mensagens rasas – prejuízo para todo mundo**

O adequado **nível de detalhe e clareza** nas mensagens exibidas por um software faz muita diferença na eficiência das operações de desenvolvimento e suporte.

Vamos imaginar duas situações em que um mesmo erro ocorre num sistema – na primeira situação a mensagem é rasa e nebulosa, na segunda é detalhada e clara – e vamos observar alguns prejuízos com o uso da primeira, e benefícios com o uso da segunda.

Para as avaliações, vamos fixar um valor de **R$ 40,00 como valor da hora do usuário** para a empresa na qual trabalha, e **R$ 60,00 como valor da hora do profissional de TI** da empresa que mantém o sistema.

Num sistema de empréstimos, ao realizar uma simulação de parcelamento de um operação, o sistema emite a seguinte mensagem: “Ocorreu um erro ao calcular o valor de uma das parcelas.” e após a exibição da mensagem aborta a execução.

Em quantidade de horas, vamos deduzir quanto tempo é gasto desde que o problema é reportado até que este esteja solucionado.

**Abertura do chamado pelo usuário final:** **10 minutos** pensando sobre a mensagem + **20 minutos** discutindo com pares sobre sobre o que pode ter sido o erro do cálculo + **10 minutos** tentando falar por telefone com o suporte, sem abrir chamado + **20 minutos** montando o corpo do chamado (anexando evidência, relatando contexto etc.) e formalizando a abertura via sistema pertinente (pois o suporte falou que só atende com chamado). Tempo total = **1 hora.**

**Atuação do suporte nível 1:** **20 minutos** realizando análise inicial do chamado + **30 minutos** coletando logs no servidor e anexando-os ao chamado + **10 minutos** compondo o corpo do chamado e encaminhando-o à equipe de desenvolvimento. Tempo total = **1 hora**.

**Resolução do problema pela equipe de desenvolvimento: 30 minutos** analisando os logs do servidor + **30 minutos** tentando simular o erro com teste exploratório + **1 hora** montando massa de dados para novo teste + **1 hora** debugando até encontrar o ponto de parada do erro + **1 hora** implementando o hotfix + **30 minutos** publicando o hotfix no servidor + **20 minutos** gerando as evidências de seu teste do hotfix + **10 minutos** respondendo o chamado e devolvendo-o ao usuário. Tempo total = **5 horas**.

**Teste da correção pelo usuário final: 30 minutos** para simular mesma situação onde ocorreu o erro e realizar nova tentativa de parcelamento no sistema. Tempo total = **0,5 horas**.

**Tempo total de tratamento do problema: 7,5 horas.**

**Custo gerado para o usuário/cliente: R$ 60,00** (1,5 horas gastas – R$ 40,00 cada hora).

**Custo gerado para a equipe de TI/fabricante do software: R$ 360,00** (6 horas gastas – R$ 60,00 cada hora).

**Causa do problema:** erro ao tentar realizar uma divisão por zero quando na tentativa de simular um parcelamento de uma operação de empréstimo. O contrato não possui saldo inicial, logo não era possível simular um parcelamento pois não havia valor a parcelar.





## **Mensagens detalhadas e objetivas – lucro para todo mundo**

Agora vamos realizar uma nova avaliação, considerando uma mensagem diferente gerada a partir da ocorrência do mesmo problema citado.

No mesmo sistema de empréstimos, ao realizar uma simulação de parcelamento de uma operação, o sistema emite a seguinte mensagem:

/*———————————————————————————————-*/
Não foi possível realizar a simulação do parcelamento para a operação solicitada.

Motivo: a operação não possui saldo inicial. Abaixo detalhes sobre os dados informados para o cálculo da simulação do parcelamento e a seguir, informações técnicas a serem informadas à equipe de suporte:

Informações de entrada para o cálculo:
Número da operação: 002YNN8989705
Quantidade de Parcelas: 6
Nome/CPF do cliente: João Paulo/055.444.721-88

Informações para envio à equipe de suporte:
Página: ManterFluxoParcelas.aspx
Classe: FluxoParcelaNegocio
Método: SimularParcelamentoOperacao(…)
Parâmetros de entrada: IdentificadorOperacao = 451233, QuantidadeParcelas = 6, IdentificadorCliente = 988745, SaldoOperacao = 0,00.
Linha do erro: 124
Stack Trace: *<detalhes de rastreamento de pilha da exceção gerada pelo software. Não incluirei aqui por ser muito extenso>*
/*———————————————————————————————-*/

Avaliemos o quanto é detalhada e clara esta mensagem, dando uma visão completa e pontual para o usuário sobre o erro ocorrido, e detalhes técnicos super precisos e completos à equipe de desenvolvimento e suporte do software.

Como realizado para o cenário anterior, em quantidade de horas, vamos deduzir quanto tempo é gasto desde que o problema é reportado até que este esteja solucionado, considerando o uso desta versão da mensagem:

**Abertura do chamado pelo usuário final: 20 minutos** montando o corpo do chamado (anexando evidência, relatando contexto etc.) e formalizando a abertura via sistema pertinente (pois o suporte falou que só atende com chamado). Tempo total = **20 minutos**.

**Atuação do suporte nível 1:** **10 minutos** compondo o corpo do chamado e encaminhando-o à equipe de desenvolvimento. Tempo total = **10 minutos**.

*/\* uma forma otimizada de reportar problemas do tipo é criar um recurso para enviar o corpo da mensagem por e-mail ou um comando para abrir automaticamente o chamado a partir da mensagem. Isso reduziria o tempo de abertura do chamado de 10 minutos para muito menos de um minuto \*/*

**Resolução do problema pela equipe de desenvolvimento: 20 minutos** implementando tratamento de exceção na classe/método/linha apontados pela mensagem, já gerando o hotfix + **30 minutos** publicando o hotfix no servidor + **20 minutos** gerando as evidências de seu teste do hotfix + **10 minutos** respondendo o chamado e devolvendo-o ao usuário. Tempo total = **1,2 horas**.

**Teste da correção pelo usuário final: 15 minutos** para simular a mesma situação onde ocorreu o erro e realizar nova tentativa de parcelamento no sistema. Tempo total = **0,25 horas**.

**Tempo total de tratamento do problema: 1,15 horas.**

**Custo gerado para o usuário/cliente:** **R$ 20,00** (arredondado para 0,5 horas gastas – R$ 40,00 o custo de cada hora).

**Custo gerado para a equipe de TI/fabricante do software: R$ 90,00** (1,5 horas gastas – R$ 60,00 cada hora).





## **Paralelo entre os dois cenários**

Um paralelo detalhado ficará para o quarto post da série, mas só para pensar: o primeiro cenário gerou um custo do atendimento de **R$ 420,00**, o segundo de **R$ 120,00**, gerando uma economia de **74%,** fora a parte emocional dos envolvidos**. Pense nisso em grande escala?**

## Concluindo

Nunca devemos subestimar as mensagens de sistema. O que parece de pouca importância, pode impactar muito (positivamente ou negativamente) no dia a dia das empresas.