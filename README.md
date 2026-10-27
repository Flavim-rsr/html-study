# Curso HTML

# Primeiros passos com HTML

---

## 1- Entendendo Comunicação Client x Server

### O que são Clients

Quando o cliente acessa a Internet(http), ela retorna do servidor arquivos estáticos (HTML, CSS, JavaScript). Normalmente o navegador grava os arquivos na sua maquina para evitar de baixar varias vezes os dados da pagina, se chama cash.

Design Responsivo : se trata de estilizar as paginas criadas para cada tipo de dispositivos, ser compatível com varias telas, como desktops, smartphones, tvs, notebooks. Utilizando boas praticas e testes.

Os navegadores são instalados para poder executar arquivos (HTML, CSS, linguagens de programação), todos navegadores mantem um padrão criados pela W3C. Para saber quais comandos funcionam nos navegadores temos o W3Schols, que informa quais TAGS funcionam  nos navegadores.

Aplicação Web são soluções criadas que possuem a internet como meio de comunicação entre client X server, não sendo necessário sua instalação, ex: youtube instalado como um aplicativo não é uma aplicação web, mas se for acessado pelo navegador se passa a ser uma aplicação web.

Dispositivos moveis são mais utilizados no mundo todo.

### O que são Servers

Servidores são maquinas que servem de apoio a outros computadores, são chamadas de rede local, servidores web ou data centers, normalmente são computadores mais robustos pois temos muitos computadores fazendo requisições nele. Temos diversos tipos de servidores: 

- Arquivos, computadores central que armazena arquivos (imagens, áudios, vídeos)para outros computadores utilizarem
- Segurança (Firewall)
- Streaming, transmitir dados
- E-mail, computadores para enviar e mails
- Web
- Data Centers, servidores maiores que armazena grandes números de dados

Softwares (sistemas operacionais, monitoramento, servidores web)

Hardware (armazenamento (ssd, disco rigido), memoria, processadores)

Os servidores tem um sistema operacional (Windows, Linux, Ubunto) que vai ter um servidor web (Apache, Nginx) instalado, responsável por atender as requisições http processando-as e devolvendo a resposta em HTML, css, javascript.

Tipos de servidores: 

- Proxy: servidor que cria limitações para não conseguir acessar alguns sites, pode ser usado como servidor de autenticação.
- Firewall: feito para criar a defesa externa caso tente acessar um arquivo malicioso vindo de fora.
- Web Server: é um servidor que bate no Apache e depois bate na internet.
- E-mail Server: voltado para armazenar e-mails.
- Database Server: usado para acessar os dados da aplicação.
- Intranet: internet de um servidor local, utilizado em meios corporativos.
- DNS: um servidor que detem uma lista de nomes e ips, utilizado para traduzir o www e redirecionar para o ip.

Hospedagem de site, quando você contrata um serviço para subir sua aplicação para a internet.

- https: conexão segura criptografada
- Dominio: é o nome que você vai registrar o site, podendo ser utilizado para e-mail, depois de registrado não pode ser criado outro igual.
- FTP: conexão exclusiva para enviar arquivos.

### Linguagens de Programação

São conjuntos de informações que são executadas conforme a logica implementada. 

