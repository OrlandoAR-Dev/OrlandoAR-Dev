<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Perfil JSON • Desarrollador Full Stack</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&display=swap');

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Fira Code', monospace;
            background: linear-gradient(135deg, #1a1e2a 0%, #2a2f3f 100%);
            min-height: 100vh;
            padding: 2rem;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #e1e4e8;
        }

        .container {
            max-width: 1200px;
            width: 100%;
        }

        .json-viewer {
            background: #1e2430;
            border-radius: 16px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
            overflow: hidden;
            border: 1px solid #2f3542;
        }

        .json-header {
            background: #0b0e14;
            padding: 1rem 1.5rem;
            display: flex;
            align-items: center;
            gap: 1rem;
            border-bottom: 2px solid #2f3542;
        }

        .json-dots {
            display: flex;
            gap: 0.5rem;
        }

        .json-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }

        .json-dot.red { background: #ff5f56; }
        .json-dot.yellow { background: #ffbd2e; }
        .json-dot.green { background: #27c93f; }

        .json-title {
            color: #808080;
            font-size: 0.9rem;
        }

        .json-content {
            padding: 2rem;
            background: #1a1e2a;
            overflow-x: auto;
        }

        pre {
            margin: 0;
            font-family: 'Fira Code', monospace;
            font-size: 0.95rem;
            line-height: 1.6;
            white-space: pre-wrap;
            word-wrap: break-word;
        }

        /* JSON Syntax Highlighting - Vibrant Colors */
        .json-key {
            color: #ff79c6;  /* Rosa vibrante */
            font-weight: 600;
        }
        
        .json-string {
            color: #9bdf6c;  /* Verde vibrante */
        }
        
        .json-number {
            color: #d19a66;  /* Naranja */
        }
        
        .json-boolean {
            color: #56b6c2;  /* Cyan */
        }
        
        .json-null {
            color: #e06c75;  /* Rojo suave */
        }
        
        .json-bracket {
            color: #e5c07b;  /* Amarillo */
        }
        
        .json-array-bracket {
            color: #61afef;  /* Azul */
        }
        
        .json-emoji {
            font-style: normal;
            filter: drop-shadow(0 2px 2px rgba(0,0,0,0.3));
        }

        .json-comment {
            color: #5c6370;
            font-style: italic;
        }

        .json-array-item {
            color: #98c379;  /* Verde para items de array */
        }

        .status-badge {
            display: inline-block;
            background: #2d3440;
            padding: 0.2rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            color: #9bdf6c;
            border: 1px solid #3b4252;
        }

        .footer {
            margin-top: 2rem;
            text-align: center;
            color: #5c6370;
            font-size: 0.85rem;
        }

        .footer a {
            color: #61afef;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer a:hover {
            color: #9bdf6c;
        }

        /* Hover effects */
        .json-key:hover, .json-string:hover, .json-number:hover {
            filter: brightness(1.2);
            transition: filter 0.2s;
            cursor: default;
        }

        /* Scrollbar personalizada */
        ::-webkit-scrollbar {
            width: 10px;
            height: 10px;
        }

        ::-webkit-scrollbar-track {
            background: #1a1e2a;
        }

        ::-webkit-scrollbar-thumb {
            background: #3b4252;
            border-radius: 5px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: #4c5566;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="json-viewer">
            <div class="json-header">
                <div class="json-dots">
                    <div class="json-dot red"></div>
                    <div class="json-dot yellow"></div>
                    <div class="json-dot green"></div>
                </div>
                <span class="json-title">perfil-desarrollador.json</span>
                <span class="status-badge">⚡ Interactivo</span>
            </div>
            <div class="json-content">
                <pre>{
    <span class="json-key">"👤 nombre"</span>: <span class="json-string">"Tu Nombre Completo"</span>,
    <span class="json-key">"🏷️ alias"</span>: <span class="json-string">"tu_username"</span>,
    <span class="json-key">"📍 ubicacion"</span>: <span class="json-string">"Tu Ciudad, País"</span>,
    <span class="json-key">"💼 profesion"</span>: <span class="json-string">"Desarrollador Full Stack"</span>,
    
    <span class="json-key">"🛠️ especialidades"</span>: [
        <span class="json-string">"✨ Frontend Development"</span>,
        <span class="json-string">"⚡ Backend Development"</span>,
        <span class="json-string">"🎨 UI/UX Design"</span>
    ],
    
    <span class="json-key">"💻 tecnologias"</span>: {
        <span class="json-key">"📌 lenguajes"</span>: [
            <span class="json-string">"JavaScript"</span>, 
            <span class="json-string">"Python"</span>, 
            <span class="json-string">"Java"</span>, 
            <span class="json-string">"TypeScript"</span>
        ],
        
        <span class="json-key">"🎨 frontend"</span>: [
            <span class="json-string">"React"</span>, 
            <span class="json-string">"Vue.js"</span>, 
            <span class="json-string">"Angular"</span>, 
            <span class="json-string">"HTML5"</span>, 
            <span class="json-string">"CSS3"</span>
        ],
        
        <span class="json-key">"🔧 backend"</span>: [
            <span class="json-string">"Node.js"</span>, 
            <span class="json-string">"Django"</span>, 
            <span class="json-string">"Spring Boot"</span>
        ],
        
        <span class="json-key">"🗄️ bases_datos"</span>: [
            <span class="json-string">"MongoDB"</span>, 
            <span class="json-string">"PostgreSQL"</span>, 
            <span class="json-string">"MySQL"</span>
        ],
        
        <span class="json-key">"🔨 herramientas"</span>: [
            <span class="json-string">"Git"</span>, 
            <span class="json-string">"Docker"</span>, 
            <span class="json-string">"AWS"</span>, 
            <span class="json-string">"VS Code"</span>
        ]
    },
    
    <span class="json-key">"⚡ estado_actual"</span>: <span class="json-string">"🚀 Buscando nuevos desafíos"</span>,
    
    <span class="json-key">"🎯 intereses"</span>: [
        <span class="json-string">"🌐 Desarrollo Web"</span>,
        <span class="json-string">"🤖 Machine Learning"</span>,
        <span class="json-string">"📦 Open Source"</span>,
        <span class="json-string">"💡 Innovación Tecnológica"</span>
    ],
    
    <span class="json-key">"📱 contacto"</span>: {
        <span class="json-key">"📧 email"</span>: <span class="json-string">"tu.email@ejemplo.com"</span>,
        <span class="json-key">"💼 linkedin"</span>: <span class="json-string">"linkedin.com/in/tuusuario"</span>,
        <span class="json-key">"🐦 twitter"</span>: <span class="json-string">"@tusuario"</span>,
        <span class="json-key">"🌐 portfolio"</span>: <span class="json-string">"tusitio.com"</span>
    },
    
    <span class="json-key">"🎲 datos_curiosos"</span>: {
        <span class="json-key">"☕ cafe"</span>: <span class="json-string">"3 tazas mínimo"</span>,
        <span class="json-key">"⚛️ framework_favorito"</span>: <span class="json-string">"React"</span>,
        <span class="json-key">"🐍 primer_lenguaje"</span>: <span class="json-string">"Python"</span>,
        <span class="json-key">"🐱 animal_favorito"</span>: <span class="json-string">"Gatos (también me gustan los perros)"</span>
    }
}</pre>
            </div>
        </div>
        <div class="footer">
            ⚡ Perfil en formato JSON con sintaxis colorida • Hecho con <span style="color: #ff79c6;">❤️</span> para desarrolladores
            <br>
            <a href="#">📋 Copiar JSON</a> • <a href="#">🔄 Actualizar datos</a> • <a href="#">📱 Modo desarrollo</a>
        </div>
    </div>

    <script>
        // Pequeño script para hacer la página más interactiva
        document.querySelector('.footer a:first-child').addEventListener('click', (e) => {
            e.preventDefault();
            const jsonContent = document.querySelector('pre').innerText;
            navigator.clipboard.writeText(jsonContent).then(() => {
                alert('✅ JSON copiado al portapapeles!');
            }).catch(() => {
                alert('❌ No se pudo copiar automáticamente');
            });
        });
    </script>
</body>
</html>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/OrlandoAR-Dev/OrlandoAR-Dev/output/pacman-contribution-graph-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/OrlandoAR-Dev/OrlandoAR-Dev/output/pacman-contribution-graph.svg">
  <img alt="pacman contribution graph" src="https://raw.githubusercontent.com/OrlandoAR-Dev/OrlandoAR-Dev/output/pacman-contribution-graph.svg">
</picture>

