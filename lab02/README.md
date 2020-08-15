# Lab02 - Data Flow & Mensagens

## Tarefa sobre catálogo de componentes

[Notebook](notebook/components-01-catalog.ipynb)

## Tarefa Web Components 1
> Escreva aqui o código da sua composição de componentes Web, como mostra o exemplo a seguir:
~~~html
<dcc-trigger label="Política mundial" action="noticia/mundo/politica" value="Política mundial">
</dcc-trigger>

<dcc-trigger label="Política nacional" action="noticia/brasil/politica" value="Política nacional">
</dcc-trigger>

<dcc-trigger label="Esportes nacional" action="noticia/brasil/esporte" value="Esportes nacional">
</dcc-trigger>

<dcc-trigger label="Esportes estadual (Bahia)" action="noticia/bahia/esporte" value="Esportes estadual (Bahia)">
</dcc-trigger>


<dcc-lively-talk duration="0s"
                 character="doctor"
                 speech="Ouvi isso: ">
  <subscribe-dcc topic="noticia/#/politica"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk duration="0s"
                 character="nurse"
                 speech="Ouvi isso: ">
  <subscribe-dcc topic="noticia/brasil/#"></subscribe-dcc>
</dcc-lively-talk>


<dcc-lively-talk duration="0s"
                 character="patient"
                 speech="Ouvi isso: ">
  <subscribe-dcc topic="noticia/#"></subscribe-dcc>
</dcc-lively-talk>
~~~

## Tarefa Web Components 2
~~~html
<dcc-trigger label="Next Item" action="next/rss">
</dcc-trigger>

<dcc-rss publish="rss/science" source="https://www.wired.com/category/science/feed">
  <subscribe-dcc topic="next/rss" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-aggregator publish="aggregate/science" quantity="3">
  <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-aggregator>

<dcc-rss publish="rss/design" source="https://www.wired.com/category/design/feed">
  <subscribe-dcc topic="next/rss" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="doctor"
                 speech="Notícias ">
  <subscribe-dcc topic="aggregate/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="nurse"
                 speech="Notícias ">
  <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="nurse"
                 speech="Notícias ">
  <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="patient"
                 speech="Notícias ">
  <subscribe-dcc topic="rss/design"></subscribe-dcc>
</dcc-lively-talk>
~~~
