# Sobre este repositório

<p>
  Este repositório foi criado para manter um desafio proposto por uma empresa para mim.
</p>

<p> 
  Nele estou documentando com carinho cada passo-a-passo que dou.
</p>

## Como a solução funciona atualmente

<p>Dado um termo de busca, o programa procura e captura as informações de <strong>todos os produtos</strong> na loja da Amazon de forma automatizada extraindo como informação principal o <strong><i>Nome do Produto e Valor</i></strong> do mesmo e também algumas <strong>informações extras</strong>.</p>


### Sobre a busca e extração de informações
<p>O programa faz todo o trabalho de buscar as informações usando as bibliotecas <strong>requests</strong> e <strong>BeautifulSoup</strong>. Após isso o tratamento e exportação dos dados é feito usando a biblioteca <strong>pandas</strong>.</p>

<ul>
  <li>A requisição da página toda é feita usando o <i>requests</i>;</li>
  <li>Com a página toda salva eu capturo a quantidade total de páginas usando o <i>BeautifulSoup</i>;</li>
  <li>Faço o restante das requisições até a página limite;</li>
  <li>Com todas as páginas salvas eu seleciono e extraio as informações de todos produtos usando os seletores CSS do <i>BeautifulSoup</i>;</li>
  <li>Limpo e Serializo os dados em uma List de Dict para deixar fácil o manuseio usando a biblioteca <i>pandas</i>;</li>
  <li>E assim, finalizo exportando (tanto em csv quanto em excel) usando a biblioteca <i>pandas</i>.</li>
</ul>

### Problemas que tive durante o processo:
<p><i>Eu diria que o maior problema foi tentar usar o Selenium logo de cara como opção principal (me senti tentando matar uma barata com uma bazuca...).</i></p>

<ul>
  <li>Primeiramente tentei interceptar a rota em que a Amazon buscava os dados dos produtos para preencher dinamicamente. Porém os dados eram muito sujos (com varios     caracteres à mais) e sendo assim mais difícil de manusear. <strong>Então foi aí que optei por lidar com o <i>html</i> da página para extrair as                       informações</strong>.
  </li>
  <li>A partir disso o problema foi fazer a request em python, pois eu não sabia como passar na header o "User-Agent" de forma personalizada.</li>
</ul>

## Referências que usei para realizar o desafio

<p>[HTTP CORS - MDN](https://developer.mozilla.org/pt-PT/docs/Web/HTTP/CORS)</p>
<p>[Data Mining](https://fia.com.br/blog/data-mining/)</p>
