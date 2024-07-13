# Conceito de Memória
Uma das funções primordiais de um computador é a capacidade que ele tem de armazenar dados, seja de curto, médio ou longo prazo. Para cada uma dessas escalas de tempo, existem diferentes tipos de memórias que podem ser usadas.

# Características da memória
Como mencionado anteriormente, diferentes tipos de memórias se adaptam a diferentes tempos de armazenamento de dados. Para que essa adaptação seja possível, algumas características dessas tecnologias de armazenamento variam, como localização, método de acesso, tipo físico, dentre outros.

## Localização
Existem diferentes localizações de memória que variam a forma com que ela se comunica com o computador.

### Interna
A memória interna é diretamente acessível à Unidade Central de Processamento (CPU). Exemplos de memória interna são a Memória Principal, Registradores, Memória Cache, etc.

### Externa
A memória externa consiste em dispositivos periféricos ao computador, que não estão diretamente acessíveis à CPU, mas sim indiretamente através dos controladores de E/S (Entrada e Saída)


## Método de acesso
Diferentes tipos de memória tem diferentes meios de acessar os dados gravados nela.

### Sequencial
No **Método de Acesso Sequencial (ou Serial)**, os dados são acessados em sequência, um atrás do outro, na ordem em que são gravados. Isso faz com que seu tempo de acesso varie, dependendo da posição do dado que se quer ler, uma vez que ele não é capaz de pular diretamente para a posição do dado desejado.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/reb47dnpktxrwevjuzfy.jpg)

### Direto
O **Método de Acesso Direto** é feito com um salto até o **bloco de registros** onde está o registro desejado, onde é realizado uma **pesquisa sequencial** logo em seguida para encontrar o registro em questão.

As divisões são de **blocos com endereço único** e o dispositivo de leitura e escrita é o mesmo. O tempo de acesso é variável.

Um exemplo de dispositivo de armazenamento que utiliza esse método é uma **Unidade de Disco Rígido**.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/iajbj7tsisyidv9zbb9s.jpg)



### Aleatório
O **Método de Acesso Aleatório** é feito diretamente no **registro** por meio do endereço do mesmo. Os mecanismos de leitura e escrita são separados e o acesso é feito diretamente no endereço, sem ter que percorrer outros endereços nem logicamente quanto fisicamente, por conta disso, o tempo de acesso é **constante**, independente de onde esteja o endereço desejado.

Um exemplo de dispositivo que utiliza do **Método de Acesso Aleatório** é a **Memória Principal**, ou **Memória RAM**.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/78se4ljqa35s08ffsdan.jpg)



### Associativo
O **Método de Acesso Associativo** é feito diretamente no registro e através de um sistema de endereçamento próprio baseado na identificação de padrões de bits. O tempo de acesso é constante.

Um exemplo de dispositivo que usa esse método é a **Memória Cache**.


## Unidade de transferência
Os dados podem estar gravados, sendo lidos ou escritos de diferentes formas, dentre elas, podem ser **"Palavras"** ou **"Blocos"**.

### Palavra
Palavra é a unidade natural em que se organiza a memória no computador. Ela tem um tamanho fixo que depende da máquina e varia entre potências (mais comum) ou múltiplos de 2 (Por exemplo: 8, 16, 32, 64, 128) e representa a quantidade de dados que podem ser lidos/escritos de uma só vez.

Um computador de 32 bits teria, por exemplo, 4 bytes (32 bits) por palavra, e é essa a unidade fixa que o processador usa para se comunicar e também que é usada para se comunicar com ele.

Instruções de programa podem exigir uma ou mais palavras.

#### Endereçamento da Memória Principal
O tamanho da palavra também serve para determinar os endereços da Memória Principal, sendo o tamanho da Palavra em **bits** a potência de 2 que resultará na quantidade de endereços disponíveis. Isso ocorre porque o endereço normalmente deve poder ser representado com uma palavra, que representa 2ⁿ possibilidades de endereços, considerando _n_ como o tamanho da palavra.

Esses endereços são usados para guardar e identificar dados da Memória Principal. Isso significa que a RAM vai ser de 2ⁿ? Não, mas seu máximo teórico sim.

Pra deixar isso mais claro, imagine que você tenha um computador de 32 bits. 2³² bits são 4GB, ou seja, você tem um **máximo teórico** de 4GB de RAM no computador. Isso significa que o computador tem 4GB de RAM? Não, a ênfase no termo "máximo teórico" foi por conta que o processador tem endereços suficientes para suportar essa quantidade de memória, mas não significa que ele terá tudo isso disponível. Se você colocar 2GB de RAM nesse computador, a memória RAM seria esgotada antes mesmo de preencher todos os endereços disponíveis (o que não significa que não funcionaria), e caso você colocasse 8GB de RAM, o computador ignoraria os outros 4GB e consideraria só os 4 primeiros, pois ele não consegue representar os endereços restantes com 32 bits de palavra.

