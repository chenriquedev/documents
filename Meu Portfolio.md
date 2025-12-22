
## Projeto Guiado

Ao final desse documento você será capaz de entender os principais conceitos do desenvolvimento de sites, bem como ter seu portfolio funcional.

##  Parte 1: Preparando o ambiente 📁

Para começar, devemos criar uma pasta no computador e dentro dela os arquivos necessários:

1. Criar uma pasta com nome `projeto-portfolio`
2. Dentro dela, crie um arquivo chamado `index.html`
3. Dentro dela, crie um arquivo chamado `index.css`
4. Crie também um arquivo chamado `reset.css`
5. E por fim, crie uma pasta chamada `imagens` para armazenar as imagens do projeto 

Seu projeto deve ficar assim:

📁 projeto-portfolio
├─ 📁 images
├─ :dev_html5_original: index.html
├─ :dev_css3_original: index.css
└─ :dev_css3_original: reset.css

## Parte 2: O Esqueleto HTML :dev_html5_original:

Para começar a desenvolver o nosso projeto, devemos primeiro montar o esqueleto inicial do HTML, onde teremos todo o conteúdo, como textos e imagens.

Como aprendemos em aula, utilizamos o atalho `!` para gerar o esqueleto inicial:

```html
<!DOCTYPE html>
<html lang="en">
	<head>
	    <meta charset="UTF-8">
	    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	    <title>Document</title>
	</head>
	<body>
	    
	</body>
</html>
```

Vamos adicionar umas configurações iniciais nesse documento

```html
<!DOCTYPE html>
<html lang="pt-br"> <!--Mudamos o idioma da pagina para pt-br-->
	<head>
	    <meta charset="UTF-8">
	    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	    <!--Aqui adicionamos uma descrição para esse arquivo HTML-->
	    <meta name="description" content="Meu portfólio">
	    <title>Portfólio</title> <!--Alteramos o título da página-->
	     <!--Aqui vamos adicionar os links do CSS. Lembrando que o reset.css deve ficar em cima do index.css para evitar bugs visuais-->
	    <link rel="stylesheet" href="reset.css">
	    <link rel="stylesheet" href="index.css">
	</head>
	<body>
	    
	</body>
</html>
```

Ainda não temos nada visual no nosso projeto, pois o elemento `body` está vazio.
Antes de continuar vamos estruturar as seções do site e vamos incluir ID nas seções do site. 

```html
<!DOCTYPE html>
<html lang="pt-br">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta name="description" content="Meu portfólio">
        <title>Portfólio</title> 
        <link rel="stylesheet" href="reset.css">
        <link rel="stylesheet" href="index.css">
    </head>

    <body>
        <header id="header">
            <nav id="navbar">
            </nav>
        </header>
        <main>
            <section id="inicio">
            </section>

            <section id="habilidades">
            </section>

            <section id="projetos">
            </section>

            <section id="contato">
            </section>
        </main>
        <footer>
        </footer>
    </body>
</html>
```

Com isso temos o arquivo HTML configurado e estruturado, pronto para receber o conteúdo.

## Parte 3: O Reset CSS :dev_css3_original: 

Antes de prosseguir com o desenvolvimento do projeto, vamos remover aquela margin e padding que os navegadores tem por padrão. Para isso, basta colar o código a seguir dentro do arquivo `reset.css`

```css
/*O asterisco significa TODOS os elementos*/
* {
  margin: 0; /*Zeramos o margin de todos os elementos*/
  padding: 0; /*Zeramos o padding de todos os elementos*/
  box-sizing: border-box;
  text-decoration: none; /*Removemos aquela linha dos links*/
  list-style: none; /*Removemos aquelas bolinhas da lista*/
}
```

## Parte 4: Instalando Ferramentas (fontes e ícones) :hammer_and_wrench: 

#### Instalando a fonte

