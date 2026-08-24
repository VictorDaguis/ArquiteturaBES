# Atividade - Destrinchando os estilos

## 1. Cliente-Servidor

### Conceito e definição

Cliente-servidor é um estilo onde existem duas partes principais: o cliente e o servidor.

O cliente faz um pedido e o servidor recebe esse pedido, faz o que precisa e devolve uma resposta.

Um exemplo simples é quando entramos em um site. O navegador faz um pedido para o servidor e o servidor retorna a página que foi solicitada.

### Casos de uso comuns

Esse estilo é usado quando vários clientes precisam acessar o mesmo serviço.

Exemplos:

* **Sites:** o navegador faz pedidos para o servidor e recebe as páginas e informações.
* **DNS:** o computador consulta um servidor DNS para descobrir o endereço IP de um site.

Também pode ser usado em sistemas de empresas, onde vários computadores acessam os mesmos dados em um servidor.

### Principais vantagens

* É um modelo simples de entender.
* Vários clientes podem usar o mesmo servidor.
* Os dados e serviços podem ficar centralizados.
* É um modelo muito usado em sistemas atualmente.

### Principais desvantagens

* O servidor pode ficar sobrecarregado se receber muitos pedidos.
* Se o servidor parar, os clientes podem ficar sem acesso ao sistema.
* Pode ser necessário aumentar a capacidade do servidor conforme o número de usuários aumenta.
* O sistema depende da comunicação entre cliente e servidor.

---

## 2. Publicador/Assinante

### Conceito e definição

Nesse estilo, um sistema publica uma informação em um canal e outros sistemas que estão interessados recebem essa informação.

O mais importante é que quem publica não precisa saber exatamente quem vai receber a mensagem.

Por exemplo, um sistema pode publicar um evento dizendo que um pedido foi realizado. Outros serviços podem receber essa informação e realizar suas tarefas.

### Casos de uso comuns

Esse estilo é muito usado quando um mesmo evento precisa gerar várias ações.

Exemplos:

* **Pedidos:** quando um pedido é feito, um serviço pode atualizar o estoque e outro pode enviar um e-mail para o cliente.
* **RabbitMQ:** pode ser usado para receber uma mensagem e encaminhá-la para o serviço responsável por enviar um e-mail.

Esse tipo de arquitetura também ajuda quando queremos que algumas tarefas sejam feitas de forma separada da ação principal.

### Principais vantagens

* Os sistemas ficam menos dependentes uns dos outros.
* Uma mensagem pode ser recebida por diferentes serviços.
* Algumas tarefas podem ser feitas em segundo plano.
* É possível adicionar novos serviços para receber os eventos.

### Principais desvantagens

* Pode ser mais difícil descobrir o que aconteceu com uma mensagem.
* Se algum serviço estiver fora do ar, a mensagem pode não ser processada na hora.
* O sistema pode ficar mais difícil de entender quando existem muitos eventos.
* É necessário controlar os canais e as mensagens.