#### Barramento
O Barramento (também chamado de _Bus_) é uma coleção de fios paralelos, normalmente impressos diretamente no PCB que transportam dados, endereços e sinais de controle. Eles conectam, por exemplo, a **Memória Interna** com a **Unidade Central de Processamento (CPU)**.

### Bloco
Blocos são conjuntos de bits maiores do que uma palavra e que, muitas vezes, contém ou podem conter múltiplas palavras.

Existem dois casos de bons exemplos de blocos. O armazenamento em dispositivos de **Memória Externa** costumam ser organizados em blocos, como em Unidades de Disco, onde os blocos recebem endereços únicos e guardam dados dentro deles. Além disso a divisão da **Memória Interna** e organização da **Memória Cache** também tem **relação** com essa estrutura.

## Capacidade
Uma característica importante das memórias é a sua capacidade de armazenar dados em relação com o tamanho da palavra.

A ordem de grandeza da capacidade da **Memória Interna** costuma variar entre KB e GB, sendo os valores mais baixos para Registradores e Memória Cache enquanto os valores mais altos para Memória Principal (RAM).

Já na **Memória Externa**, o comum é ver capacidades da ordem de grandeza de MB, GB, ou até mesmo TB que tem barateado muito ultimamente.

O motivo dessa diferença de capacidade entre as memórias é bem simples: custo.

As memórias que precisam se comunicar mais com o processador são mais rápidas mas também são mais caras, portanto não é viável e nem necessário uma Memória Cache de 2TB, por exemplo.


## Desempenho
Existem algumas variáveis dentre os tipos de memória que podem ser levados em conta para comparar seus desempenhos.

### Tempo de acesso
Tempo que dura a localização, leitura ou escrita de um dado.

### Tempo de ciclo
O tempo de ciclo é o tempo de acesso somado ao tempo necessário para fazer o restante dos processos de um ciclo, até estar apto a iniciar outro processo de acesso de memória.

### Taxa de transferência
Quantidade de **dados transferidos em função do tempo**, como por exemplo "Mbps" (Megabits por segundo), usado para demonstrar a taxa de transferência de downloads.


## Tipo físico
Existem diferentes tipos físicos de memória e que são mais empregados em alguns tipos específicos de memórias.

### Semicondutor
Semicondutores são os tipos físicos mais usados atualmente em memórias internas, a Memória Principal (RAM), por exemplo, funciona a base de semicondutores.

### Magnético
Um exemplo de memória que utiliza de superfície magnética por exemplo é a Unidade de Disco, que move um braço que modifica a magnetização da superfície do disco para gerar um padrão de "magnetizado" e "não-magnetizado" de grosso modo, criando um padrão legível como os 0 e 1 que representam os dados.

### Óptico
A superfície óptica é um material que pode ser queimado por um laser no processo de gravação de dados, e essas "queimaduras" poderão ser posteriormente lidas por um laser de alta precisão. Esse é o exemplo da gravação de memória em CDs e DVDs


## Características físicas

### Persistência de dados (Volátil / Não Volátil)

#### Memória Volátil
A memória volátil é a memória que **mantém os dados apenas enquanto o dispositivo está sendo energizado**. Ao desligar o computador por exemplo, o que estava armazenado em memória volátil é perdido. Um exemplo de memória volátil é a memória RAM (memória principal)

#### Memória não-volátil
A memória não volátil é a memória que **mantém os dados mesmo quando não está sendo energizado**, mantendo assim os dados quando o computador é desligado. Um exemplo de memória não volátil são os HDs e SSDs, ou seja, em grande parte memórias externas são não voláteis.

### Apagável / Não apagável
Existem diferentes tipos de memória que variam sua capacidade de modificação do conteúdo. Algumas memórias, por exemplo, servem apenas para leitura.

#### Read Only Memory (ROM)
Memória apenas de leitura, não permite gravação.

#### Memória principalmente de leitura
Memórias que **permitem gravação**, porém são **mais usadas para leitura**.

#### Memória de leitura e gravação
Memórias que permitem **leitura** e **gravação** de dados.

# Hierarquia de Memória


![Imagem de pirâmide hierárquica de memória](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/eeebp6tfhmq4lmz8ykmq.png)



Hierarquia de memória:

1. Registradores
2. Cache L1
3. Cache L2
4. Memória Principal
5. Cache de Disco
6. Disco magnético
7. Disco óptico
8. Fita magnética