Para a construção desse projeto foi utilizado uma fonte externa, chamada `Inter`. Como não temos ela por padrão precisamos importar ela. Para isso, devemos acessar o site do  [Google Fonts](https://fonts.google.com/) e buscar a fonte `Inter`.

Ao clicar no link você será redirecionado para o site do Google Fonts.

<div>
	<img src="../imagens/googlefontsinicio.png" alt="tela inicial do google fonts">
</div>

Na barra de pesquisa devemos buscar a fonte `Inter`

<div>
	<img src="../imagens/googlefontssearch.png" alt="buscando a fonte inter no site google fonts">
</div>

Vamos selecionar a primeira opção, onde tem o nome da fonte `Inter`

<div>
	<img src="../imagens/fontselected.png" alt="Fonte selecionada">
</div>

Quando selecionamos a fonte somos transferidos para essa tela que possui informações daquela fonte como o estilo dela e o peso dela `(weight)`. Para prosseguir devemos clicar no botão superior esquerdo que tem escrito `Get Font`.

<div>
	<img src="../imagens/fontselectedtodownload.png" alt="Fonte selecionada para baixar">
</div>

Nessa etapa estamos vendo informações tipo, quantas fontes selecionamos e o site nos fornece duas opções para essa fonte, baixar ou pegar o código para inserir no arquivo HTML ou CSS. Para prosseguir. selecionamos a opção `<> Get Embed Code` ou `<> obter código de incorporação` caso o site esteja em português.

<div>
	<img src="../imagens/optionsgooglefonts.png" alt="Opções para incorporar a fonte">
</div>

Nessa parte temos a opção de pegar o código por meio da tag `<link>` e também temos a opção de usar por meio de `@import`.

Se escolher usar por meio da tag `<link>`, o código fornecido deverá ser incluido dentro da tag `HEAD` do html. 

No nosso caso iremos escolher a opção `@import`, pois basta colocar no topo do nosso arquivo `index.css` para funcionar.

<div>
	<img src="../imagens/importfont.png" alt="Opções para incorporar a fonte">
</div>

```css
/*Aqui importamos a fonte Inter direto do Google Fonts*/
@import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap');

html {
	/*Agora aplicamos a fonte em todo o documento HTML*/
	font-family: "Inter", sans-serif;
}
```

#### Instalando a biblioteca de ícones

Agora que instalamos a fonte vamos instalar uma biblioteca de ícones. Vamos escolher a biblioteca phosphor icons. 

Para instalar ela basta incluir essas duas tags `<link>` dentro da tag `<head>`

```html
<head>
    <link
      rel="stylesheet"
      type="text/css"
      href="https://cdn.jsdelivr.net/npm/@phosphor-icons/web@2.1.1/src/regular/style.css"
    />
    <link
      rel="stylesheet"
      type="text/css"
      href="https://cdn.jsdelivr.net/npm/@phosphor-icons/web@2.1.1/src/fill/style.css"
    />
</head>
```

Agora nosso Arquivo HTML ficará assim:

```html
<!DOCTYPE html>
<html lang="pt-br">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta name="description" content="Meu portfólio">
        <title>Portfólio</title> 
        <link rel="stylesheet" href="reset.css">
        <link rel="stylesheet" href="index.css">
        <link
      rel="stylesheet"
      type="text/css"
      href="https://cdn.jsdelivr.net/npm/@phosphor-icons/web@2.1.1/src/regular/style.css"
    />
    <link
      rel="stylesheet"
      type="text/css"
      href="https://cdn.jsdelivr.net/npm/@phosphor-icons/web@2.1.1/src/fill/style.css"
    />
    </head>

    <body>
        <header id="header">
            <nav id="navbar">
            </nav>
        </header>
        <main>
            <section id="inicio">
            </section>

            <section id="habilidades">
            </section>

            <section id="projetos">
            </section>

            <section id="contato">
            </section>
        </main>
        <footer>
        </footer>
    </body>
</html>
```

## Parte 5: Preenchendo o Cabeçalho :dev_html5_original:

Agora que temos tudo configurado, o próximo passo será Preencher o cabeçalho.

No arquivo HTML, localize a tag `<header id="header">` que está vazia, apenas com uma tag `nav` dentro, e coloque esse código.

```html
<header id="header">
    <div class="logo">
	    <!--Essa imagem você pode encontrar no link do FIGMA-->
        <img src="" alt="logo do site">
    </div>

    <nav id="navbar">
        <ul>
            <li><a href="#inicio">Início</a></li>
            <li><a href="#habilidades">Habilidades</a></li>
            <li><a href="#projetos">Meus Projetos</a></li>
            
            <li><a href="#contato" class="btn-contato">Contato</a></li>
        </ul>
    </nav>
</header>
```

E pronto. Isso é o que precisamos até agora. Parabéns, você acaba de definir o cabeçalho do site.

## Parte 6: Preenchendo o inicio :dev_html5_original:

Essa é a parte principal do site, é a primeira seção que o usuário ver quando entra no site. No nosso caso, a seção inicio é dividida em dois lados, na esquerda com textos e botões, e na direita com a imagem.

No arquivo HTML localize a tag `<section id="inicio">` e coloque o código a seguir:

```html
<section id="inicio">
    <div class="hero-texto">
        <h1>SEU NOME <br> AQUI</h1>
        <p>Web Developer e Designer de Interfaces focado em criar experiências digitais incríveis.</p>
        
        <div class="hero-botoes">
            <a href="#projetos" class="btn-primario">Meus Projetos</a>
            
            <div class="redes-sociais">
                <a href="#"><i class="ph-fill ph-linkedin-logo"></i></a>
                <a href="#"><i class="ph-fill ph-github-logo"></i></a>
                <a href="#"><i class="ph-fill ph-instagram-logo"></i></a>
            </div>
        </div>
    </div>

    <div class="hero-imagem">
	    <!--A imagem daqui voce consegue pegar no FIGMA-->
        <img src="imagens/ilustracao.png" alt="Ilustração de um programador">
    </div>
</section>
```

Parabéns, agora temos 2 componentes prontos do nosso site, o Cabeçalho e a seção Inicio.

## Parte 7: Preenchendo a seção Habilidades :dev_html5_original:

Nosso próximo passo é criar a estrutura da seção de habilidades, ou seja, vamos mostrar o que você sabe fazer, quais tecnologias você conhece. Para isso, no arquivo HTML, localize a tag `<section id="habilidades">` e colar o código abaixo dentro dela.

```html
<section id="habilidades">
    <h2 class="titulo-secao">Minhas Habilidades</h2>

    <div class="habilidades-grid">
        
        <div class="card">
            <i class="ph ph-file-html"></i>
            <h3>HTML 5</h3>
            <p>Criação de estrutura semântica para sites.</p>
        </div>

        <div class="card">
            <i class="ph ph-palette"></i>
            <h3>CSS 3</h3>
            <p>Estilização, layout responsivo e animações.</p>
        </div>

        <div class="card">
            <i class="ph ph-brackets-curly"></i>
            <h3>JavaScript</h3>
            <p>Interatividade e lógica de programação.</p>
        </div>

        <div class="card">
            <i class="ph ph-atom"></i>
            <h3>React.js</h3>
            <p>Criação de interfaces baseadas em componentes.</p>
        </div>

        <div class="card">
            <i class="ph ph-git-branch"></i>
            <h3>Git & GitHub</h3>
            <p>Versionamento de código e trabalho em equipe.</p>
        </div>

        <div class="card">
            <i class="ph ph-code"></i>
            <h3>TypeScript</h3>
            <p>Códigos mais seguros e tipagem estática.</p>
        </div>

    </div>
</section>
```

Aqui usamos a classe  card, `class="card"`, 6 vezes por que todos os elementos terão o mesmo estilo visual. Usamos também a tag `<i>` pois são padrões na biblioteca que instalamos, o Phosphor Icons, para incluir ícones no nosso projeto.

Parabéns, acabamos de incluir a seção de habilidades do nosso projeto.

## Parte 8: Preenchendo a seção Projetos :dev_html5_original:

Nessa parte iremos colocar os projetos que você já fez, ou pode citar um projeto qualquer, para fazer parte do seu portfólio. A ideia aqui é demonstrar o que você já criou.

Para isso, no arquivo HTML localize a tag `<section id="projetos">` e cole o código a seguir:

```html
<section id="projetos">
    <h2 class="titulo-secao">Meus Projetos</h2>

    <div class="projetos-grid">
        
        <div class="card-projeto">
            <div class="img-box">
                <img src="imagens/projeto1.png" alt="Print do projeto">
            </div>
            
            <div class="projeto-info">
                <h3>Landing Page</h3>
                <p>Uma página de vendas com design moderno e responsivo.</p>
                
                <div class="tags">
                    <span>HTML</span>
                    <span>CSS</span>
                </div>

                <div class="botoes-projeto">
                    <a href="#">Ver Site</a>
                    <a href="#">Código</a>
                </div>
            </div>
        </div>

        <div class="card-projeto">
            <div class="img-box">
                <img src="imagens/projeto2.png" alt="Print do projeto">
            </div>
            
            <div class="projeto-info">
                <h3>Dashboard</h3>
                <p>Painel administrativo para controle de tarefas.</p>
                
                <div class="tags">
                    <span>React</span>
                    <span>JS</span>
                </div>

                <div class="botoes-projeto">
                    <a href="#">Ver Site</a>
                    <a href="#">Código</a>
                </div>
            </div>
        </div>

        <div class="card-projeto">
            <div class="img-box">
                <img src="imagens/projeto3.png" alt="Print do projeto">
            </div>
            
            <div class="projeto-info">
                <h3>Blog Pessoal</h3>
                <p>Blog minimalista para postagem de artigos técnicos.</p>
                
                <div class="tags">
                    <span>HTML</span>
                    <span>CSS</span>
                </div>

                <div class="botoes-projeto">
                    <a href="#">Ver Site</a>
                    <a href="#">Código</a>
                </div>
            </div>
        </div>

    </div>
</section>
```

Caso você não tenha projetos ainda, pode inventar um e colocar imagens encontradas no google.

> [!INFO] Dica
> Se vocês ainda não tiverem as imagens dos projetos não tem problema. O ícone de 'imagem quebrada' vai aparecer, e o alt também. Depois basta colocar as imagens na pasta correta


## Parte 9: Preenchendo a seção Contato :dev_html5_original:

Essa é, finalmente, a ultima seção do site, onde colocamos cartões grandes chamando para conversar (Email, LinkedIn, WhatsApp)

No arquivo HTML, localize a tag `<section id="contato">` e cole o código:

```html
<section id="contato">
    <div class="contato-header">
        <h2 class="titulo-secao">Vamos Conversar?</h2>
        <p>Gostou do meu portfólio? Entre em contato para construirmos algo juntos.</p>
    </div>

    <div class="contato-grid">
        
        <div class="card-contato">
            <i class="ph ph-envelope-simple"></i>
            <h3>Email</h3>
            <a href="mailto:seuemail@gmail.com">Enviar mensagem</a>
        </div>

        <div class="card-contato">
            <i class="ph ph-linkedin-logo"></i>
            <h3>LinkedIn</h3>
            <a href="#" target="_blank">Conectar</a>
        </div>

        <div class="card-contato">
            <i class="ph ph-whatsapp-logo"></i>
            <h3>WhatsApp</h3>
            <a href="#" target="_blank">Falar agora</a>
        </div>

    </div>
</section>
```

## Parte 10: Preenchendo o rodapé :dev_html5_original:

Nosso site começou com um header, onde temos a nossa logo e um menu de navegação, nada mais justo que deveremos ter um rodapé, para deixar nosso site completo.

Localize a tag `<footer>`, ela deve ser a última tag dentro do body, e cole:

```html
<footer>
    <p>© Todos os direitos reservados - 2025</p>
    <p>Desenvolvido por <strong style="color: #7c3aed;">SEU NOME</strong></p>
</footer>
```

Parabéns, você acaba de estruturar toda a página HTML, além que fez as configurações necessárias. Agora partiremos para o CSS, onde deixaremos tudo bonito.

**Código HTML até o momento**

```html
<!DOCTYPE html>
<html lang="pt-br">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta name="description" content="Meu portfólio">
        <title>Portfólio</title> 
        <link rel="stylesheet" href="reset.css">
        <link rel="stylesheet" href="index.css">
        <link
      rel="stylesheet"
      type="text/css"
      href="https://cdn.jsdelivr.net/npm/@phosphor-icons/web@2.1.1/src/regular/style.css"
    />
    <link
      rel="stylesheet"
      type="text/css"
      href="https://cdn.jsdelivr.net/npm/@phosphor-icons/web@2.1.1/src/fill/style.css"
    />
    </head>

    <body>
        <header id="header">
		    <div class="logo">
	    <!--Essa imagem você pode encontrar no link do FIGMA-->
		        <img src="" alt="logo do site">
		    </div>

		    <nav id="navbar">
		        <ul>
		            <li><a href="#inicio">Início</a></li>
		            <li><a href="#habilidades">Habilidades</a></li>
		            <li><a href="#projetos">Meus Projetos</a></li>
		            
		            <li><a href="#contato" class="btn-contato">Contato</a></li>
		        </ul>
		    </nav>
		</header>
        <main>
            <section id="inicio">
			    <div class="hero-texto">
			        <h1>SEU NOME <br> AQUI</h1>
			        <p>Web Developer e Designer de Interfaces focado em criar experiências digitais incríveis.</p>
			        
			        <div class="hero-botoes">
			            <a href="#projetos" class="btn-primario">Meus Projetos</a>
			            
			            <div class="redes-sociais">
			                <a href="#"><i class="ph-fill ph-linkedin-logo"></i></a>
			                <a href="#"><i class="ph-fill ph-github-logo"></i></a>
			                <a href="#"><i class="ph-fill ph-instagram-logo"></i></a>
			            </div>
			        </div>
			    </div>
			
			    <div class="hero-imagem">
				    <!--A imagem daqui voce consegue pegar no FIGMA-->
			        <img src="imagens/ilustracao.png" alt="Ilustração de um programador">
			    </div>
			</section>

            <section id="habilidades">
			    <h2 class="titulo-secao">Minhas Habilidades</h2>
			
			    <div class="habilidades-grid">
			        
			        <div class="card">
			            <i class="ph ph-file-html"></i>
			            <h3>HTML 5</h3>
			            <p>Criação de estrutura semântica para sites.</p>
			        </div>
			
			        <div class="card">
			            <i class="ph ph-palette"></i>
			            <h3>CSS 3</h3>
			            <p>Estilização, layout responsivo e animações.</p>
			        </div>
			
			        <div class="card">
			            <i class="ph ph-brackets-curly"></i>
			            <h3>JavaScript</h3>
			            <p>Interatividade e lógica de programação.</p>
			        </div>
			
			        <div class="card">
			            <i class="ph ph-atom"></i>
			            <h3>React.js</h3>
			            <p>Criação de interfaces baseadas em componentes.</p>
			        </div>
			
			        <div class="card">
			            <i class="ph ph-git-branch"></i>
			            <h3>Git & GitHub</h3>
			            <p>Versionamento de código e trabalho em equipe.</p>
			        </div>
			
			        <div class="card">
			            <i class="ph ph-code"></i>
			            <h3>TypeScript</h3>
			            <p>Códigos mais seguros e tipagem estática.</p>
			        </div>
			
			    </div>
			</section>

            <section id="projetos">
			    <h2 class="titulo-secao">Meus Projetos</h2>
			
			    <div class="projetos-grid">
			        
			        <div class="card-projeto">
			            <div class="img-box">
			                <img src="imagens/projeto1.png" alt="Print do projeto">
			            </div>
			            
			            <div class="projeto-info">
			                <h3>Landing Page</h3>
			                <p>Uma página de vendas com design moderno e responsivo.</p>
			                
			                <div class="tags">
			                    <span>HTML</span>
			                    <span>CSS</span>
			                </div>
			
			                <div class="botoes-projeto">
			                    <a href="#">Ver Site</a>
			                    <a href="#">Código</a>
			                </div>
			            </div>
			        </div>
			
			        <div class="card-projeto">
			            <div class="img-box">
			                <img src="imagens/projeto2.png" alt="Print do projeto">
			            </div>
			            
			            <div class="projeto-info">
			                <h3>Dashboard</h3>
			                <p>Painel administrativo para controle de tarefas.</p>
			                
			                <div class="tags">
			                    <span>React</span>
			                    <span>JS</span>
			                </div>
			
			                <div class="botoes-projeto">
			                    <a href="#">Ver Site</a>
			                    <a href="#">Código</a>
			                </div>
			            </div>
			        </div>
			
			        <div class="card-projeto">
			            <div class="img-box">
			                <img src="imagens/projeto3.png" alt="Print do projeto">
			            </div>
			            
			            <div class="projeto-info">
			                <h3>Blog Pessoal</h3>
			                <p>Blog minimalista para postagem de artigos técnicos.</p>
			                
			                <div class="tags">
			                    <span>HTML</span>
			                    <span>CSS</span>
			                </div>
			
			                <div class="botoes-projeto">
			                    <a href="#">Ver Site</a>
			                    <a href="#">Código</a>
			                </div>
			            </div>
			        </div>
			
			    </div>
			</section>

            <section id="contato">
			    <div class="contato-header">
			        <h2 class="titulo-secao">Vamos Conversar?</h2>
			        <p>Gostou do meu portfólio? Entre em contato para construirmos algo juntos.</p>
			    </div>
			
			    <div class="contato-grid">
			        
			        <div class="card-contato">
			            <i class="ph ph-envelope-simple"></i>
			            <h3>Email</h3>
			            <a href="mailto:seuemail@gmail.com">Enviar mensagem</a>
			        </div>
			
			        <div class="card-contato">
			            <i class="ph ph-linkedin-logo"></i>
			            <h3>LinkedIn</h3>
			            <a href="#" target="_blank">Conectar</a>
			        </div>
			
			        <div class="card-contato">
			            <i class="ph ph-whatsapp-logo"></i>
			            <h3>WhatsApp</h3>
			            <a href="#" target="_blank">Falar agora</a>
			        </div>
			
			    </div>
			</section>

        </main>
        <footer>
		    <p>© Todos os direitos reservados - 2025</p>
		    <p>Desenvolvido por <strong style="color: #7c3aed;">SEU NOME</strong></p>
		</footer>
    </body>
</html>
```

## Parte 11: Estilização (Configurações) :dev_css3_original:

Agora é onde a mágica acontece, nós estruturamos o esqueleto do site (HTML) agora chegou o momento de dar cores para ele (CSS).

A partir de agora, iremos trabalhar no arquivo `index.css`. Logo abaixo daquele `@import` vamos colocar algumas configurações do site e das seções, para isso, cole o seguinte código no arquivo `index.css`:

```css
/* 1. Variáveis de Cores (A Paleta do Site) */
:root {
    --cor-primaria: #7c3aed; /* Roxo principal */
    --cor-primaria-escura: #5b21b6; /* Roxo mais escuro para hover */
    --cor-fundo: #ffffff; /* Branco */
    --cor-fundo-secundario: #f9fafb; /* Cinza bem clarinho */
    --cor-texto: #111827; /* Preto suave */
    --cor-texto-secundario: #6b7280; /* Cinza para textos menores */
}

/* 2. Configurações do Corpo do Site */
html {
    scroll-behavior: smooth; /* Faz a rolagem do menu ser suave */
}

body {
    background-color: var(--cor-fundo);
    color: var(--cor-texto);
    /* A fonte já foi definida no passo anterior, mas reforçamos aqui se precisar */
}

/* 3. Configuração Geral das Seções */
section {
    padding: 80px 10%; /* Espaçamento interno: 80px em cima/baixo, 10% nas laterais */
}

h2.titulo-secao {
    text-align: center;
    font-size: 2rem;
    margin-bottom: 60px;
    text-transform: uppercase;
    letter-spacing: 1px;
}
```


## Parte 12: Estilização do Cabeçalho :dev_css3_original:

O cabeçalho, aquele que tem a logo e o menu de navegação, precisa ficar no topo do site, com a logo alinhada a esquerda e com o menu de navegação alinhado com a direita.

Para conseguir fazer isso, devemos usar o `display: flex;` e usar algumas de suas propriedades.

Para isso, cole o código a seguir no arquivo `index.html`, logo abaixo do código anterior:

```css
/* --- CABEÇALHO --- */
#header {
    display: flex; /* Coloca logo e menu lado a lado */
    justify-content: space-between; /* Empurra um para cada ponta */
    align-items: center; /* Alinha verticalmente */
    padding: 20px 10%;
    
    background-color: rgba(255, 255, 255, 0.95); /* Fundo branco levemente transparente */
    position: fixed; /* Fixa o menu no topo */
    width: 100%;
    top: 0;
    left: 0;
    z-index: 1000; /* Garante que fique acima de tudo */
    box-shadow: 0 2px 10px rgba(0,0,0,0.05); /* Sombrae suave */
}

.logo {
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--cor-primaria);
}

#navbar ul {
    display: flex;
    gap: 32px; /* Espaço entre os links do menu */
}

#navbar a {
    color: var(--cor-texto);
    font-weight: 500;
    transition: color 0.3s;
}

#navbar a:hover {
    color: var(--cor-primaria);
}

/* Botão de Contato destacado no menu */
.btn-contato {
    background-color: var(--cor-primaria);
    color: white !important; /* O !important garante que a cor branca pegue */
    padding: 10px 24px;
    border-radius: 8px;
    transition: background-color 0.3s;
}

.btn-contato:hover {
    background-color: var(--cor-primaria-escura);
}
```

## Parte 13: Estilizando o Inicio :dev_css3_original:

Após estilizar o Navbar podemos arrumar a seção início, que é a parte principal do site. 

Para seguirmos com a estilização, cole o código logo depois do código anterior.


```css
/* --- SEÇÃO INÍCIO (HERO) --- */
#inicio {
    display: flex;
    align-items: center;
    justify-content: space-between;
    min-height: 100vh; /* Garante que ocupe a altura toda da tela */
    padding-top: 80px; /* Compensação por causa do menu fixo */
}

.hero-texto {
    max-width: 50%; /* O texto ocupa metade da tela */
}

.hero-texto h1 {
    font-size: 3.5rem; /* Tamanho grande para o título */
    line-height: 1.2;
    margin-bottom: 24px;
}

.hero-texto p {
    font-size: 1.1rem;
    color: var(--cor-texto-secundario);
    margin-bottom: 40px;
    line-height: 1.6;
    max-width: 500px;
}

/* Botões e Redes Sociais */
.hero-botoes {
    display: flex;
    align-items: center;
    gap: 30px;
}

.btn-primario {
    background-color: var(--cor-primaria);
    color: white;
    padding: 14px 32px;
    border-radius: 8px;
    font-weight: 600;
    box-shadow: 0 4px 14px rgba(124, 58, 237, 0.3); /* Sombra roxa bonita */
    transition: transform 0.2s;
}

.btn-primario:hover {
    transform: translateY(-2px); /* Efeito de 'subir' levemente */
    background-color: var(--cor-primaria-escura);
}

.redes-sociais {
    display: flex;
    gap: 20px;
}

.redes-sociais i {
    font-size: 2rem;
    color: var(--cor-texto-secundario);
    transition: 0.3s;
}

.redes-sociais i:hover {
    color: var(--cor-primaria);
    transform: scale(1.1);
}

/* Imagem */
.hero-imagem img {
    width: 100%;
    max-width: 550px; /* Limita o tamanho máximo para não ficar gigante */
    animation: flutuar 3s ease-in-out infinite; /* (Opcional) Animação */
}

/* Animação bônus para a imagem flutuar */
@keyframes flutuar {
    0% { transform: translateY(0px); }
    50% { transform: translateY(-15px); }
    100% { transform: translateY(0px); }
}
```

No final dessa instrução do CSS temos um bônus, uma pequena demonstração de como podemos criar animações com CSS.

## Parte 14: Estilizando a seção Habilidades :dev_css3_original:

No cabeçalho nós precisamos usar o conceito de flexbox para poder alinhar os elementos. Nessa parte iremos utilizar outro tipo de display, o grid-layout, para isso vamos usar o `display: grid`.

Ele é tão prático quanto o flexbox, para vermos isso funcionando, vamos colar esse código logo depois do anterior:

```css
/* --- SEÇÃO HABILIDADES --- */
/* Fundo cinza claro para separar visualmente da seção anterior */
#habilidades {
    background-color: var(--cor-fundo-secundario); 
}

.habilidades-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* Cria 3 colunas de tamanho igual */
    gap: 32px; /* Espaço entre os cards */
}

/* Estilo de cada cartão */
.card {
    background-color: var(--cor-fundo);
    padding: 32px;
    border-radius: 12px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05); /* Sombra leve */
    border: 1px solid #e5e7eb; /* Borda bem fininha */
    transition: transform 0.3s, border-color 0.3s;
}

/* Efeito ao passar o mouse (Hover) */
.card:hover {
    transform: translateY(-5px); /* O card sobe um pouquinho */
    border-color: var(--cor-primaria); /* A borda fica roxa */
}

/* Ícone dentro do card */
.card i {
    font-size: 3rem; /* Ícone grande */
    color: var(--cor-primaria);
    margin-bottom: 16px;
}

.card h3 {
    font-size: 1.25rem;
    margin-bottom: 8px;
}

.card p {
    color: var(--cor-texto-secundario);
    line-height: 1.5;
}
```


## Parte 15: Estilizando a seção Projetos :dev_css3_original:

Estamos quase no fim dessa jornada da landing page. Até aqui vocês entenderam bastante conceito. Para próxima parte vamos estilizar a parte de projetos. 

A lógica é parecida com a das habilidades, mas aqui temos um pouco mais 

Para isso, colem o código a seguir logo a baixo do anterior.

```css
/* --- SEÇÃO PROJETOS --- */
.projetos-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* 3 Colunas */
    gap: 32px;
}

.card-projeto {
    background-color: var(--cor-fundo);
    border-radius: 12px;
    overflow: hidden; /* Garante que a imagem não saia pelas bordas arredondadas */
    box-shadow: 0 4px 10px rgba(0,0,0,0.05);
    border: 1px solid #e5e7eb;
    transition: transform 0.3s;
}

.card-projeto:hover {
    transform: translateY(-5px);
}

/* A caixa da imagem */
.img-box img {
    width: 100%; /* Imagem ocupa a largura total do card */
    height: 200px; /* Altura fixa para todos ficarem iguais */
    object-fit: cover; /* Corta a imagem para preencher sem esticar */
}

.projeto-info {
    padding: 24px;
}

.projeto-info h3 {
    margin-bottom: 8px;
    font-size: 1.25rem;
}

.projeto-info p {
    color: var(--cor-texto-secundario);
    margin-bottom: 16px;
    font-size: 0.9rem;
}

/* As etiquetas (HTML, CSS, etc) */
.tags {
    display: flex;
    gap: 8px;
    margin-bottom: 20px;
}

.tags span {
    background-color: #ede9fe; /* Fundo roxo bem clarinho */
    color: var(--cor-primaria);
    padding: 4px 12px;
    border-radius: 4px;
    font-size: 0.75rem;
    font-weight: 600;
}

/* Botões do card */
.botoes-projeto {
    display: flex;
    gap: 10px;
}

.botoes-projeto a {
    flex: 1; /* Faz os dois botões terem o mesmo tamanho */
    text-align: center;
    padding: 10px;
    border-radius: 6px;
    font-size: 0.9rem;
    font-weight: 600;
    transition: 0.3s;
}

/* Primeiro botão (Ver Site) */
.botoes-projeto a:first-child {
    background-color: var(--cor-primaria);
    color: white;
}

.botoes-projeto a:first-child:hover {
    background-color: var(--cor-primaria-escura);
}

/* Segundo botão (Código) */
.botoes-projeto a:last-child {
    border: 1px solid var(--cor-primaria);
    color: var(--cor-primaria);
}

.botoes-projeto a:last-child:hover {
    background-color: #ede9fe;
}
```

Nessa parte utilizamos conceitos mais avançados como pseudo-classes e encadeamento delas. Como podem ver temos o seguinte código `a:last-child:hover`. Aqui ele ta indicando o último filho da tag `<a>` e aplica esse estilo quando o mouse é passado por cima dele. INTERESSANTE NÃO ?

## Parte 16: Estilizando a seção Contato e o rodapé :dev_css3_original:

Para finalizar, vamos deixar a área de contato bem chamativa e centralizada.

```css
/* --- SEÇÃO CONTATO --- */
#contato {
    background-color: var(--cor-fundo-secundario);
    text-align: center; /* Centraliza tudo */
}

.contato-header {
    max-width: 600px;
    margin: 0 auto 60px auto; /* Centraliza o bloco na tela */
}

.contato-grid {
    display: flex; /* Aqui usamos Flex pois são poucos itens */
    justify-content: center;
    gap: 32px;
    flex-wrap: wrap; /* Permite quebrar linha se a tela for pequena */
}

.card-contato {
    background-color: var(--cor-fundo);
    padding: 32px;
    width: 240px;
    border-radius: 12px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 12px;
    transition: 0.3s;
}

.card-contato:hover {
    transform: translateY(-5px);
    border: 1px solid var(--cor-primaria);
}

.card-contato i {
    font-size: 2.5rem;
    color: var(--cor-primaria);
}

.card-contato a {
    color: var(--cor-texto-secundario);
    font-weight: 500;
}

.card-contato a:hover {
    color: var(--cor-primaria);
    text-decoration: underline;
}

/* --- RODAPÉ --- */
footer {
    text-align: center;
    padding: 40px;
    background-color: var(--cor-fundo);
    border-top: 1px solid #e5e7eb;
    color: var(--cor-texto-secundario);
    font-size: 0.9rem;
}
```

## Agradecimentos

Se você chegou até aqui **PARABÉNS**, você concluiu sua landing page. Você não apenas copiou e colou, mas aprendeu vários conceitos e viu como as coisas funcionam quando estamos desenvolvendo aplicações reais.

Aqui você aprendeu: 

- **Estrutura de Arquivos:** Como organizar um projeto real separando HTML, CSS e imagens em pastas.

- **HTML Semântico:** O uso correto de tags como `<header>`, `<main>`, `<section>` e `<footer>` para dar significado ao código e melhorar a leitura.

- **Reset CSS:** A importância de "zerar" as margens e preenchimentos padrão do navegador para ter controle total sobre o layout.

- **Integração de Bibliotecas:** Como importar recursos externos no projeto, como fontes do **Google Fonts** (Inter) e ícones do **Phosphor Icons**.

- **Flexbox:** Técnica moderna para alinhar itens (usada para colocar o Logo e o Menu lado a lado no cabeçalho).

- **CSS Grid:** O poder de criar colunas perfeitas para organizar os cards de Habilidades e Projetos.

- **Variáveis CSS:** Como armazenar cores em variáveis (`:root`) para facilitar a manutenção e mudança de temas.

- **Box Model:** O entendimento prático de como funcionam `margin`, `padding` e `border-box` na construção dos espaçamentos.