Linguagens de programação que rodam diretamente no servidor, Server Side (PHP, Java, JavaScript, Ruby, C#). Cada uma possui a sua sintaxe.

Linguagem de programação que rodam do lado do cliente, Client Side (JavaScript).

## 2- Introdução ao HTML na pratica

### Corpo do HTML

O **arquivo `index.html`** geralmente é a página principal de um site, sendo o ponto de entrada para a aplicação.

- A estrutura básica de um documento HTML é composta por duas seções principais:
    1. **`<head>`**: Contém informações sobre a página, como o título (exibido na aba do navegador), links para arquivos externos (como CSS e fontes), metadados (como charset e descrição) e outras configurações que não são visíveis diretamente na página.
    2. **`<body>`**: Tudo que está dentro desta tag será exibido no corpo da página, incluindo textos, imagens, botões e demais elementos visíveis para o usuário.

```html
<html>
		<head>
				<title>Meu titulo da pagina</title>
		</head>
		<body>
				<!-- Corpo da pagina fica no body->
		<body/>
</html>
```

- A maioria das **tags HTML** precisa ser **aberta e fechada**. No entanto, algumas tags são **auto fechadas**, ou seja, não precisam de uma tag de fechamento explícita. Essas tags geralmente representam elementos vazios, como a tag `<input>`, que cria campos de formulário. **Tags auto fechadas** geralmente terminam com uma barra (`/`), embora isso seja opcional em HTML5:
    
    ```html
    <strong>Olá Mundo, <i>Tudo bem</i></strong>
    <input type = "text" />
    <img />
    ```
    

- Atributos: são identificadores de elementos, o javascript tem o poder de pegar esse atributo e alterar o conteúdo do elemento.
    
    ```html
    <strong id= "titulo">Olá Mundo, <i>Tudo bem<i></strong>
    <strong style= "color: blue;">Olá Mundo, <i>Tudo bem<i></strong>
    <strong class= "titulo-principal">Olá Mundo, <i>Tudo bem<i></strong>
    <input type= "color"/>
    <input type= "text"/>
    <input type= "number"/>
    <img width ="150" src="" />
    ```
    

### Tipografia HTML são os tipos de tags para texto no HTML:

- **Títulos**:
    
    **`<h1>`**, **`<h2>`**, **`<h3>`** (até **`<h6>`**): São usados para criar títulos de diferentes níveis. O **`<h1>`** é o mais importante, geralmente usado para o título principal da página. O **`<h2>`** é um subtítulo, e assim por diante, até o **`<h6>`**, que é o título de menor importância.
    
    ```html
    <h1>Meu Título Principal</h1>
    <h2>Subtítulo Secundário</h2>
    ```
    

- **Parágrafos**:
    
    **`<p>`**: Define um parágrafo de texto. Sempre que você quiser iniciar um novo bloco de texto, você utiliza essa tag. A tag `<p>` cria automaticamente uma quebra de linha antes e depois do parágrafo.
    
    ```html
    <p>Este é um parágrafo de texto.</p>
    ```
    

- **Citações**:
    
    **`<blockquote>`**: Utilizado para destacar citações longas de outras fontes. Ele geralmente aplica indentação ao texto citado.
    
    ```html
    <blockquote>“A persistência é o caminho do êxito.” - Charles Chaplin</blockquote>
    ```
    

- **Negrito**:
    
    **`<strong>`**: Serve para dar ênfase forte em um texto, geralmente renderizado em negrito. Ele indica que o conteúdo tem uma importância maior.
    
    ```html
    <p>Este é um texto <strong>muito importante</strong>.</p>
    ```
    

- **Sublinhado**:
    
    **`<u>`**: Aplica um sublinhado no texto. Essa tag geralmente é usada para destacar algo, mas seu uso tem sido substituído em muitos casos pelo CSS.
    
    ```html
    <p>Este é um texto <u>sublinhado</u>.</p>
    ```
    

- **Itálico**:
    
    **`<i>`**: Deixa o texto em itálico. É usado principalmente para indicar ênfase, palavras estrangeiras ou o título de uma obra.
    
    ```html
    <p>Este é um texto em <i>itálico</i>.</p>
    ```
    

- **Marcado**:
    
    **`<mark>`**: Sublinhar uma parte do texto, destacando-o com uma cor de fundo, como se fosse um marcador de texto.
    
    ```html
    <p>Este é um texto <mark>destacado</mark>.</p>
    ```
    

- **Texto em sobrescrito**:
    
    **`<sup>`**: Coloca o texto em uma posição elevada, geralmente usado para expoentes matemáticos ou referências.
    
    ```html
    <p>E=mc<sup>2</sup></p>
    ```
    

### Listas no HTML

- **Ordered List** (Lista Ordenada)
    
    A tag **`<ol>`** é usada para criar uma **lista ordenada** em HTML, onde os itens são numerados automaticamente. Cada item da lista é representado pela tag **`<li>`** (list item).
    
    **`<ol>`**: Define o início e o fim de uma lista ordenada.
    
    **`<li>`**: Representa cada item da lista dentro da tag `<ol>`.
    
    ```html
    <ol>
      <li>Primeiro item</li>
      <li>Segundo item</li>
      <li>
    			<ol>
    				<li>Item 1</li>
    				<li>Item 2</li>
    			</ol>
      </li>
    </ol>
    ```
    

- **Unordered List** (Lista Não Ordenada)
    
    A tag **`<ul>`** é usada para criar uma **lista não ordenada** em HTML, onde os itens são representados por marcadores (pontos) em vez de números. Cada item da lista é definido pela tag **`<li>`** (list item).**`<ul>`**: Define o início e o fim de uma lista não ordenada.
    
    **`<li>`**: Representa cada item da lista dentro da tag `<ul>`.
    
    ```html
    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
      <li>Item 3</li>
    </ul>
    ```
    

### Navegações

A tag **`<a>`** (de "âncora") é usada para criar links em uma página HTML. Ela utiliza o atributo **`href`** para definir o destino do link. O texto colocado dentro da tag **`<a>`** será exibido como o link clicável.

```html
<a href="https://www.exemplo.com">Visite nosso site</a>
```

Neste exemplo, ao clicar no texto "Visite nosso site", o usuário será direcionado ao site especificado no **`href`**.

- Alguns atributos importantes:
    
    **`target`**: Define como o link será aberto.
    
    **`target="_blank"`**: Abre o link em uma **nova aba** ou janela do navegador
    
    ```html
    <a href="https://www.exemplo.com" target="_blank">Abrir em nova aba</a>
    ```
    
    **`target="_self"`**: Abre o link na **mesma aba** (comportamento padrão se o atributo não for especificado).
    
    ```html
    <a href="sobre.html" target="_self">Sobre nós</a>
    ```
    
    **`title`**: Quando utilizado, exibe um balão de ajuda com uma mensagem quando o mouse passa por cima do link.
    
    ```html
    <a href="https://www.exemplo.com" title="Clique para visitar">Nosso site</a>
    ```
    

- Navegação entre arquivos HTML:
É possível fazer navegação entre páginas HTML locais, utilizando o nome do arquivo no atributo **`href`**. Por exemplo:
    
    ```html
    <a href="contato.html">Página de Contato</a>
    ```
    
    Ao clicar, o usuário será direcionado para o arquivo **`contato.html`**, facilitando a navegação entre diferentes páginas do site.
    
- Boas práticas:
    
    Quando estiver criando links dentro do próprio site, é recomendado manter o usuário na mesma aba, ou seja, sem usar **`target="_blank"`**.
    
    Utilize **`target="_blank"`** apenas para links que levam o usuário para **outros sites**, abrindo-os em uma nova aba para evitar que o visitante saia do seu site principal.
    

### Bônus

- `<hr>` **(tracejado)**: A tag `<hr>` é utilizada para criar uma linha horizontal no documento HTML, muitas vezes usada para separar seções de conteúdo.
- **Links como âncora**: Os links podem ser usados não apenas para navegar para outras páginas, mas também para fazer ancoragem dentro da própria página. Isso significa que você pode direcionar o usuário para um local específico dentro da mesma página sem necessariamente recarregar a página inteira.
    
    **Exemplo**: Para criar um link que leve o usuário para uma seção específica da página, você pode definir um ID (`id`) no elemento de destino e usar esse ID como o valor do atributo `href` do link. Por exemplo:
    
    ```html
    <a href="#secao2">Ir para Seção 2</a>
    <!-- ... -->
    <h2 id="secao2">Seção 2</h2>
    <p>Conteúdo da Seção 2.</p>
    ```
    
    Neste exemplo, ao clicar no link "Ir para Seção 2", o navegador irá rolar a página até a seção com o ID `secao2`.
    
    **Botão de voltar usando `<small>`**: Para criar um botão de voltar discreto, pode-se usar a tag `<small>` para estilizar o texto como menor. Por exemplo:
    
    ```html
    <small><a href="#topo">Voltar ao Topo</a></small>
    ```
    
    Onde `#topo` seria o ID da seção inicial da página.
    
    A ancoragem é uma técnica útil para melhorar a navegabilidade de páginas longas, permitindo que os usuários naveguem rapidamente para seções específicas sem a necessidade de rolar manualmente por todo o conteúdo.
    

# HTML 1: Conceitos Básicos

---

## 1- Trabalhando com formulários

### Tag form

Um **formulário** em HTML é um elemento usado para capturar informações do usuário, como texto, números, e estados (ex.: se o usuário está ativo ou não). Quando o usuário preenche o formulário e clica no botão de envio, ocorre uma comunicação entre o **cliente** (navegador) e o **servidor**.

- **Lado cliente**: Enquanto o usuário está visualizando e preenchendo o formulário na tela, ele está interagindo com a parte cliente (front-end).
- **Lado servidor**: Ao clicar em "Enviar", os dados são enviados para o servidor (back-end), onde podem ser processados. O servidor pode, por exemplo, consumir essas informações e decidir se elas devem ou não ser salvas em um banco de dados (BD).

A **segurança** é um aspecto crucial no uso de formulários, principalmente quando eles capturam dados sensíveis, como informações pessoais ou financeiras. Por isso, é importante garantir que os dados sejam transmitidos e armazenados de maneira segura, evitando vazamentos ou acessos não autorizados.

Para entender melhor como proteger dados sensíveis, recomenda-se estudar normas como a **LGPD** (Lei Geral de Proteção de Dados). Essa legislação visa garantir a transparência sobre como os dados dos usuários são coletados, armazenados e utilizados, exigindo que as empresas informem claramente ao usuário o que será feito com suas informações.

A tag **`<input>`** é uma filha da tag **`<form>`** e é usada para criar campos onde o usuário pode inserir informações, como texto, números, ou senhas. Esses campos podem ser manipulados diretamente pelo JavaScript para validar, capturar ou alterar os dados inseridos antes do envio.

Um **formulário** (tag `<form>`) é um conjunto de campos interativos, como inputs, botões, caixas de seleção, entre outros. Quando o formulário é enviado, todas as informações preenchidas pelo usuário são coletadas e enviadas para o servidor.

Durante o envio, esses dados **trafegam pela internet**. Se o formulário for enviado por um protocolo **HTTPS** (Hypertext Transfer Protocol Secure), os dados são **criptografados**. A criptografia embaralha as informações, garantindo que, se forem interceptadas, não possam ser lidas ou interpretadas facilmente por terceiros mal-intencionados. Isso protege informações sensíveis como senhas, números de cartão de crédito, e dados pessoais.

Atributos comuns em `<form>` :

- **Atributo `name` :**
    
    
    O atributo `name` é usado para identificar os campos do formulário quando os dados são enviados. No JavaScript, esse atributo facilita a manipulação dos dados, permitindo validar, verificar ou ajustar os valores antes de enviar. Por exemplo, pode-se garantir que um campo de idade não aceite valores absurdos, como números negativos. Exemplo: 
    
    ```html
    <input type="text" name="username">
    ```
    

- **Atributo `action`**:

O atributo `action` define o destino para onde os dados do formulário serão enviados. Normalmente, isso é uma URL que aponta para o servidor que vai processar os dados. Há uma regra de segurança conhecida como **CORS** (Cross-Origin Resource Sharing) que restringe o envio de dados para domínios diferentes daquele que você está acessando, a menos que haja permissões explícitas. Exemplo:
    
    ```html
    <form action="https://meusite.com/processar" method="POST">
    ```
    

- **Atributo `method`**:
    
    O atributo `method` define como os dados do formulário serão enviados ao servidor. Existem dois métodos comuns:
    
    **GET**: Envia os dados anexados à URL, como uma string de consulta (`query string`). Isso não é seguro para dados sensíveis, pois a URL fica visível e pode ser armazenada no histórico do navegador. Exemplo:
    
    ```html
    <form method="GET">
    ```
    

**POST**: Envia os dados no corpo da requisição (body), tornando-os mais seguros, já que eles não aparecem na URL. Ideal para dados confidenciais. Exemplo:

```html
<form method="POST">
```

- **Atributo `target`**:

O atributo `target` especifica onde o resultado do envio do formulário será exibido. O valor **`_blank`** abre a resposta em uma nova aba ou janela do navegador. Exemplo:
    
    ```html
    <form action="/enviar" target="_blank">
    ```
    

- **Atributo `autocomplete`**:

O atributo `autocomplete` pode ter os valores `"on"` ou `"off"`, e indica se o navegador deve ou não armazenar e sugerir valores anteriores inseridos nos campos do formulário. Com o `autocomplete` ativado (`on`), o navegador pode sugerir automaticamente valores previamente digitados. Com ele desativado (`off`), essas sugestões não são mostradas. Exemplo:
    
    ```html
    <input type="text" name="email" autocomplete="on">
    ```
    

- **Atributo `onsubmit`**:

O atributo `onsubmit` define uma ação que será executada quando o formulário for enviado. Geralmente é usado para validar os dados do formulário antes que eles sejam realmente enviados. Com o JavaScript, você pode interceptar o envio, validar os campos e evitar o envio se os dados estiverem incorretos. Exemplo:
    
    ```html
    <form onsubmit="return validarFormulario()">
    ```
    
    E no JavaScript:
    
    ```jsx
    function validarFormulario() {
      const nome = document.forms['meuFormulario']['nome'].value;
      if (nome === "") {
        alert("O campo nome é obrigatório");
        return false;  // Impede o envio
      }
      return true;  // Permite o envio
    }
    ```
    

Esses atributos são fundamentais para controlar como os dados do formulário são manipulados, enviados e processados, garantindo também a segurança e a experiência do usuário ao preencher os formulários.

### Tag input

A tag **`<input>`** é usada para criar campos interativos onde os usuários podem inserir valores, como texto, números, senhas, e muito mais. Existem diferentes tipos de inputs, definidos pelo atributo `type`. 

Cada tipo de input tem suas características e comportamentos específicos, dependendo do navegador. Nem todos os tipos de inputs são totalmente compatíveis com todos os navegadores, principalmente em navegadores mais antigos. Isso acontece porque alguns navegadores podem não suportar certos tipos mais recentes, como `date` ou `color`, que foram introduzidos em versões mais recentes do HTML.

Para garantir que seu site funcione bem em diferentes navegadores, é importante verificar a **compatibilidade** dos tipos de input que você pretende usar. Ferramentas como o **Can I Use** ajudam a verificar a compatibilidade de elementos e atributos HTML em diversos navegadores.

Tipos de inputs:

- **`text`**: Cria um campo para inserção de texto. O usuário pode digitar qualquer valor textual. **Exemplo**:
    
    ```html
    <input type="text" name="nome">
    ```
    
- **`number`**: Aceita apenas números. Você pode definir os atributos `min` e `max` para limitar os valores permitidos. **Exemplo**:
    
    ```html
    <input type="number" name="quantidade" min="1" max="10">
    ```
    
- **`step`**: Usado com o `type="number"`, define o incremento dos valores. Por exemplo, um step de 2 fará com que os valores permitidos sejam pulados de dois em dois. **Exemplo**:
    
    ```html
    <input type="number" name="quantidade" step="2">
    ```
    
- **`button`**: Cria um botão que, por padrão, não envia o formulário. Para manter a semântica do HTML, recomenda-se o uso da tag `<button>` em vez de `<input type="button">`. Você pode definir os tipos `submit` (envia o formulário), `reset` (reseta o formulário), ou `button` (botão genérico para scripts). **Exemplo**:
    
    ```html
    <button type="submit">Enviar</button>
    ```
    
- **`range`**: Cria um controle deslizante (scroll bar) para selecionar valores entre um intervalo mínimo e máximo. Comumente usado para ajustar volumes ou intensidades. **Exemplo**:
    
    ```html
    <input type="range" name="volume" min="0" max="100">
    ```
    
- **`color`**: Exibe um seletor de cores onde o usuário pode escolher uma cor. **Exemplo**:
    
    ```html
    <input type="color" name="cor">
    ```
    
- **`email`**: Valida automaticamente o campo para garantir que o valor inserido seja um endereço de e-mail. Caso contrário, o navegador exibirá uma mensagem de erro. **Exemplo**:
    
    ```html
    <input type="email" name="email">
    ```
    
- **`url`**: Exige que o usuário insira uma URL válida, incluindo o protocolo (como `http://` ou `https://`). Caso contrário, o navegador mostra um alerta. **Exemplo**:
    
    ```html
    <input type="url" name="website">
    ```
    
- **`date`**: Abre um calendário para o usuário selecionar uma data (dia, mês e ano). Nem todos os navegadores oferecem suporte total a este input. **Exemplo**:
    
    ```html
    <input type="date" name="dataNascimento">
    ```
    
- **`week`**: Permite a seleção de uma semana do ano. Funciona em alguns navegadores, mas não no Firefox. **Exemplo**:
    
    ```html
    <input type="week" name="semana">
    ```
    
- **`month`**: Permite a seleção de um mês e ano. Funciona em alguns navegadores, mas não no Firefox. **Exemplo**:
    
    ```html
    <input type="month" name="mes">
    ```
    
- **`checkbox`**: Cria uma caixa de seleção que representa um valor booleano (verdadeiro ou falso). O usuário pode marcar ou desmarcar a caixa. **Exemplo**:
    
    ```html
    <input type="checkbox" name="aceitarTermos"> Aceito os termos
    ```
    
- **`radio` :** Permite a seleção de apenas uma opção em um grupo. Todos os botões de rádio que pertencem ao mesmo grupo devem compartilhar o mesmo atributo `name`. **Exemplo**:
    
    ```html
    <input type="radio" name="sexo" value="masculino"> Masculino
    <input type="radio" name="sexo" value="feminino"> Feminino
    ```
    
- **`file`**: Cria um campo para envio de arquivos. O atributo `multiple` permite que o usuário selecione vários arquivos ao mesmo tempo. **Exemplo**:
    
    ```html
    <input type="file" name="arquivo" multiple>
    ```
    
- **`hidden`**: Cria um campo que não é visível para o usuário, mas que envia dados quando o formulário é submetido. Utilizado para armazenar valores importantes que não devem ser modificados diretamente pelo usuário. **Exemplo**:
    
    ```html
    <input type="hidden" name="userId" value="12345">
    ```
    
- **`search`**: Cria um campo de texto comum com uma funcionalidade adicional: aparece um “X” para limpar o campo de texto. Funciona melhor em navegadores baseados no Google Chrome. **Exemplo**:
    
    ```html
    <input type="search" name="buscar">
    ```
    
- **`password`**: Cria um campo onde o texto inserido é ocultado (normalmente representado por pontos ou asteriscos). Ideal para inserção de senhas. **Exemplo**:
    
    ```html
    <input type="password" name="senha">
    ```
    

Para saber mais sobre os diferentes tipos de inputs e atributos suportados, você pode consultar o site [**W3Schools**](https://www.w3schools.com/), que contém uma vasta documentação sobre HTML, CSS, e JavaScript.

### Checkbox e Radio button

- CheckBox:
    
    O **checkbox** é usado para permitir que o usuário selecione múltiplas opções ao mesmo tempo em um formulário. Ao enviar um formulário com vários checkboxes, podemos capturar todos os valores selecionados utilizando o atributo `name` de forma adequada.
    
    Como enviar múltiplos valores de checkboxes:
    
    Para enviar todos os valores selecionados de uma vez, atribuímos o **mesmo valor ao atributo `name`**, seguido de `[]`, indicando para o back-end que estamos enviando uma **lista de valores**. Dessa forma, todos os checkboxes marcados serão incluídos na requisição e tratados como uma lista de itens. **Exemplo**:
    
    Ao enviar o formulário, se o usuário marcar "Música" e "Tecnologia", o back-end receberá uma lista contendo os valores `["music", "technology"]`.
    
    ```html
    <form action="/submit" method="POST">
      <label><input type="checkbox" name="interests[]" value="music"> Música</label>
      <label><input type="checkbox" name="interests[]" value="sports"> Esportes</label>
      <label><input type="checkbox" name="interests[]" value="technology"> Tecnologia</label>
      <button type="submit">Enviar</button>
    </form>
    ```
    
    O atributo `disabled` no checkbox:
    
    Se quisermos desativar um checkbox (torná-lo não selecionável), podemos usar o atributo `disabled`. Um checkbox desativado não permite interação e o valor dele não será enviado no formulário. **Exemplo**:
    
    ```html
    <input type="checkbox" name="option" value="disabled-option" disabled>
    ```
    

- Radio Button
    
    O **radio button** é utilizado quando se deseja limitar o usuário a **uma única escolha** dentro de um grupo de opções. Ao contrário do checkbox, o radio button só permite selecionar uma opção por vez dentro de um mesmo grupo.
    
    Para agrupar vários radio buttons e garantir que apenas uma opção seja selecionada, utilizamos o **mesmo valor para o atributo `name`** em todos os botões dentro do grupo. Assim, o navegador entende que eles pertencem ao mesmo conjunto de opções, e o usuário poderá escolher apenas um valor. **Exemplo**:
    
    **O que acontece**: O back-end receberá o valor do botão de rádio selecionado, por exemplo, `gender="male"` se o usuário escolher "Masculino".
    
    ```html
    <form action="/submit" method="POST">
      <label><input type="radio" name="gender" value="male"> Masculino</label>
      <label><input type="radio" name="gender" value="female"> Feminino</label>
      <label><input type="radio" name="gender" value="other"> Outro</label>
      <button type="submit">Enviar</button>
    </form>
    ```
    
    O atributo `disabled` no radio button:
    
    Assim como no checkbox, podemos usar o atributo `disabled` em um radio button para impedir que ele seja selecionado. **Exemplo**:
    
    ```html
    <input type="radio" name="option" value="disabled-option" disabled>
    ```
    

### Button

Tipos de Botões em Formulários

- **Botão Normal (`<button>` ou `<input type="button">`)**:
    
    Esse botão é utilizado para realizar ações específicas, mas não tem um comportamento padrão de enviar o formulário. Para torná-lo funcional, precisamos utilizar um evento, como `onclick`, que chama uma função JavaScript quando o botão é clicado. **Exemplo**:
    
    ```html
    <button onclick="minhaFuncao()">Clique aqui</button>
    ```
    
- **Botão de Reset (`<input type="reset">`)**:
    
    Este botão é usado para limpar todos os campos dentro do formulário em que está incluído. Quando clicado, ele redefine todos os inputs para seus valores iniciais (os valores que estavam quando a página foi carregada). **Exemplo**:
    
    ```html
    <input type="reset" value="Limpar Campos">
    ```
    
- **Botão de Submit** **(`<input type="submit">`)**:
    
    Este botão é utilizado para enviar os dados do formulário para o servidor. Quando o botão é clicado, ele aciona o evento `onsubmit` do formulário, que geralmente é utilizado para validações antes de enviar os dados. **Exemplo**:
    
    ```html
    <input type="submit" value="Enviar">
    ```
    
    É importante estar ciente de que pressionar a tecla **Enter** enquanto está em um campo de formulário também ativa o envio do formulário, por isso é essencial implementar validações para evitar erros. As validações devem ser feitas tanto no front-end (JavaScript) quanto no back-end (servidor) para garantir a segurança e a integridade dos dados. 
    
- **Validações e Segurança**
    
    Ao usar o botão de submit, é fundamental validar os campos do formulário:
    
    - **Front-end**: Realize validações básicas para melhorar a experiência do usuário, como verificar se os campos obrigatórios estão preenchidos.
    - **Back-end**: Validações rigorosas devem ser aplicadas no servidor para garantir que os dados sejam válidos e seguros. Isso protege contra tentativas de manipulação de dados e outros ataques.
- **Indicadores de Campos Obrigatórios**
    - É uma boa prática marcar os campos que são obrigatórios com um asterisco (*) ou uma outra forma de destaque, para que os usuários saibam quais informações devem ser preenchidas antes de enviar o formulário. **Exemplo**:
        
        ```html
        <label for="nome">Nome: *</label>
        <input type="text" id="nome" name="nome" required>
        ```
        

### Select

O elemento `<select>` é utilizado para criar uma lista suspensa (dropdown) no formulário, onde o usuário pode escolher entre várias opções predefinidas. Ele é útil quando queremos restringir as opções de entrada a valores específicos, tornando a interface mais controlada e intuitiva.

Estrutura Básica

- O elemento `<select>` contém várias tags `<option>`, que representam as opções disponíveis na lista. Cada opção pode ter um valor associado através do atributo `value`, que será enviado ao servidor quando o formulário for submetido.
- **Exemplo básico**:
    
    ```html
    <label for="estado">Escolha seu estado:</label>
    <select id="estado" name="estado">
        <option value="" disabled selected>Selecione seu estado</option>
        <option value="SP">São Paulo</option>
        <option value="RJ">Rio de Janeiro</option>
        <option value="MG">Minas Gerais</option>
    </select>
    ```
    
- Atributos Importantes
- **`<option>` com Valor Nulo (Placeholder)**:
    
    A primeira opção pode ser um valor "nulo" ou uma opção de instrução, como "Selecione uma opção...". Para garantir que o usuário não escolha essa opção por engano, podemos definir o atributo `disabled` para que ela não seja selecionável, e o atributo `selected` para que seja a primeira opção visível. **Exemplo**:
    
    ```html
    <option value="" disabled selected>Selecione uma opção</option>
    ```
    
- **Atributo `selected`**:
    
    Se quiser que uma opção já apareça como pré-selecionada, você pode usar o atributo `selected` diretamente em uma `<option>`. **Exemplo**:
    
    ```html
    <option value="RJ" selected>Rio de Janeiro</option>
    ```
    
- **Atributo `multiple`**:
    
    O atributo `multiple` permite que o usuário selecione mais de uma opção. Para selecionar várias opções, o usuário precisa segurar a tecla **Ctrl** (ou **Cmd** no Mac) enquanto clica em múltiplas opções. Quando este atributo é utilizado, o campo se comporta como uma lista expandida em vez de uma dropdown comum. **Exemplo**:
    
    ```html
    <label for="frutas">Escolha suas frutas favoritas:</label>
    <select id="frutas" name="frutas[]" multiple>
        <option value="maçã">Maçã</option>
        <option value="banana">Banana</option>
        <option value="laranja">Laranja</option>
        <option value="uva">Uva</option>
    </select>
    ```
    
    Observe que o nome do atributo `name` do `<select>` contém `[]` no final, indicando que uma lista de valores será enviada para o back-end. Isso é essencial para que o servidor reconheça que múltiplas opções foram selecionadas.
    Quando utilizar o atributo `multiple`, é importante garantir que o usuário saiba que pode selecionar mais de uma opção. Geralmente, é uma boa prática explicar isso com um texto auxiliar, como "Segure Ctrl para selecionar mais de uma opção".
    

### Textarea

O `<textarea>` é usado para criar um campo de texto de várias linhas. Os atributos `rows` e `cols` controlam seu tamanho:

- **`rows`**: Define o número de linhas visíveis no campo.
- **`cols`**: Define a largura em termos de caracteres visíveis.

Exemplo:

```html
<textarea rows="4" cols="50"></textarea>
```

Nesse exemplo, a área de texto terá 4 linhas e 50 colunas de largura.

## 2-Estruturando seu HTML +Formatações

### Formatação de textos

A tag `<blockquote>` é usada para citações longas que devem ser destacadas do texto principal. Ela não adiciona automaticamente espaçamento ao texto, mas pode ser estilizada com CSS para incluir espaçamento entre as citações e o restante do conteúdo.

A semântica no HTML refere-se à utilização adequada das tags para descrever corretamente o conteúdo que elas envolvem. Isso ajuda não só na interpretação por parte dos navegadores, mas também por ferramentas de acessibilidade e motores de busca.
A tag `<font>` era utilizada para definir a formatação de fonte diretamente no HTML, mas seu uso não é mais recomendado, pois é considerada obsoleta. A forma moderna de formatar fontes é através do CSS.
Atributos da tag `<font>`:

- `color`: para definir a cor do texto.
- `face`: para especificar a fonte a ser utilizada. Você poderia listar várias fontes em ordem de preferência, como `face="Arial, Helvetica, sans-serif"`. É importante ressaltar que o navegador usará a primeira fonte da lista que estiver instalada no sistema do usuário. Se nenhuma estiver disponível, ele usará a fonte padrão definida pelo navegador.

### Div e Span

**`div`** e **`span`** são conhecidas como "tags coringas" porque não possuem significado semântico próprio. Elas são usadas para delimitar áreas que podem ser estilizadas com CSS:

- **`div`**: É uma tag de **bloco** (display block), ocupando toda a largura disponível. Ela é comumente usada para dividir seções maiores da página, como topo, conteúdo, e rodapé.
- **`span`**: É uma tag **inline**, ou seja, ocupa apenas o espaço necessário no fluxo do texto. É usada para estilizar partes específicas de conteúdo, como palavras ou trechos dentro de um parágrafo.

Estrutura de uma página HTML, uma página web é geralmente organizada com as seguintes seções:

- **Topo**: Pode incluir banners, logotipos, etc.
- **Menu de navegação**: Frequentemente localizado no lado esquerdo.
- **Conteúdo**: Geralmente à direita ou na parte central da página.
- **Rodapé**: Fica na parte inferior da página, contendo informações como links ou direitos autorais.

**Uso de `div` para layout:**

- Dentro de cada seção principal, como topo, conteúdo, e rodapé, **`div`** é usada para criar áreas que podem ser manipuladas com CSS. Cada `div` é um elemento de bloco, ou seja, ocupa a largura total da página horizontalmente.
- **Landing Page:**
    
    Uma **landing page** é uma página web em que todo o conteúdo está concentrado em uma única página, sem navegação para outras páginas. O usuário rola para baixo para acessar todo o conteúdo disponível.
    

### Fieldsets

- **`fieldset`** é uma tag estrutural usada em formulários para agrupar elementos relacionados. Ela cria um contorno ao redor dos campos, melhorando a organização visual para o usuário. Quando combinada com a tag **`legend`**, um título é adicionado ao topo do retângulo, indicando o propósito do grupo de campos.
- **`label`** é uma tag usada para associar um texto descritivo a um campo de formulário, como `input`, `select`, ou `textarea`. Ela é semelhante à tag **`span`**, mas é projetada especificamente para facilitar a interação com os campos de formulário, e geralmente aparece ao lado do campo correspondente.
- **Identar** significa organizar o código com espaçamentos ou recuos (em "escadinha") para torná-lo mais legível e compreensível. Uma boa identação facilita a leitura e manutenção do código.

### Embed

A tag **`<embed>`** era usada anteriormente para incorporar mídias externas ou plugins, como vídeos ou animações Flash, diretamente em páginas web. Embora ainda possa ser encontrada em alguns sites antigos, seu uso é considerado obsoleto.

Hoje em dia, utilizamos tags mais modernas e semânticas, como **`<video>`**, que oferecem mais controle e acessibilidade, além de melhor compatibilidade com navegadores. A tag **`<video>`** suporta vários atributos importantes:

- **`controls`**: Adiciona controles de reprodução, como play/pause, volume, etc.
- **`autoplay`**: Faz o vídeo começar a ser reproduzido automaticamente.
- **`loop`**: Reproduz o vídeo em loop contínuo.
    
    ```html
    <video width="320" height="240" controls autoplay>
      <source src="video.mp4" type="video/mp4">
      Seu navegador não suporta a tag de vídeo.
    </video>
    ```
    

### Iframes

A tag **`<iframe>`** permite incorporar conteúdo de outro site diretamente dentro de uma página web. Com ela, é possível exibir uma página completa, como um mapa do Google Maps ou um vídeo do YouTube, dentro da sua própria página. No entanto, o uso de **`iframe`** pode ter implicações de segurança, pois conteúdo de terceiros pode potencialmente executar scripts maliciosos ou comprometer a privacidade do usuário.

Muitos sites, por questões de segurança, bloqueiam o carregamento de suas páginas dentro de um **`iframe`**, o que impede a exibição de certos conteúdos. Além disso, alguns navegadores e configurações de segurança podem restringir o uso de **`iframe`** para evitar ataques, como o **clickjacking**.

Cuidados com a segurança: 

- **Clickjacking**: Um ataque em que um **`iframe`** malicioso é colocado sobre botões ou links do site, enganando o usuário a clicar no conteúdo malicioso.
- **Política de Conteúdo**: Muitos sites configuram o cabeçalho `X-Frame-Options` para bloquear o uso de seus conteúdos em **`iframe`**.

Bonus: 
Quando você incorpora um vídeo do YouTube usando a tag **`<iframe>`**, o YouTube oferece várias opções de personalização para ajustar o comportamento e a aparência do player.

Opções de personalização do `<iframe>` do YouTube:

- **`start`**: Define o momento específico (em segundos) em que o vídeo deve começar a ser reproduzido. Exemplo: `?start=60` faz o vídeo começar no minuto 1.
- **`controls`**: Define se os controles de reprodução (play, pause, volume, etc.) serão exibidos. Usar `controls=0` remove os controles, enquanto `controls=1` os exibe.
- **`autoplay`**: Faz o vídeo começar automaticamente quando a página carrega. Exemplo: `?autoplay=1`.
- **`mute`**: Inicia o vídeo sem som. Para ativar, use `?mute=1`.
- **`loop`**: Faz com que o vídeo seja reproduzido em loop contínuo. Para isso, o atributo `loop=1` deve ser combinado com a ID do vídeo em **`playlist`** (por exemplo, `?loop=1&playlist=VIDEO_ID`).
- **`fullscreen`**: Permite que o vídeo seja assistido em tela cheia. Para ativar, basta incluir o atributo `allowfullscreen` no iframe.

### Resenha sobre cores

Os navegadores aceitam aproximadamente 140 nomes de cores, mas há outras formas mais precisas de definir cores:

- **RGB (Red, Green, Blue)**: Combinação de vermelho, verde e azul com valores de 0 a 255.
- **HEX (Hexadecimal)**: Representa cores usando números hexadecimais (0-9, A-F), com pares para vermelho, verde e azul.
- **HSL (Hue, Saturation, Lightness)**: Matriz com matiz (hue), saturação e iluminação. O matiz é representado por um ângulo onde 0° é vermelho, 120° é verde e 240° é azul.
- **RGBA**: Igual ao RGB, mas com o canal alpha, que define a transparência (0 = totalmente transparente, 1 = opaco).
- **HSLA**: Igual ao HSL, mas com o canal alpha para transparência.

Exemplos:

- **RGB**: `rgb(255, 0, 0)` (vermelho)
- **HEX**: `#FF0000` (vermelho)
- **HSL**: `hsl(0, 100%, 50%)` (vermelho)
- **RGBA**: `rgba(255, 0, 0, 0.5)` (vermelho com 50% de transparência)

Obs: RGBA e HSLA o ultimo valor vai de 0 a 1, para definir a transparência.

## 3-Trabalhando com mídias utilizando HTML

### Tag img

A tag **`<img>`** é usada para exibir imagens em uma página web. Ela utiliza o atributo **`src`**, que define a URL da imagem. Essa URL pode ser um endereço externo (online) ou o caminho local da imagem no diretório do seu projeto. Se a imagem online for removida ou não estiver disponível, ela não será mais exibida.

Formatos de imagem suportados pela tag `<img>`:

- **GIF**: Suporta animações, mas geralmente são arquivos maiores e podem deixar a página lenta.
- **JPG/JPEG**: Comprime imagens para reduzir o tamanho do arquivo, mas perde qualidade (recomendado para fotos e galerias de imagens).
- **PNG**: Oferece compressão sem perda de qualidade, suporta transparência, sendo ideal para logotipos e imagens com fundo transparente.
- **SVG**: Formato vetorial que não utiliza pixels, o que permite redimensionar sem perda de qualidade. Para melhor controle de SVGs, é recomendável usar a tag **`<svg>`** diretamente.

Atributos importantes da tag `<img>`:

- **`alt`**: Texto alternativo, importante para acessibilidade (leitores de tela para pessoas com deficiência visual) e também exibido quando a imagem não é carregada. Deve descrever a imagem de forma clara.
- **`title`**: Exibe uma mensagem em um balão quando o usuário passa o mouse sobre a imagem. Esse atributo pode ser usado para fornecer informações adicionais, mas não substitui o atributo `alt` para acessibilidade.
    
    ```html
    <img src="logo.png" alt="Logotipo da empresa com fundo transparente" title="Logotipo da empresa">
    ```
    

### Tag áudio

A tag **`<audio>`** é usada para incorporar arquivos de áudio em uma página web e possui suporte nativo nos navegadores modernos, carregando o peso semântico de ser usada para mídia de áudio.

Estrutura e Atributos da Tag `<audio>`:

- **`<source>`**: Tag filha que especifica o caminho do arquivo de áudio através do atributo **`src`** e define o tipo do arquivo com o atributo **`type`**. Você pode incluir várias fontes para garantir que diferentes navegadores consigam reproduzir o áudio (ex.: formatos MP3 e Ogg).
- **`controls`**: Adiciona um player com botões de reprodução, pausa, controle de volume, etc., para o usuário.
- **`autoplay`**: Faz com que o áudio comece a tocar automaticamente assim que a página é carregada.
- **Fallback**: Caso o navegador não suporte a tag `<audio>`, você pode incluir uma mensagem dentro da tag que será exibida, instruindo o usuário.
    
    ```html
    <audio controls autoplay>
      <source src="audio.mp3" type="audio/mpeg">
      <source src="audio.ogg" type="audio/ogg">
      Seu navegador não suporta a reprodução de áudio.
    </audio>
    ```
    

### Tag vídeo

A tag **`<video>`** é usada para incorporar vídeos diretamente em uma página web, utilizando os recursos nativos do navegador. Ela oferece uma solução semântica e acessível para exibir vídeos e permite a inclusão de múltiplos formatos, garantindo que o vídeo seja reproduzido em diferentes navegadores.

Atributos da Tag `<video>`:

- **`controls`**: Exibe os controles nativos do player de vídeo, permitindo ao usuário pausar, reproduzir, ajustar o volume, etc.
- **`autoplay`**: Faz o vídeo começar a ser reproduzido automaticamente quando a página carrega.
- **`loop`**: Faz o vídeo ser reproduzido em loop contínuo.
- **`muted`**: Inicia o vídeo sem som.
- **Fallback**: Caso o navegador não suporte o formato de vídeo ou a tag `<video>`, você pode incluir uma mensagem que será exibida no lugar do vídeo.

Nem todos os navegadores suportam os mesmos formatos de vídeo. O **MP4** é amplamente suportado, mas você pode fornecer formatos alternativos, como **Ogg** e **WebM**, para garantir compatibilidade. O navegador tentará reproduzir o primeiro formato listado e, se não conseguir, tentará o próximo.

Exemplo de uso da tag `<video>`:

```html
<video width="640" height="360" controls>
  <source src="video.mp4" type="video/mp4">
  <source src="video.ogg" type="video/ogg">
  Seu navegador não suporta a reprodução de vídeo.
</video>
```

A tag **`<track>`** é usada em vídeos para adicionar legendas, descrições, capítulos e outros tipos de dados relacionados ao vídeo. Ela é um elemento filho da tag **`<video>`** e permite melhorar a acessibilidade do conteúdo, especialmente para pessoas com deficiência auditiva ou para quem deseja assistir a vídeos em diferentes idiomas.

Atributos da tag `<track>`:

**`src`**: Define o caminho do arquivo de legendas ou descrições (geralmente no formato VTT, como `.vtt`).

**`kind`**: Especifica o tipo de faixa que está sendo adicionada. Pode assumir os seguintes valores:

- **`captions`**: Legendas para deficientes auditivos (descrição completa do que está acontecendo).
- **`subtitles`**: Legendas em outro idioma.
- **`descriptions`**: Descrições auditivas de cenas para deficientes visuais.
- **`chapters`**: Capítulos que ajudam a navegação dentro do vídeo.
- **`metadata`**: Informações não visíveis para o usuário, como metadados sobre o conteúdo.

**`srclang`**: Define o idioma da faixa de legendas (ex.: "en" para inglês, "pt" para português).

**`default`**: Indica qual faixa será carregada como padrão se várias faixas de legenda estiverem disponíveis.

```html
<video controls>
  <source src="video.mp4" type="video/mp4">
  <track src="legenda.vtt" kind="subtitles" srclang="pt" label="Português" default>
  <track src="chapters.vtt" kind="chapters" srclang="en" label="Capítulos">
  Seu navegador não suporta a reprodução de vídeo.
</video>
```

Arquivos VTT:

Os arquivos **VTT** (WebVTT - Web Video Text Tracks) são usados para especificar o tempo exato em que a legenda ou descrição será exibida no vídeo, definindo intervalos de tempo para exibir cada texto. Existem programas que ajudam a gerar esses arquivos automaticamente.

A tag **`<track>`** é fundamental para melhorar a experiência de usuários com necessidades específicas e para oferecer opções de idioma ou navegação dentro de vídeos.

## 4 - Criando tabelas com HTML

## Sobre tabelas

As tabelas em HTML são usadas para organizar dados em um formato tabular, composto por linhas e colunas. Para garantir que as tabelas sejam semânticas e acessíveis, é importante usar corretamente as tags e atributos relacionados.

Estrutura básica das tabelas:

- **`<table>`**: Tag principal que cria a tabela.
- **`<tr>`** (Table Row): Define uma linha na tabela.
- **`<td>`** (Table Data): Representa uma célula normal (dados) dentro de uma linha.
- **`<th>`** (Table Header): Define uma célula de cabeçalho. Células de cabeçalho são importantes para descrever o conteúdo das colunas ou linhas, especialmente para acessibilidade.

Atributos importantes:

- **`border`**: Define a largura da borda ao redor das células.
- **`cellspacing`**: Controla o espaço entre as células da tabela.
- **`cellpadding`**: Define o espaçamento interno das células (distância entre o conteúdo da célula e a borda).
- **`summary`**: Atributo obsoleto em HTML5, mas era usado para fornecer uma descrição da tabela, ajudando na acessibilidade para leitores de tela (similar ao atributo **`alt`** das imagens).

Acessibilidade e boas práticas:

- **`<th>`**: Deve ser usado para cabeçalhos e pode incluir o atributo **`scope`** para indicar se o cabeçalho se aplica a uma linha (`scope="row"`) ou coluna (`scope="col"`).
- **Título e descrição**: Para melhorar a acessibilidade e ajudar leitores de tela a entender o conteúdo da tabela, pode-se usar descrições ou títulos adicionais, embora o uso do atributo **`summary`** tenha sido substituído por outras práticas modernas como **`<caption>`** e **`aria-describedby`**.
- **Semântica**: O uso de **`<th>`** e **`<td>`** com descrições apropriadas garante que a tabela seja interpretada corretamente por leitores de tela.
- **Acessibilidade**: Sempre que possível, fornecer informações que ajudem usuários com deficiência visual a compreender a estrutura e o conteúdo da tabela é essencial.

Em uma tabela HTML, é possível organizar melhor seu conteúdo utilizando as tags **`<thead>`**, **`<tbody>`** e **`<tfoot>`**. Essas tags ajudam a dividir a tabela em seções, facilitando a compreensão e a estilização, além de melhorar a acessibilidade.

Organização de uma tabela:

- **`<thead>`**: Usada para agrupar o cabeçalho da tabela. Contém normalmente as células de cabeçalho (**`<th>`**) que descrevem as colunas.
- **`<tbody>`**: Define o corpo da tabela, onde ficam as linhas de dados (**`<tr>`** contendo **`<td>`**). É a parte principal que pode ser repetida em múltiplas páginas ao imprimir, por exemplo.
- **`<tfoot>`**: Representa o rodapé da tabela, onde informações como totais ou resumos podem ser colocados. Mesmo que apareça antes de **`<tbody>`** no código HTML, será renderizado após o corpo da tabela.

**`<caption>`**:

- A tag **`<caption>`** é usada para fornecer um título ou descrição curta da tabela, que geralmente é exibido acima da tabela, embora seja tecnicamente parte dela. Ela melhora a acessibilidade, ajudando a descrever o propósito da tabela para todos os usuários.

O atributo **`colspan`** em HTML é usado na tag **`<td>`** ou **`<th>`** para fazer com que uma célula ocupe várias colunas em uma tabela. Ele "expande" a célula horizontalmente, mesclando-a com outras células ao lado.

O atributo **`rowspan`** em HTML é utilizado nas tags **`<td>`** ou **`<th>`** para fazer com que uma célula ocupe várias linhas em uma tabela. Ele "expande" a célula verticalmente, mesclando-a com as células abaixo.

# HTML 2: Ampliando o Conhecimento

---

## 1- Entendendo HTML Semântico

### HTML semântica

HTML semântico se refere à prática de usar as tags HTML de forma que elas transmitam claramente o propósito e a estrutura do conteúdo, facilitando tanto para desenvolvedores quanto para navegadores e ferramentas de acessibilidade entenderem o que está sendo apresentado. O HTML5 introduziu novas tags semânticas, como `<header>`, `<article>`, `<section>`, `<footer>`, entre outras, que têm significados específicos e ajudam a descrever melhor o conteúdo da página. Isso torna o HTML mais fácil de interpretar e mais acessível, já que qualquer pessoa, ou sistema que leia o código, consegue identificar rapidamente o papel de cada parte do documento.

### Mudanças HTML 5

No HTML5, novas **tags semânticas** foram criadas para melhorar a estrutura e acessibilidade das páginas web. Essas novas tags ajudam a definir claramente diferentes seções de um documento, facilitando a leitura e a interpretação tanto para desenvolvedores quanto para máquinas, como motores de busca. Aqui estão alguns exemplos:

- **`<main>`**: Define o conteúdo principal do documento, o que é diretamente relacionado ao propósito da página.
- **`<header>`**: Usado para agrupar cabeçalhos e informações introdutórias, como logotipos e menus de navegação.
- **`<footer>`**: Representa o rodapé da página ou de uma seção, onde geralmente ficam informações como direitos autorais e links adicionais.
- **`<nav>`**: Destina-se à navegação, agrupando links de menu ou navegação principal.
- **`<section>`**: Representa uma seção de conteúdo, geralmente com um tema relacionado.
- **`<aside>`**: Usado para conteúdo complementar, como barras laterais ou anúncios.
- **`<article>`**: Ideal para conteúdos independentes que poderiam ser distribuídos ou reutilizados, como posts de blog.
- **`<video>`**: Insere vídeos diretamente no documento HTML.

Esses elementos facilitam a organização de layouts, sem precisar de uso excessivo de `divs`, e tornam o código mais fácil de ler e manter.

Tags que não são mais recomendadas: 

Algumas tags HTML mais antigas foram descontinuadas porque o HTML5 se preocupa principalmente com **estruturação**, deixando a **formatação** para o CSS. Tags como:

- **`<basefont>`**, **`<font>`**: Eram usadas para definir o estilo de fonte diretamente no HTML, algo que hoje é controlado pelo CSS.
- **`<big>`, `<tt>`, `<strike>`**: Serviam para modificar o estilo do texto, mas agora esses efeitos são aplicados via CSS.
- **`<center>`**: Centralizava conteúdo, algo que hoje é feito com propriedades CSS como `text-align`.
- **`<frame>`**, **`<frameset>`**: Eram usados para dividir a tela em diferentes áreas com conteúdo independente, algo que se tornou obsoleto com a introdução de layouts mais modernos e flexíveis no CSS.

Quando você utiliza essas tags descontinuadas em um editor como o **VS Code**, o código ainda funcionará, mas o editor exibirá avisos informando que essas tags estão **obsoletas** ou **deprecated**. Isso significa que, embora ainda possam funcionar em alguns navegadores, elas não são mais recomendadas e podem não ser suportadas em versões futuras. O ideal é sempre seguir os padrões atuais, utilizando as tags semânticas e deixando a formatação de layout e estilo para o **CSS**.

O principal **objetivo do HTML5** é estruturar o conteúdo da página. Ou seja, o HTML cuida da **organização e semântica** do conteúdo, enquanto o **CSS** lida com a **formatação e estilo visual**. Essa separação de responsabilidades torna o código mais limpo, reutilizável e fácil de manter.

Essencialmente, o HTML5 melhora a semântica e a acessibilidade das páginas web, enquanto o CSS é responsável por toda a parte estética.

### Acessibilidade

Acessibilidade no HTML refere-se às práticas e técnicas que tornam o conteúdo web acessível para o maior número possível de pessoas, incluindo aquelas com deficiências visuais, auditivas, motoras ou cognitivas. O objetivo é garantir que todos possam navegar, interagir e consumir o conteúdo da web de maneira eficiente, independentemente de suas limitações.

Princípios de Acessibilidade no HTML

Existem algumas práticas fundamentais que ajudam a melhorar a acessibilidade de um site:

- **Uso de tags semânticas**: Tags como `<header>`, `<nav>`, `<main>`, `<article>`, `<footer>`, entre outras, dão estrutura ao conteúdo, permitindo que leitores de tela e outros assistentes saibam qual é a função de cada parte da página. Isso é importante para que usuários com deficiência visual possam entender a estrutura da página.
- **Texto alternativo em imagens (`alt`)**: Para imagens, sempre deve ser fornecido um texto alternativo com o atributo `alt`. Esse texto descreve a imagem para usuários que não conseguem vê-la, como os que utilizam leitores de tela.
- **Rótulos e legendas para formulários**: Campos de formulários precisam ter rótulos adequados com a tag `<label>`. Isso ajuda usuários de tecnologias assistivas a entenderem o que cada campo exige.
- **Navegação por teclado**: Muitas pessoas utilizam o teclado (em vez de um mouse) para navegar na web. Certifique-se de que os elementos interativos, como links e botões, sejam acessíveis por meio do teclado, utilizando a ordem de tabulação (`tabindex`).
- **Uso correto de cabeçalhos**: Cabeçalhos (`<h1>`, `<h2>`, etc.) devem ser usados em uma hierarquia correta para estruturar o conteúdo. Isso ajuda leitores de tela a entenderem a organização das seções de uma página.
- **Descrições para conteúdo multimídia**: Vídeos e áudios devem incluir legendas ou transcrições para usuários surdos ou com deficiência auditiva, e o elemento `<video>` permite incluir `track` para legendas ou descrições.
- **Uso de ARIA (Accessible Rich Internet Applications)**: ARIA é um conjunto de atributos que melhora a acessibilidade para elementos HTML mais complexos, como menus dinâmicos e sliders. Atributos ARIA como `role`, `aria-label`, `aria-hidden`, entre outros, ajudam tecnologias assistivas a interpretar melhor o conteúdo.

Árvore de Acessibilidade (Accessibility Tree)

A **árvore de acessibilidade** é uma estrutura gerada pelos navegadores a partir da **árvore DOM (Document Object Model)**. Ela é utilizada por **tecnologias assistivas**, como leitores de tela, para interpretar a página web de maneira acessível para usuários com deficiências.

Funcionamento da Árvore de Acessibilidade

- **DOM e árvore de renderização**: Quando uma página é carregada, o navegador constrói a árvore DOM (representação do conteúdo HTML) e a árvore de renderização (responsável por exibir visualmente o conteúdo). A árvore de acessibilidade é derivada dessas duas árvores, mas contém apenas os elementos relevantes para acessibilidade.
- **Elementos filtrados**: A árvore de acessibilidade inclui apenas elementos que são visíveis ou significativos para tecnologias assistivas. Elementos que estão ocultos (por CSS ou `aria-hidden="true"`) ou que não têm valor semântico relevante são excluídos.
- **Informação semântica**: Elementos que possuem informações semânticas importantes, como cabeçalhos (`<h1>`, `<h2>`, etc.), links (`<a>`), botões (`<button>`) e áreas interativas, são processados na árvore de acessibilidade com suas funções específicas, facilitando a navegação por meio de leitores de tela.
- **Atributos ARIA**: Os atributos ARIA influenciam diretamente a árvore de acessibilidade, ajudando a fornecer informações adicionais que não são claramente descritas no HTML padrão. Por exemplo, o atributo `aria-label` pode fornecer uma descrição de um elemento que não tem texto visível.
- **Interação com tecnologias assistivas**: Tecnologias como leitores de tela interagem com a árvore de acessibilidade, utilizando essas informações para criar uma experiência de navegação. Elas "anunciam" o conteúdo, permitem que os usuários naveguem pelo site e interajam com elementos usando atalhos de teclado.

### Web Scraping

Um **crawler**, também conhecido como **web crawler**, **spider** ou **bot**, é um programa automatizado que navega pela internet de maneira sistemática, visitando páginas web, coletando e indexando informações. Seu objetivo principal é descobrir e analisar conteúdo disponível na web, geralmente para construir uma base de dados que será utilizada por motores de busca, como o Google.

**Web scraping** é a técnica de extrair dados de sites de forma automatizada. Ela envolve o uso de programas ou scripts que acessam páginas da web, extraem informações específicas e as organizam de forma estruturada, como em arquivos CSV ou bancos de dados.

Principais Etapas:

- **Acesso ao site**: O scraper envia uma solicitação HTTP para obter o conteúdo da página web.
- **Extração de dados**: O conteúdo da página, geralmente em HTML, é analisado e os dados de interesse são extraídos, usando bibliotecas como BeautifulSoup (Python) ou Cheerio (JavaScript).
- **Tratamento dos dados**: Os dados extraídos são processados, filtrados ou transformados conforme necessário.
- **Armazenamento**: Os dados são salvos em um formato apropriado, como JSON, CSV ou banco de dados.

O **HTML semântico** é extremamente importante no **web scraping** porque facilita a extração de dados, tornando o processo mais eficiente e preciso. Tags semânticas fornecem significado e estrutura ao conteúdo de uma página, permitindo que o scraper entenda melhor o papel de cada elemento. Isso resulta em extrações mais consistentes e menos dependentes de estruturas visuais ou classes CSS que podem mudar frequentemente.

### Main, Header e Footer

O `<header>` é a seção da página usada para agrupar informações introdutórias ou de navegação. Normalmente contém o logo, títulos, menus de navegação e outras informações relacionadas à parte superior de uma página ou seção.

A tag `<main>` representa o conteúdo principal de uma página. Esse conteúdo deve ser único e essencial para o propósito do documento. Por boas práticas, pode haver apenas **um** `<main>` por página, e ele só pode ser filho direto do `<body>`, ou seja, não deve estar dentro de outras tags como `<article>`, `<section>`, ou `<div>`.

O `<footer>` é a seção que contém o rodapé da página ou de uma seção específica. Geralmente inclui informações como direitos autorais, links adicionais ou contatos. O `<footer>` pode aparecer no final de uma página inteira ou no final de uma seção dentro da página.

A tag `<address>` é usada para fornecer informações de contato ou autoria de um documento. Quando usada dentro de um `<footer>`, ela é comumente utilizada para exibir informações de contato, como endereço, e-mail ou telefone, relacionados à empresa ou ao responsável pela página.

### Aside, section e nav

A tag **`<section>`** é usada para definir uma seção genérica de conteúdo dentro de uma página. Ela agrupa partes relacionadas do conteúdo, como capítulos de um artigo, tópicos ou segmentos de uma página. O `<section>` é uma tag semântica, o que significa que o conteúdo dentro dela é uma parte logicamente relacionada, geralmente com um título associado.

A tag **`<nav>`** representa uma área de **navegação** dentro de um site ou uma página. Ela contém links de navegação principais ou secundários, como menus, barras laterais de navegação ou links internos. Um `<nav>` pode ser usado para agrupar links que ajudam os usuários a se moverem pelo site, e não deve ser utilizado para qualquer conjunto de links, mas sim para seções de navegação.

A tag **`<aside>`** é usada para conteúdo **secundário ou complementar** ao conteúdo principal. Geralmente, o `<aside>` é utilizado para exibir informações adicionais, como barras laterais com links, citações, propagandas ou dados relacionados ao que está sendo apresentado na página. O conteúdo do `<aside>` está conectado ao conteúdo principal, mas pode ser considerado separável.

Diferença entre as tags:

- **`<section>`** é usada para agrupar conteúdo que está relacionado de forma temática, podendo ser parte do conteúdo principal.
- **`<nav>`** é usada para criar blocos de links de navegação que ajudam o usuário a se orientar no site.
- **`<aside>`** serve para exibir conteúdo complementar ou relacionado ao conteúdo principal, mas que não é essencial para a compreensão do tema central da página.

### Article, Blockquote e Q

A tag **`<blockquote>`** é usada para indicar **citações em bloco**. Ela é geralmente usada para citações longas que são destacadas do texto principal, e o navegador pode aplicar um recuo ou outro estilo visual para diferenciá-las. As citações dentro de `<blockquote>` são frequentemente acompanhadas pelo autor ou fonte, que pode ser indicado usando o atributo `cite`.

```html
<blockquote cite="https://exemplo.com/citacao">
  "Esta é uma citação de várias linhas que pode ser formatada com recuo."
</blockquote>
```

A tag **`<article>`** representa um **conteúdo independente e completo**, como um artigo de blog, uma notícia, uma postagem em fórum ou qualquer outra parte do conteúdo que pode ser reutilizada ou distribuída separadamente. O conteúdo dentro de `<article>` deve fazer sentido por si só, sem depender do restante da página.

```html
<article>
  <h2>Título do Artigo</h2>
  <p>Este é o conteúdo do artigo. Ele pode ser lido de forma independente.</p>
</article>
```

A tag **`<q>`** é usada para representar **citações curtas e inline** (dentro de uma linha de texto). Diferente de `<blockquote>`, que é usada para citações longas e destacadas, o `<q>` geralmente envolve citações rápidas, e os navegadores costumam adicionar aspas automaticamente ao redor do conteúdo.

```html
<p>Ela disse, <q>Estamos prontos para começar o projeto.</q></p>
```

Diferença entre as tags:

- **`<blockquote>`** é para **citações longas** e destacadas do texto principal.
- **`<article>`** define **conteúdo autossuficiente**, como um artigo ou notícia.
- **`<q>`** é para **citações curtas** inseridas diretamente em uma frase.

### Figure, Figcaption e picture

A tag **`<figure>`** é usada para agrupar elementos de mídia, como imagens, gráficos, ou ilustrações, e qualquer outro conteúdo que seja relevante, mas que pode ser movido ou reposicionado na página sem afetar o entendimento principal. Geralmente, o `<figure>` é acompanhado por uma legenda (usando `<figcaption>`), que descreve o conteúdo visual.

```html
<figure>
  <img src="imagem.jpg" alt="Descrição da imagem">
  <figcaption>Legenda explicando o conteúdo da imagem</figcaption>
</figure>
```

A tag **`<figcaption>`** é usada dentro de um `<figure>` para fornecer uma **legenda** ou descrição do conteúdo agrupado. Ela deve ser colocada no início ou no final da tag `<figure>`. O `<figcaption>` dá contexto adicional ao conteúdo da mídia, melhorando a acessibilidade e a compreensão.

```html
<figure>
  <img src="paisagem.jpg" alt="Paisagem de montanhas ao pôr do sol">
  <figcaption>Uma bela paisagem de montanhas ao pôr do sol.</figcaption>
</figure>
```

A tag **`<picture>`** permite que diferentes **versões de uma imagem** sejam exibidas dependendo do contexto, como o tamanho da tela, a densidade de pixels ou outros fatores. O `<picture>` é usado para fornecer alternativas otimizadas da mesma imagem, melhorando o desempenho e a responsividade do site. Ele usa a tag `<source>` para definir diferentes formatos ou resoluções da imagem, e o `<img>` como fallback para navegadores que não suportam `<picture>`.

```html
<picture>
  <source media="(min-width: 800px)" srcset="imagem-grande.jpg">
  <source media="(max-width: 799px)" srcset="imagem-pequena.jpg">
  <img src="imagem-default.jpg" alt="Imagem responsiva">
</picture>
```

Diferença entre as tags: 

- **`<figure>`** é usada para agrupar conteúdo de mídia, como imagens ou gráficos, com uma legenda opcional.
- **`<figcaption>`** fornece uma legenda descritiva para o conteúdo dentro do `<figure>`.
- **`<picture>`** permite o uso de diferentes versões de uma imagem para se adaptar a diferentes condições (como tamanho da tela ou formato), sendo útil para layouts **responsivos**.

### SEO (Search Engine Optimization)

**SEO** (Search Engine Optimization) é o processo de otimização de um site para melhorar sua **visibilidade nos motores de busca** como o Google, aumentando as chances de aparecer em melhores posições nos resultados de pesquisa orgânica (não paga). O objetivo do SEO é atrair mais tráfego qualificado para o site, tornando-o mais fácil de ser encontrado pelos usuários que buscam por termos relacionados ao seu conteúdo ou serviços.

## 2 - HTML: Recursos especiais

### Datalist

A tag **`<datalist>`** é usada para fornecer uma lista de opções predefinidas para um campo de entrada (**`<input>`**). Ela permite que os usuários escolham uma opção da lista ou insiram seus próprios valores. Essa tag é muito útil quando você quer sugerir opções, mas também quer permitir flexibilidade para o usuário digitar algo diferente.

O `<datalist>` é conectado a um campo de entrada (`<input>`) por meio do atributo `list` no `<input>`, que deve ter o mesmo valor que o `id` da tag `<datalist>`.

```html
<label for="frutas">Escolha uma fruta:</label>
<input list="frutas" id="fruta" name="fruta" placeholder="Digite ou selecione uma fruta">

<datalist id="frutas">
  <option value="Maçã">
  <option value="Banana">
  <option value="Laranja">
  <option value="Manga">
</datalist>
```

### Code, kbd e pre

A tag **`<code>`** é usada para representar **trechos de código** em um documento HTML. Ela exibe o texto em uma fonte monoespaçada, diferenciando visualmente o código do restante do conteúdo. No entanto, não preserva a formatação de espaços e quebras de linha.

A tag **`<pre>`** é usada para exibir **texto pré-formatado**. Ela preserva espaços, quebras de linha e tabulações exatamente como estão no código-fonte, tornando-a ideal para exibir blocos de texto ou código que exigem formatação específica. Ela é frequentemente combinada com a tag `<code>` para exibir blocos de código com formatação apropriada.

A tag **`<kbd>`** é usada para representar **entrada de teclado** ou comandos digitados pelo usuário. O conteúdo dentro da tag `<kbd>` é exibido em uma fonte monoespaçada, sugerindo que a pessoa deve digitar o texto mostrado.

Uma **fonte monoespaçada** (ou **monoespace**) é um tipo de fonte em que **todos os caracteres ocupam a mesma quantidade de espaço horizontal**, independentemente de serem letras, números ou símbolos. Em fontes monoespaçadas, cada caractere tem a mesma largura, o que contrasta com fontes proporcionais, onde a largura de cada caractere pode variar.

### Details e Summary

As tags **`<details>`** e **`<summary>`** são usadas para criar um elemento interativo que o usuário pode expandir ou recolher para exibir ou ocultar conteúdo adicional. Elas são especialmente úteis para mostrar informações que o usuário pode querer visualizar sob demanda, como FAQs, descrições detalhadas ou seções informativas.

A tag **`<details>`** é usada para criar uma seção que pode ser **expandida ou recolhida**. Por padrão, o conteúdo dentro do `<details>` está oculto e só é revelado quando o usuário clica na seta de expansão.

A tag **`<summary>`** é usada dentro do `<details>` para fornecer um **título ou rótulo** que descreve o conteúdo a ser expandido ou recolhido. O texto do `<summary>` é o que o usuário vê e clica para expandir ou recolher a seção de detalhes. Se a tag `<summary>` não for usada, o conteúdo do `<details>` ainda poderá ser expandido, mas sem um título visível.

```html
<details>
  <summary>O que é HTML?</summary>
  <p>HTML (HyperText Markup Language) é a linguagem de marcação usada para criar páginas web.</p>
</details>

<details open>
  <summary>O que é CSS?</summary>
  <p>CSS (Cascading Style Sheets) é uma linguagem de estilo usada para definir a aparência de uma página web.</p>
</details>
```

### Meter e progress

As tags **`<progress>`** e **`<meter>`** são usadas para representar valores medidos ou indicativos em uma página HTML, mas cada uma com um propósito específico. Elas são frequentemente usadas para mostrar progresso ou estado visualmente, de uma maneira semântica e acessível.

A tag **`<progress>`** é usada para representar o **progresso de uma tarefa**, geralmente em termos de uma porcentagem concluída. Ela exibe uma barra de progresso que pode ser atualizada dinamicamente, mostrando o quanto de uma tarefa já foi completado.
Atributos: 

- **`value`**: O valor atual do progresso.
- **`max`**: O valor máximo, ou o total que a tarefa precisa atingir. O valor padrão é 1.0 se não especificado.

```html
<progress value="70" max="100"></progress>
```

A tag **`<meter>`** é usada para representar um **valor dentro de uma faixa conhecida**, como medições de temperatura, níveis de bateria, ou resultados de um teste de desempenho. Diferente do `<progress>`, o `<meter>` é usado para indicar uma quantidade que não necessariamente está ligada a uma tarefa em andamento.

Atributos:

- **`value`**: O valor atual a ser representado.
- **`min`** (opcional): O valor mínimo da faixa.
- **`max`** (opcional): O valor máximo da faixa.
- **`low`** (opcional): Um valor indicando o limite para valores baixos.
- **`high`** (opcional): Um valor indicando o limite para valores altos.
- **`optimum`** (opcional): O valor considerado ideal ou desejado.

```html
<meter value="0.7" min="0" max="1" low="0.3" high="0.9" optimum="0.8"></meter>
```

### Canvas

A tag **`<canvas>`** é usada para **desenhar gráficos e elementos visuais** diretamente em uma página web por meio de **JavaScript**. Ela cria uma área de desenho em 2D ou 3D onde você pode gerar imagens, gráficos, animações e até mesmo jogos. Sozinha, a tag `<canvas>` não exibe nada; todo o conteúdo dentro dela deve ser manipulado por scripts.

Características principais:

- **Área de desenho**: O `<canvas>` cria uma área retangular onde gráficos podem ser renderizados.
- **Manipulação via JavaScript**: Todo o conteúdo desenhado no canvas é gerado dinamicamente por código JavaScript, utilizando métodos da API de contexto gráfico, como `getContext("2d")`.
- **Versatilidade**: Pode ser usada para criar gráficos interativos, jogos, editores de imagem, animações, entre outros.

### Atributos novos do HTML5

- **`autofocus`**: Coloca o foco automaticamente em um elemento quando a página é carregada, geralmente em formulários para facilitar a interação do usuário.
- **`placeholder`**: Exibe um texto temporário dentro de um campo de input, fornecendo uma dica ou exemplo sobre o tipo de dado esperado.
- **`required`**: Indica que o campo de input deve ser preenchido antes de o formulário ser enviado, tornando-o obrigatório.
- **`fieldset` e `input disabled`**:
    - **`fieldset`**: Agrupa elementos de um formulário para organizá-los logicamente e estilisticamente.
    - **`disabled`**: Quando aplicado a um campo de input, desativa o campo, impedindo que ele seja editado ou enviado com o formulário.
- **`textarea minlength` e `maxlength`**:
    - **`minlength`**: Define o número mínimo de caracteres que o usuário deve digitar em um campo de texto.
    - **`maxlength`**: Define o número máximo de caracteres permitidos em um campo de texto.

# Diretórios (Caminhos/path)

---

## **Caminhos absolutos e relativos**

### Caminho Absolutos