Quanto maior o nível (mais próximo do 1) da memória na hierarquia, menor tende a ser a capacidade (por conta do alto custo de capacidade) e mais rápida ela é, do mesmo modo que quanto menor o nível (mais próximo do 8), maior a capacidade e menor a velocidade. Da mesma forma, quanto maior o nível na hierarquia, maior a frequência de comunicação dela com a CPU e vice-versa.

## Princípio da Inclusão
De acordo com a hierarquia demonstrada anteriormente, o **Princípio da Inclusão** diz que o conteúdo de uma memória de maior nível (mais próximo do 1) deve estar incluso em uma memória de menor nível (mais próximo do 8).

## Princípio da Coerência
Ainda relacionado à hierarquia anteriormente mencionada, o **Princípio da Coerência** diz que o conteúdo copiado em memórias de diferentes níveis (Princípio da Inclusão) devem ser consistentes. Por exemplo, deve ter uma consistência entre um dado que, do **disco magnético** passou para a **memória principal** e depois para o **Cache L1**, todos essas cópias de dados devem ser consistentes entre si.

## Localidade de Referência
Durante a execução de um programa, as referências de memórias pelo processador para instruções e dados tendem a se agrupar.

### Localidade Temporal
O Princípio da Localidade Temporal diz que endereços de memória acessados, **tendem** a serem acessados novamente em um curto intervalo de tempo.

Por exemplo, o uso de variáveis temporárias, laços de repetição, etc.

### Localidade Espacial
O Princípio da Localidade Espacial diz que conteúdos com endereços de memória próximos tendem a serem acessados em intervalos de tempo semelhantes. Por exemplo, considere que um endereço hipotético A está ao lado do endereço B. Quando o endereço A for acessado, a tendência é que B seja acessado em breve.

Por exemplo arrays, strings e outras estruturas sequenciais.

## Acertos e falhas
O conceito de acertos e falhas faz referência ao resultado de uma busca na memória.

### Acerto (hit)
Um acerto acontece quando se encontra o dado desejado no endereço de memória.

### Falha (fault)
Uma falha acontece quando não se encontra o dado desejado no endereço de memória.

> Ou seja, se você faz uma busca em um endereço qualquer "x", caso o dado que você queira realmente estava em x, você tem um acerto, caso contrário, você tem uma falha.

### Taxa de acerto e de falha

A taxa de acerto e de falha é calculada pela quantidade de acertos/falhas que você tem por acessos/tentativas.

### Tempo de Acerto
Tempo de acerto é o tempo que o computador leva para, dado uma tentativa de acesso, determinar se foi um acerto ou uma falha.

### Penalidade por Falha
Tempo necessário para substituir um bloco de memória pelo bloco de nível superior que contém o dado desejado, contando com o tempo de envio ao processador.

# Princípios da Memória Cache

## Origem

A memória cache foi criada como um intermediário entre a CPU e a Memória Principal para acelerar o processamento de dados.

## Funcionamento

A memória cache tem uma cópia de alguns dados da memória principal, sendo assim, quando o processador precisa de uma palavra da memória, ele primeiro verifica se essa palavra está no cache, pois caso esteja, o acesso pode ser feito de forma mais rápida, uma vez que a memória cache é mais rápida que a memória principal.
Caso a palavra não esteja na cache, o bloco com a palavra requerida é transferido para a cache, e então para o processador, porém o tempo de acesso se torna maior pois é necessário que se acesse a Memória Principal.

> O acesso a Memória Principal retorna um bloco à Memória Cache pois pelo **Princípio da Localidade**, trazer um bloco à cache aumenta a chance da próxima palavra que o processador precisar estar na cache, acelerando o processo de busca.

## Mapeamento da Memória Principal
A Memória Principal é composta de 2ⁿ palavras onde cada palavra tem um endereço distinto de _n_ bits.

> Um sistema de 64 bits teria uma Memória Principal de 2⁶⁴ palavras, com cada palavra tendo um endereço único de 64 bits

Além disso, a Memória Principal ainda seria dividida em blocos de tamanho fixo com uma quantidade _K_ de palavras por bloco.

## Mapeamento da Memória Cache
A Memória Cache é composta de uma quantidade _m_ de blocos, chamados de **linhas**, sendo cada linha composta de _K_ palavras, bits de controle e uma tag de alguns bits que indica o bloco a qual pertence os dados que estão armazenados na linha 
 
# É isso!
Espero que tenham conseguido entender as explicações, e caso você tenha alguma dúvida, sugestão ou correção para fazer, sinta-se a vontade para deixar nos comentários.
Bons estudos ;)