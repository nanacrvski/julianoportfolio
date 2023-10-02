  <html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Portfólio</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #b3d7ff; 
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #6579ad; 
            color: #fff;
            padding: 20px 0;
            text-align: center;
        }

        nav {
            background-color: #7795e0; /* Rosa médio */
            color: #fff;
            text-align: center;
            padding: 10px 0;
        }

        nav a {
            color: #fff;
            text-decoration: none;
            margin: 0 15px;
            font-weight: bold;
            font-size: 18px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff; /* Fundo branco */
            border-radius: 10px; /* Bordas arredondadas */
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2); /* Sombra suave */
        }

        h1 {
            font-size: 36px;
            color: #ff6699; /* Rosa escuro */
            margin-bottom: 20px;
        }

        p {
            font-size: 18px;
            line-height: 1.5;
            color: #666;
        }

        .button {
            display: inline-block;
            padding: 12px 24px;
            background-color: #1b2640; /* Rosa escuro */
            color: #fff;
            text-decoration: none;
            font-weight: bold;
            border-radius: 5px;
            transition: background-color 0.3s;
        }

        .button:hover {
            background-color: #1b2640; /* Rosa médio */
        }
    </style>
</head>
<body>
    <header>
        <h1>Bem-vindo ao Meu Portfólio</h1>
    </header>
    <nav>
        <a href="#" id="btn-inicio">Início</a>
        <a href="#" id="btn-sobre">Conteúdos</a>
        <a href="#" id="btn-servicos">Autoavaliação</a>
    </nav>
    <div class="container" id="conteudo-inicio">
        <h2>Início</h2>
        <p>Esta é a página inicial do nosso site.</p>
    </div>
    <div class="container" id="conteudo-sobre" style="display: none;">
        <h2>Conteúdos</h2>
        <p>Aqui você encontrará informações sobre meus projetos e trabalhos.</p>
        <a href="#" class="button" id="btn-saiba-mais-sobre">Saiba Mais</a>
    </div>
    <div class="container" id="conteudo-servicos" style="display: none;">
        <h2>Autoavaliação</h2>
        <p>Confira minha autoavaliação e meu progresso.</p>
        <a href="#" class="button" id="btn-saiba-mais-servicos">Saiba Mais</a>
    </div>
    <div class="container" id="conteudo-contato" style="display: none;">
        <h2>Contato</h2>
        <p>Entre em contato comigo através do formulário abaixo:</p>
        <form>
            <label for="nome">Nome:</label>
            <input type="text" id="nome" name="nome" required><br><br>
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required><br><br>
            <textarea id="mensagem" name="mensagem" rows="4" cols="50" placeholder="Digite sua mensagem aqui..." required></textarea><br><br>
            <input type="submit" value="Enviar">
        </form>
    </div>

    <script>
        // JavaScript para controlar a exibição das seções
        const btnInicio = document.getElementById('btn-inicio');
        const btnSobre = document.getElementById('btn-sobre');
        const btnServicos = document.getElementById('btn-servicos');
        const btnContato = document.getElementById('btn-contato');
        const conteudoInicio = document.getElementById('conteudo-inicio');
        const conteudoSobre = document.getElementById('conteudo-sobre');
        const conteudoServicos = document.getElementById('conteudo-servicos');
        const conteudoContato = document.getElementById('conteudo-contato');

        btnInicio.addEventListener('click', () => {
            conteudoInicio.style.display = 'block';
            conteudoSobre.style.display = 'none';
            conteudoServicos.style.display = 'none';
            conteudoContato.style.display = 'none';
        });

        btnSobre.addEventListener('click', () => {
            conteudoInicio.style.display = 'none';
            conteudoSobre.style.display = 'block';
            conteudoServicos.style.display = 'none';
            conteudoContato.style.display = 'none';
        });

        btnServicos.addEventListener('click', () => {
            conteudoInicio.style.display = 'none';
            conteudoSobre.style.display = 'none';
            conteudoServicos.style.display = 'block';
            conteudoContato.style.display = 'none';
        });

        btnContato.addEventListener('click', () => {
            conteudoInicio.style.display = 'none';
            conteudoSobre.style.display = 'none';
            conteudoServicos.style.display = 'none';
            conteudoContato.style.display = 'block';
        });
    </script>
</body>
</html>
