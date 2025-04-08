HTML
```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Como Encontrar o Número de Série - ServiceNow</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-content">
            <img src="https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/images/company-library/logo/servicenow-logo-white.svg" alt="ServiceNow Logo" class="logo">
            <span class="header-title">Suporte de TI</span>
        </div>
    </header>

    <!-- Breadcrumb -->
    <div class="breadcrumb">
        <a href="#">Home</a> &gt; 
        <a href="#">Catálogos</a> &gt; 
        <a href="#">Microinformática</a> &gt; 
        <span>Como Encontrar o Número de Série</span>
    </div>

    <!-- Main Content -->
    <main>
        <div class="card">
            <h1 class="page-title">
                Como Encontrar o Número de Série do Notebook via CMD
            </h1>

            <p class="description">
                Siga este guia passo a passo para encontrar o número de série do seu notebook usando o Prompt de Comando (CMD) do Windows. Este número é essencial para o registro e suporte do seu equipamento.
            </p>

            <!-- Step 1 -->
            <div class="step">
                <div class="step-header">
                    <div class="step-number">1</div>
                    <h3 class="step-title">Abra o Prompt de Comando (CMD)</h3>
                </div>
                <div class="step-content">
                    <p>
                        Pressione a tecla <strong>Windows + R</strong>, digite <strong>cmd</strong> e pressione <strong>Enter</strong>.
                    </p>
                    <div class="icon-container">
                        <svg class="icon-large" viewBox="0 0 512 512">
                            <path d="M80 368H16a16 16 0 0 0-16 16v64a16 16 0 0 0 16 16h64a16 16 0 0 0 16-16v-64a16 16 0 0 0-16-16zm0-320H16A16 16 0 0 0 0 64v64a16 16 0 0 0 16 16h64a16 16 0 0 0 16-16V64a16 16 0 0 0-16-16zm0 160H16a16 16 0 0 0-16 16v64a16 16 0 0 0 16 16h64a16 16 0 0 0 16-16v-64a16 16 0 0 0-16-16zm416 176H176a16 16 0 0 0-16 16v32a16 16 0 0 0 16 16h320a16 16 0 0 0 16-16v-32a16 16 0 0 0-16-16zm0-320H176a16 16 0 0 0-16 16v32a16 16 0 0 0 16 16h320a16 16 0 0 0 16-16V64a16 16 0 0 0-16-16zm0 160H176a16 16 0 0 0-16 16v32a16 16 0 0 0 16 16h320a16 16 0 0 0 16-16v-32a16 16 0 0 0-16-16z"/>
                        </svg>
                    </div>
                </div>
            </div>

            <!-- Step 2 -->
            <div class="step">
                <div class="step-header">
                    <div class="step-number">2</div>
                    <h3 class="step-title">Digite o comando para obter o número de série</h3>
                </div>
                <div class="step-content">
                    <p>
                        Digite o seguinte comando e pressione <strong>Enter</strong>:
                    </p>
                    <div class="code-block">
                        <code>wmic bios get serialnumber</code>
                        <button id="copyButton" class="copy-button">
                            <svg class="icon-copy" viewBox="0 0 448 512">
                                <path d="M320 448v40c0 13.255-10.745 24-24 24H24c-13.255 0-24-10.745-24-24V120c0-13.255 10.745-24 24-24h72v296c0 30.879 25.121 56 56 56h168zm0-344V0H152c-13.255 0-24 10.745-24 24v368c0 13.255 10.745 24 24 24h272c13.255 0 24-10.745 24-24V128H344c-13.2 0-24-10.8-24-24zm120.971-31.029L375.029 7.029A24 24 0 0 0 358.059 0H352v96h96v-6.059a24 24 0 0 0-7.029-16.97z"/>
                            </svg>
                        </button>
                    </div>
                    <p>
                        Este comando exibirá o número de série do seu notebook diretamente no prompt de comando.
                    </p>
                </div>
            </div>

            <!-- Step 3 -->
            <div class="step">
                <div class="step-header">
                    <div class="step-number">3</div>
                    <h3 class="step-title">Resultado esperado</h3>
                </div>
                <div class="step-content">
                    <p>
                        Você verá uma saída semelhante a esta:
                    </p>
                    <div class="code-block">
                        <code>SerialNumber
ABC123XYZ</code>
                    </div>
                    <p>
                        O número abaixo de "SerialNumber" é o número de série do seu notebook.
                    </p>
                </div>
            </div>

            <!-- Step 4 -->
            <div class="step">
                <div class="step-header">
                    <div class="step-number">4</div>
                    <h3 class="step-title">Tire uma captura de tela do resultado</h3>
                </div>
                <div class="step-content">
                    <div class="info-box">
                        <h4 class="info-title">
                            <svg class="icon-info" viewBox="0 0 512 512">
                                <path d="M256 8C119.043 8 8 119.083 8 256c0 136.997 111.043 248 248 248s248-111.003 248-248C504 119.083 392.957 8 256 8zm0 110c23.196 0 42 18.804 42 42s-18.804 42-42 42-42-18.804-42-42 18.804-42 42-42zm56 254c0 6.627-5.373 12-12 12h-88c-6.627 0-12-5.373-12-12v-24c0-6.627 5.373-12 12-12h12v-64h-12c-6.627 0-12-5.373-12-12v-24c0-6.627 5.373-12 12-12h64c6.627 0 12 5.373 12 12v100h12c6.627 0 12 5.373 12 12v24z"/>
                            </svg>
                            Método 1: Print Screen
                        </h4>
                        <p>
                            Pressione a tecla <strong>Print Screen</strong> ou <strong>PrtScn</strong> no seu teclado para copiar a tela inteira.
                        </p>
                    </div>
                    
                    <div class="info-box">
                        <h4 class="info-title">
                            <svg class="icon-info" viewBox="0 0 512 512">
                                <path d="M256 8C119.043 8 8 119.083 8 256c0 136.997 111.043 248 248 248s248-111.003 248-248C504 119.083 392.957 8 256 8zm0 110c23.196 0 42 18.804 42 42s-18.804 42-42 42-42-18.804-42-42 18.804-42 42-42zm56 254c0 6.627-5.373 12-12 12h-88c-6.627 0-12-5.373-12-12v-24c0-6.627 5.373-12 12-12h12v-64h-12c-6.627 0-12-5.373-12-12v-24c0-6.627 5.373-12 12-12h64c6.627 0 12 5.373 12 12v100h12c6.627 0 12 5.373 12 12v24z"/>
                            </svg>
                            Método 2: Ferramenta de Captura
                        </h4>
                        <p>
                            Pressione <strong>Windows + Shift + S</strong> para usar a ferramenta de captura do Windows e selecionar apenas a área do CMD.
                        </p>
                    </div>
                </div>
            </div>

            <!-- Step 5 -->
            <div class="step">
                <div class="step-header">
                    <div class="step-number">5</div>
                    <h3 class="step-title">Salve a captura de tela</h3>
                </div>
                <div class="step-content">
                    <p>
                        <strong>Se usou o método 1:</strong> Abra o Paint (pressione Windows + R, digite "mspaint" e pressione Enter), cole a imagem (Ctrl+V) e salve-a (Ctrl+S).
                    </p>
                    <p>
                        <strong>Se usou o método 2:</strong> Após selecionar a área, a imagem será copiada para a área de transferência. Você pode colá-la diretamente no formulário ou salvá-la primeiro em um editor de imagens.
                    </p>
                </div>
            </div>

            <!-- Alternative Method -->
            <div class="alternative-method">
                <h3 class="alternative-title">
                    <svg class="icon-lightbulb" viewBox="0 0 352 512">
                        <path d="M96.06 454.35c.01 6.29 1.87 12.45 5.36 17.69l17.09 25.69a31.99 31.99 0 0 0 26.64 14.28h61.71a31.99 31.99 0 0 0 26.64-14.28l17.09-25.69a31.989 31.989 0 0 0 5.36-17.69l.04-38.35H96.01l.05 38.35zM0 176c0 44.37 16.45 84.85 43.56 115.78 16.52 18.85 42.36 58.23 52.21 91.45.04.26.07.52.11.78h160.24c.04-.26.07-.51.11-.78 9.85-33.22 35.69-72.6 52.21-91.45C335.55 260.85 352 220.37 352 176 352 78.61 272.91-.3 175.45 0 73.44.31 0 82.97 0 176zm176-80c-44.11 0-80 35.89-80 80 0 8.84-7.16 16-16 16s-16-7.16-16-16c0-61.76 50.24-112 112-112 8.84 0 16 7.16 16 16s-7.16 16-16 16z"/>
                    </svg>
                    Método alternativo: PowerShell
                </h3>
                <p>
                    Se o comando WMIC não funcionar, você pode usar o PowerShell. Pressione <strong>Windows + X</strong> e selecione "Windows PowerShell" ou "Terminal".
                </p>
                <div class="code-block">
                    <code>Get-WmiObject win32_bios | Select-Object SerialNumber</code>
                </div>
            </div>

            <!-- Action Buttons -->
            <div class="action-buttons">
                <button id="backButton" class="button button-secondary">
                    Voltar
                </button>
                <button id="doneButton" class="button button-primary">
                    Entendi, concluir
                </button>
            </div>
        </div>

        <!-- Help Box -->
        <div class="help-box">
            <h3 class="help-title">
                <svg class="icon-question" viewBox="0 0 512 512">
                    <path d="M504 256c0 136.997-111.043 248-248 248S8 392.997 8 256C8 119.083 119.043 8 256 8s248 111.083 248 248zM262.655 90c-54.497 0-89.255 22.957-116.549 63.758-3.536 5.286-2.353 12.415 2.715 16.258l34.699 26.31c5.205 3.947 12.621 3.008 16.665-2.122 17.864-22.658 30.113-35.797 57.303-35.797 20.429 0 45.698 13.148 45.698 32.958 0 14.976-12.363 22.667-32.534 33.976C247.128 238.528 216 254.941 216 296v4c0 6.627 5.373 12 12 12h56c6.627 0 12-5.373 12-12v-1.333c0-28.462 83.186-29.647 83.186-106.667 0-58.002-60.165-102-116.531-102zM256 338c-25.365 0-46 20.635-46 46 0 25.364 20.635 46 46 46s46-20.636 46-46c0-25.365-20.635-46-46-46z"/>
                </svg>
                Precisa de ajuda?
            </h3>
            <p>
                Se você estiver com dificuldades para encontrar o número de série do seu notebook, entre em contato com o suporte de TI.
            </p>
            <div class="contact-info">
                <div class="contact-item">
                    <svg class="icon-contact" viewBox="0 0 512 512">
                        <path d="M493.4 24.6l-104-24c-11.3-2.6-22.9 3.3-27.5 13.9l-48 112c-4.2 9.8-1.4 21.3 6.9 28l60.6 49.6c-36 76.7-98.9 140.5-177.2 177.2l-49.6-60.6c-6.8-8.3-18.2-11.1-28-6.9l-112 48C3.9 366.5-2 378.1.6 389.4l24 104C27.1 504.2 36.7 512 48 512c256.1 0 464-207.5 464-464 0-11.2-7.7-20.9-18.6-23.4z"/>
                    </svg>
                    <span>Ramal: 1234</span>
                </div>
                <div class="contact-item">
                    <svg class="icon-contact" viewBox="0 0 512 512">
                        <path d="M502.3 190.8c3.9-3.1 9.7-.2 9.7 4.7V400c0 26.5-21.5 48-48 48H48c-26.5 0-48-21.5-48-48V195.6c0-5 5.7-7.8 9.7-4.7 22.4 17.4 52.1 39.5 154.1 113.6 21.1 15.4 56.7 47.8 92.2 47.6 35.7.3 72-32.8 92.3-47.6 102-74.1 131.6-96.3 154-113.7zM256 320c23.2.4 56.6-29.2 73.4-41.4 132.7-96.3 142.8-104.7 173.4-128.7 5.8-4.5 9.2-11.5 9.2-18.9v-19c0-26.5-21.5-48-48-48H48C21.5 64 0 85.5 0 112v19c0 7.4 3.4 14.3 9.2 18.9 30.6 23.9 40.7 32.4 173.4 128.7 16.8 12.2 50.2 41.8 73.4 41.4z"/>
                    </svg>
                    <span>suporte.ti@empresa.com.br</span>
                </div>
            </div>
        </div>
    </main>

    <!-- Toast Notification -->
    <div id="toast" class="toast">
        <span id="toastMessage">Comando copiado para a área de transferência!</span>
    </div>

    <script>
        // Copy command functionality
        document.getElementById('copyButton').addEventListener('click', function() {
            const command = 'wmic bios get serialnumber';
            navigator.clipboard.writeText(command).then(function() {
                // Show toast notification
                const toast = document.getElementById('toast');
                toast.classList.add('show');
                
                // Change icon to check
                document.getElementById('copyButton').innerHTML = `
                    <svg class="icon-copy" viewBox="0 0 512 512">
                        <path d="M173.898 439.404l-166.4-166.4c-9.997-9.997-9.997-26.206 0-36.204l36.203-36.204c9.997-9.998 26.207-9.998 36.204 0L192 312.69 432.095 72.596c9.997-9.997 26.207-9.997 36.204 0l36.203 36.204c9.997 9.997 9.997 26.206 0 36.204l-294.4 294.401c-9.998 9.997-26.207 9.997-36.204-.001z"/>
                    </svg>
                `;
                
                // Hide toast after 3 seconds
                setTimeout(function() {
                    toast.classList.remove('show');
                    // Change icon back to copy
                    document.getElementById('copyButton').innerHTML = `
                        <svg class="icon-copy" viewBox="0 0 448 512">
                            <path d="M320 448v40c0 13.255-10.745 24-24 24H24c-13.255 0-24-10.745-24-24V120c0-13.255 10.745-24 24-24h72v296c0 30.879 25.121 56 56 56h168zm0-344V0H152c-13.255 0-24 10.745-24 24v368c0 13.255 10.745 24 24 24h272c13.255 0 24-10.745 24-24V128H344c-13.2 0-24-10.8-24-24zm120.971-31.029L375.029 7.029A24 24 0 0 0 358.059 0H352v96h96v-6.059a24 24 0 0 0-7.029-16.97z"/>
                        </svg>
                    `;
                }, 3000);
            });
        });

        // Button actions
        document.getElementById('backButton').addEventListener('click', function() {
            // In a real implementation, this would navigate back to the previous page
            alert('Voltando para a página anterior...');
        });

        document.getElementById('doneButton').addEventListener('click', function() {
            // In a real implementation, this would mark the guide as completed
            alert('Guia concluído! Retornando ao formulário...');
        });
    </script>
</body>
</html>
```
css
```
/* Base styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background-color: #f5f5f5;
    color: #2e2e2e;
    line-height: 1.5;
}

/* Header styles */
header {
    background-color: #2e2e2e;
    color: white;
    padding: 12px 20px;
}

.header-content {
    display: flex;
    align-items: center;
}

.logo {
    height: 30px;
    margin-right: 15px;
}

.header-title {
    font-size: 18px;
    font-weight: 600;
}

/* Breadcrumb styles */
.breadcrumb {
    background-color: #f1f1f1;
    padding: 8px 20px;
    border-bottom: 1px solid #ddd;
    font-size: 14px;
}

.breadcrumb a {
    color: #2e2e2e;
    text-decoration: none;
}

.breadcrumb a:hover {
    text-decoration: underline;
}

/* Main content styles */
main {
    max-width: 800px;
    margin: 20px auto;
    padding: 0 20px;
}

.card {
    background-color: white;
    border-radius: 4px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
    padding: 25px;
    margin-bottom: 20px;
}

.page-title {
    color: #2e2e2e;
    font-size: 24px;
    margin-top: 0;
    margin-bottom: 20px;
    font-weight: 600;
    border-bottom: 1px solid #eee;
    padding-bottom: 15px;
}

.description {
    color: #666;
    margin-bottom: 25px;
}

/* Step styles */
.step {
    margin-bottom: 30px;
}

.step-header {
    display: flex;
    align-items: flex-start;
    margin-bottom: 10px;
}

.step-number {
    background-color: #2196F3;
    color: white;
    width: 28px;
    height: 28px;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-right: 15px;
    flex-shrink: 0;
    font-weight: 600;
}

.step-title {
    margin: 0;
    font-size: 18px;
    font-weight: 600;
    color: #2e2e2e;
}

.step-content {
    margin-left: 43px;
}

.step-content p {
    margin-top: 5px;
    color: #555;
    margin-bottom: 10px;
}

.icon-container {
    background-color: #f9f9f9;
    border: 1px solid #eee;
    border-radius: 4px;
    padding: 15px;
    text-align: center;
    margin-top: 10px;
}

/* Code block styles */
.code-block {
    background-color: #2e2e2e;
    color: white;
    border-radius: 4px;
    padding: 15px;
    font-family: monospace;
    margin: 10px 0;
    position: relative;
}

.code-block code {
    display: block;
    white-space: pre-wrap;
}

.copy-button {
    position: absolute;
    top: 8px;
    right: 8px;
    background: none;
    border: none;
    color: #aaa;
    cursor: pointer;
    padding: 0;
}

.copy-button:hover {
    color: white;
}

/* Info box styles */
.info-box {
    background-color: #e8f4fd;
    border-left: 4px solid #2196F3;
    padding: 15px;
    margin: 15px 0;
}

.info-title {
    margin-top: 0;
    margin-bottom: 10px;
    color: #2e2e2e;
    font-size: 16px;
    display: flex;
    align-items: center;
}

/* Alternative method styles */
.alternative-method {
    margin-top: 40px;
    background-color: #f9f9f9;
    border: 1px solid #eee;
    border-radius: 4px;
    padding: 20px;
}

.alternative-title {
    margin-top: 0;
    color: #2e2e2e;
    font-size: 18px;
    font-weight: 600;
    margin-bottom: 15px;
    display: flex;
    align-items: center;
}

/* Action buttons styles */
.action-buttons {
    margin-top: 30px;
    display: flex;
    justify-content: flex-end;
    border-top: 1px solid #eee;
    padding-top: 20px;
}

.button {
    padding: 10px 20px;
    border-radius: 4px;
    font-weight: 600;
    cursor: pointer;
}

.button-secondary {
    background-color: #f5f5f5;
    border: 1px solid #ddd;
    color: #333;
    margin-right: 10px;
}

.button-primary {
    background-color: #2196F3;
    border: none;
    color: white;
}

.button-secondary:hover {
    background-color: #e5e5e5;
}

.button-primary:hover {
    background-color: #0d8aee;
}

/* Help box styles */
.help-box {
    background-color: white;
    border-radius: 4px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
    padding: 20px;
}

.help-title {
    margin-top: 0;
    color: #2e2e2e;
    font-size: 18px;
    font-weight: 600;
    margin-bottom: 15px;
    display: flex;
    align-items: center;
}

.contact-info {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
    margin-top: 15px;
}

.contact-item {
    display: flex;
    align-items: center;
}

/* Toast notification styles */
.toast {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background-color: #323232;
    color: white;
    padding: 12px 24px;
    border-radius: 4px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.3);
    display: none;
    z-index: 1000;
    opacity: 0;
    transition: opacity 0.3s ease;
}

.toast.show {
    display: block;
    opacity: 1;
}

/* Icon styles */
.icon-large {
    width: 40px;
    height: 40px;
    fill: #2196F3;
}

.icon-copy {
    width: 16px;
    height: 16px;
    fill: currentColor;
}

.icon-info {
    width: 16px;
    height: 16px;
    fill: #2196F3;
    margin-right: 8px;
}

.icon-lightbulb {
    width: 16px;
    height: 16px;
    fill: #FFC107;
    margin-right: 10px;
}

.icon-question {
    width: 16px;
    height: 16px;
    fill: #2196F3;
    margin-right: 10px;
}

.icon-contact {
    width: 14px;
    height: 14px;
    fill: #2196F3;
    margin-right: 8px;
}
```
