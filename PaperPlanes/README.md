# Análise do aplicativo Paper Planes

**Papers Planes** faz parte do programa _**Google Chrome Experiments**_, *showroom on-line* de experimentos baseados em navegador da 
*web*, programas interativos e projetos artísticos. É um aplicativo web e mobile que permite o usuário criar e dobrar seu próprio avião 
de papel virtual, carimbando-o com a sua localização e "jogando" de volta ao mundo, onde ele poderá ser pego por alguém em outra 
localização para visualizar os carimbos e deixar também a marca do seu endereço.

O **Paper Planes** foi apresentado inicialmente no **Google I/O** em 18 de maio de 2016, conectando participantes e espectadores 
externos por 30 minutos. Para o lançamento público no Dia da Paz de 2016, foi criado um aplicativo **Android** para aumentar a 
tecnologia da web existente com recursos nativos do Android, como notificações avançadas quando um avião é pego em outro lugar do mundo.

O projeto web foi construído utilizando **JavaScript** e **WebGL**, já o experimento **Android** da **Paper Planes** usa a mesma 
renderização **WebGL**, mas é integrado como uma **WebView** em um aplicativo **Android** nativo que estende sua funcionalidade para 
tirar proveito de recursos adicionais, como notificações push avançadas do **Android** e serviços em segundo plano.
	
Como o **Paper Planes** é um aplicativo ativo, com uma infraestrutura de *back-end* em funcionamento e uma base de código que cobre 
várias funcionalidades da experiência, não é possível abrir o código-fonte inteiro de todo o projeto de maneira segura e aceitável, 
sendo assim é aberto para comunidade [4 repositórios online](https://github.com/activetheory/Paper-Planes-Android-Experiment) cobrindo 
4 das inúmeras funcionalidades do experimento:

* **Flocagem**: como usam vários encadeamentos em JavaScript para calcular a simulação de flocagem dos aviões.
* **Aperte para abrir**: como usam o three.js e os metamorfos para criar um avião dobrável animado.
* **Notificaçes Push**: como utilizam o firebase e o sistema rico de notificações do Android.
* **Ponte nativa do WebView**: um exemplo de código completo de como criar um aplicativo com um **WebView** em tela cheia como a camada 
de visualização, além de como se comunicar entre **Java** e **JavaScript**.

## Flocagem

O aglomerado dos planos de papel ao redor da Terra foi realizado utilizando *multi-threading* para lidar com as simulações da 
localização de cada avião. Isso mantinha o thread principal livre para gerenciar as animações e interações do aplicativo. 

O **Threejs** foi utilizado para gerar uma geometria instanciada, combinando todos os planos em uma chamada de renderização, permitindo 
muita complexidade e mantendo a comunicação no mínimo. Cada segmento consistia em uma simulação separada, lidando cada um com apenas 
uma seleção de planos; um segmento da geometria. Ao receber as posições e orientações atualizadas de cada *thread*, os *buffers* da 
geometria são atualizados para refletir a localização de cada avião.

## Aperte para abrir

A mecânica *pinch-to-open* consistia em uma variável de progresso gerenciada por uma classe interativa de *pinching* e em uma animação 
de destino de metamorfose criada usando a biblioteca **WebGL**, **Threejs**. Quando um usuário aperta para fora ou para dentro de um 
plano dobrado, o avião se anima desdobrando e dobrando. Era muito importante para nós manter esses elementos entrelaçados, para que um 
usuário pudesse brincar com a animação, esfregando-o para a frente e para trás, como preferir, em vez de apenas acionar uma animação 
quando o usuário começar a interagir. Esses tipos de interações individuais ajudam bastante a fazer com que um aplicativo pareça 
responsivo e divertido.

## Notificações push nativas

À medida que as pessoas pegam e jogam aviões de todo o mundo, as notificações *push* foram utilizadas no aplicativo **Android** para 
notificar os usuários de que o avião foi pego e jogado.

O **FCB** (*Firebase Cloud Messaging*) é usado para enviar notificações *push* para o aplicativo.  Os [arquivos de exemplo](https://github.com/activetheory/Paper-Planes-Android-Experiment/tree/master/PushNotifications/app/src/main/java/net/activetheory/examples/notifications) 
demonstram como as bibliotecas do **Firebase** foram utilizadas para receber mensagens no aplicativo **Android**.

## Comunicação WebView nativa

Um recurso extremamente poderoso do **Android** é o fato de o **Chrome** ser incorporado no **sistema operacional** e pode ser usado 
para criar aplicativos que ampliam o poder da *Web* com os recursos nativos do **Android**.

Este repositório demonstra a criação de um aplicativo **WebView** em tela cheia com comunicação **Java <-> JavaScript** para enviar 
dados e acionar uma notificação nativa do **Android 7**.
