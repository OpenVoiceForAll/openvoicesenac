<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OPEN VOICE</title>
    <link rel="icon" type="image/x-icon" href="imagens/mic.ico">
    <style>
        /* Reset de margens e padding */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Estilo para o corpo da página */
        body {
            
            background-size: cover; /* Cobrir todo o espaço do body */
            background-position: center; /* Centralizar a imagem */
            background-attachment: fixed; /* Fixar a imagem para que role com a página */
            color: #fff; /* Cor do texto */
            font-family: Arial, sans-serif; 
            margin: 0; 
            padding: 0; 
        }

        /* Estilos para o cabeçalho */
        header {
            background-color:#00AEEF; 
            padding: 20px 0; 
            position: fixed; 
            width: 100%; 
            z-index: 100; 
        }
        .container {
            width: 80%;
            margin: 0 auto; /* Centralizar o conteúdo */
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        .logo {
            max-width: 100px; 
        }
        nav ul {
            list-style-type: none;
            display: flex;
        }
        nav ul li {
            margin-right: 20px;
        }
        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-size: 16px;
        }
        nav ul li a:hover {
            color: black;
        }

        /* Estilos para o rodapé */
        footer {
            background-color:#00AEEF; 
            color:#fff; 
            padding: 20px 0;
            text-align: center;
            position: fixed; 
            bottom: 0; 
            width: 100%; 
            z-index: 1;
        }

        /* Estilos para as seções */
        .hero, .posts, .contato, .sobre {
            min-height: calc(100vh - 60px); 
            background-color: black; 
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            position: relative;
            z-index: 1; 
            margin-bottom: 60px; 
        }
        .text-overlay {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: black;
        }

        /* Estilos para os modais */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            overflow: auto;
        }
        .modal-content {
            background-color: hsla(0, 0%, 100%, 0);
            margin: 15% auto;
            padding: 20px;
            border: 1px solid #888;
            width: 80%;
            max-width: 600px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            text-align: center;
            position: relative;
        }
        .close {
            color: red;
            position: absolute;
            top: 10px;
            right: 15px;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }
        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
        }

        button {
            padding: 10px 20px;
            background-color: #4CAF50;
            color: white;
            font-size: 16px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            text-transform: uppercase;
        }

        button:hover {
            background-color: #45a049;
        }
    
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>OPEN VOICE </h1 Merriweather>
            <nav>
                <ul>
                    <li><a href="#inicio">Início</a></li>
                    <li><a href="#servicos" id="link-servicos">Serviços</a></li>
                    <li><a href="#contato" id="link-contato">Contato</a></li>
                    <li><a href="#sobre-nos" id="link-sobre">Sobre Nós</a></li>
                    <li><a href="howto.html" id="link-facaseu">Faça o seu</a></li> 
                </ul>
            </nav>
        </div>
    </header>
    
    <div class="hero" id="inicio">
        <div class="text-overlay">
        <img src="imagens/fundo.jpg" alt="">
        </div>
    </div>


    <footer>
        <div class="container">
            <p>O palco é seu, com o karaokê SENAC REGISTRO</p>
        </div>
    </footer>


    <div id="modal-servicos" class="modal">
        <div class="modal-content">
            <span class="close" onclick="fecharModal('modal-servicos')">&times;</span>
            <h2>Nossos Serviços</h2>
            <p>Alguns de Nossos Serviços</p>
            <ul>
                <li><img src="imagens/karaoke.jfif" alt=""></li>
            </ul>
        </div>
    </div>


    <div id="modal-contato" class="modal">
        <div class="modal-content">
            <span class="close" onclick="fecharModal('modal-contato')">&times;</span>
            <h2>Contatos</h2>
            <p>Email: openvoice.senac@gmail.com</p>
        </div>
    </div>

   
    <div id="modal-sobre" class="modal">
        <div class="modal-content">
            <span class="close" onclick="fecharModal('modal-sobre')">&times;</span>
            <h2>Sobre Nós</h2>
            <p>Nosso primeiro projeto integrador combina todos os temas abordados nas unidades
                curriculares 1, 2 e 3, mas com um toque distintivo: a música. Decidimos integrar o conceito
                de karaokê com design inspirado na tecnologia antiga, como celulares antigos, utilizando
                hardwares completamente recuperados de outras máquinas e um software desenvolvido do
                zero. O software terá a identidade visual única do nosso grupo e será totalmente gratuito,
                disponível para download e acesso livre a todos. Além disso, estamos criando um site
                dedicado à marca e ao projeto, denominado 'Open Voice</p>
        </div>
    </div>

   
    <div id="modal-facaseu" class="modal">
        <div class="modal-content">
            <span class="close" onclick="fecharModal('modal-facaseu')">&times;</span>
            <h2>Faça o seu</h2>
            <p>Passo a Passo aqui</p>
        </div>
    </div>

    <script>
        
        const linkServicos = document.getElementById('link-servicos');
        const modalServicos = document.getElementById('modal-servicos');

        linkServicos.addEventListener('click', function(e) {
            e.preventDefault();
            modalServicos.style.display = 'block';
        });

  
        const linkContato = document.getElementById('link-contato');
        const modalContato = document.getElementById('modal-contato');

        linkContato.addEventListener('click', function(e) {
            e.preventDefault();
            modalContato.style.display = 'block';
        });

 
        const linkSobre = document.getElementById('link-sobre');
        const modalSobre = document.getElementById('modal-sobre');

        linkSobre.addEventListener('click', function(e) {
            e.preventDefault();
            modalSobre.style.display = 'block';
        });

        // Função para fechar o modal ao clicar no botão de fechar (X)
        function fecharModal(idModal) {
            const modal = document.getElementById(idModal);
            modal.style.display = 'none';
        }

        // Fechar o modal se o usuário clicar fora da área do modal
        window.onclick = function(event) {
            if (event.target.classList.contains('modal')) {
                event.target.style.display = 'none';
            }
        }
    </script>
</body>
</html>
