# Lab03 - Model-View-Controller

## Tarefa 1

![Diagrama de Orquestração](images/tarefa1.png)

## Tarefa 2
![Diagrama de Coreografia](images/tarefa2.png)
1. O componente Comprador faz postagem de mensagem utilizando o tópico *cotação/#* (exemplo: cotação/geladeira);
2. O componente Leilão assina o tópico *cotação* e realiza publicação de mensagem utilizando o tópico *leilão*;
3. Os componentes do tipo Fornecedor assinam o tópico *leilão* e fazem publicação de mensagens com o tópico *precificação*;
4. O componente Agregador assina o tópico *precificação* e realiza publicação de mensagem com o tópico *agregado*;
5. Os componentes do tipo Comprador assinam o tópico *agregado* e mostra os melhores preços para os consumidores.

## Tarefa 3

> ![tela 1](images/tela1.jpeg)
> ![tela 2](images/tela2.jpeg)
> ![tela 3](images/tela3.jpeg)
> ![tela 4](images/tela4.jpeg)
> ![tela 3](images/tela5.jpeg)
> ![tela 4](images/tela6.jpeg)
![blocks](images/blocks.png)

[Link para o arquivo do aplicativo](app/tarefa3.aia)
