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

<a href="https://fia.com.br/blog/data-mining/">Data Mining</a><br>
<a href="https://www.crummy.com/software/BeautifulSoup/bs4/doc/">BeautifulSoup Documentation</a><br>
<a href="https://requests.readthedocs.io/pt_BR/latest/user/quickstart.html#cabecalhos-personalizados">Requests - Cabeçalhos Personalizados</a><br>
<a href="https://requests.readthedocs.io/pt_BR/latest/user/advanced.html">Requests - Uso avançado</a><br>
<a href="https://docs.microsoft.com/pt-br/sql/data-quality-services/data-cleansing?view=sql-server-ver15#:~:text=Limpeza%20de%20dados%20%C3%A9%20o,fazer%20altera%C3%A7%C3%B5es%20assim%20aos%20dados.">Data Cleansing - Microsoft</a><br>
<a href="https://numpy.org/doc/stable/reference/generated/numpy.array.html">Numpy Array - API Reference</a><br>

<br><strong><u>Mozilla Web Docs</strong></u><br>
<a href="https://developer.mozilla.org/pt-PT/docs/Web/HTTP/CORS">HTTP CORS - MDN</a><br>
<a href="https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Headers/User-Agent">User-Agent - MDN</a><br>
<a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Browser_detection_using_the_user_agent">Browser detection using the user agent - MDN</a><br>


<strong><u>GeekForGeeks</strong></u><br>
<a href="https://www.geeksforgeeks.org/response-url-python-requests/">Python response url - GeekForGeeks</a><br>
<a href="https://www.geeksforgeeks.org/convert-a-numpy-array-into-a-csv-file/">Numpy Array to csv file - GeekForGeeks</a><br>

<strong><u>pandas</strong></u><br>
<a href="https://pandas.pydata.org/docs/reference/index.html">pandas - API Reference</a><br>
<a href="https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.from_dict.html">pandas.DataFram.from_dict()</a><br>
<a href="https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_excel.html">pandas.DataFrame.to_excel()</a><br>

<strong><u>StackOverflow</u></strong><br>
<a href="https://stackoverflow.com/questions/2957013/beautifulsoup-just-get-inside-of-a-tag-no-matter-how-many-enclosing-tags-there">bs4 - find all tags</a><br>
<a href="https://stackoverflow.com/questions/6081008/dump-a-numpy-array-into-a-csv-file">Numpy - dump array into csv</a><br>
<a href="https://stackoverflow.com/questions/48053207/writing-single-csv-header-with-pandas">Writing csv headers with pandas</a><br>
<a href="https://stackoverflow.com/questions/44691524/write-a-2d-array-to-a-csv-file-with-delimiter">Write 2d array into a csv with delimiter</a><br>
<a href="https://stackoverflow.com/questions/19124601/pretty-print-an-entire-pandas-series-dataframe">pandas - Pretty print dataframe</a><br>
