HTML
```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ServiceNow - Gerenciamento de Notebooks</title>
    <style>
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

        /* Main page styles */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .page-header {
            background-color: #2e2e2e;
            color: white;
            padding: 15px 20px;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
        }

        .page-logo {
            height: 30px;
            margin-right: 15px;
        }

        .page-title {
            font-size: 20px;
            font-weight: 600;
        }

        .content-card {
            background-color: white;
            border-radius: 4px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
            padding: 25px;
            margin-bottom: 20px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
        }

        .form-input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-family: inherit;
            font-size: 14px;
        }

        .button {
            padding: 10px 20px;
            border-radius: 4px;
            font-weight: 600;
            cursor: pointer;
        }

        .button-primary {
            background-color: #2196F3;
            border: none;
            color: white;
        }

        .button-secondary {
            background-color: #f5f5f5;
            border: 1px solid #ddd;
            color: #333;
        }

        .button-link {
            background: none;
            border: none;
            color: #2196F3;
            padding: 0;
            font-size: 14px;
            text-decoration: underline;
            cursor: pointer;
        }

        /* Modal styles */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0, 0, 0, 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1000;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }

        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .modal {
            background-color: white;
            border-radius: 4px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            width: 90%;
            max-width: 800px;
            max-height: 90vh;
            overflow-y: auto;
            transform: translateY(-20px);
            transition: transform 0.3s ease;
            position: relative;
        }

        .modal-overlay.active .modal {
            transform: translateY(0);
        }

        .modal-close {
            position: absolute;
            top: 15px;
            right: 15px;
            background: none;
            border: none;
            font-size: 24px;
            line-height: 1;
            color: #999;
            cursor: pointer;
            z-index: 10;
        }

        .modal-close:hover {
            color: #333;
        }

        /* Header styles for modal */
        .modal-header {
            background-color: #2e2e2e;
            color: white;
            padding: 15px 20px;
            border-top-left-radius: 4px;
            border-top-right-radius: 4px;
        }

        .modal-title {
            font-size: 18px;
            font-weight: 600;
        }

        .modal-body {
            padding: 20px;
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
            margin-top: 30px;
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
            z-index: 1100;
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
    </style>
</head>
<body>
    <!-- Main Page Content -->
    <header class="page-header">
        <img src="https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/images/company-library/logo/servicenow-logo-white.svg" alt="ServiceNow Logo" class="page-logo">
        <h1 class="page-title">Gerenciamento de Notebooks</h1>
    </header>

    <div class="container">
        <div class="content-card">
            <h2 style="margin-bottom: 20px;">Registro de Notebook</h2>
            
            <form id="notebook-form">
                <div class="form-group">
                    <label for="model" class="form-label">Modelo do Notebook</label>
                    <select id="model" class="form-input" required>
                        <option value="" disabled selected>Selecione o modelo</option>
                        <option value="dell-latitude">Dell Latitude</option>
                        <option value="dell-xps">Dell XPS</option>
                        <option value="hp-elitebook">HP EliteBook</option>
                        <option value="lenovo-thinkpad">Lenovo ThinkPad</option>
                        <option value="macbook-pro">MacBook Pro</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label for="serial" class="form-label">Número de Série</label>
                    <input type="text" id="serial" class="form-input" placeholder="Ex: ABC123XYZ" required>
                    <button type="button" id="openModalBtn" class="button-link" style="margin-top: 8px;">
                        Como encontrar o número de série?
                    </button>
                </div>
                
                <div class="form-group">
                    <label for="branch" class="form-label">Agência</label>
                    <input type="text" id="branch" class="form-input" placeholder="Código da agência" required>
                </div>
                
                <div style="display: flex; justify-content: flex-end;">
                    <button type="submit" class="button button-primary">Registrar Notebook</button>
                </div>
            </form>
        </div>
    </div>

    <!-- Modal Overlay -->
    <div id="modalOverlay" class="modal-overlay">
        <div class="modal">
            <button id="closeModalBtn" class="modal-close">&times;</button>
            
            <!-- Modal Header -->
            <div class="modal-header">
                <h2 class="modal-title">Como Encontrar o Número de Série do Notebook</h2>
            </div>
            
            <!-- Modal Body -->
            <div class="modal-body">
                <p style="margin-bottom: 20px; color: #666;">
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
                    <button id="closeModalButton" class="button button-primary">
                        Entendi, voltar ao formulário
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- Toast Notification -->
    <div id="toast" class="toast">
        <span id="toastMessage">Comando copiado para a área de transferência!</span>
    </div>

    <script>
        // Modal functionality
        const modalOverlay = document.getElementById('modalOverlay');
        const openModalBtn = document.getElementById('openModalBtn');
        const closeModalBtn = document.getElementById('closeModalBtn');
        const closeModalButton = document.getElementById('closeModalButton');
        
        // Open modal
        openModalBtn.addEventListener('click', function() {
            modalOverlay.classList.add('active');
            document.body.style.overflow = 'hidden'; // Prevent scrolling of background
        });
        
        // Close modal functions
        function closeModal() {
            modalOverlay.classList.remove('active');
            document.body.style.overflow = ''; // Re-enable scrolling
        }
        
        closeModalBtn.addEventListener('click', closeModal);
        closeModalButton.addEventListener('click', closeModal);
        
        // Close modal when clicking outside
        modalOverlay.addEventListener('click', function(e) {
            if (e.target === modalOverlay) {
                closeModal();
            }
        });
        
        // Prevent closing when clicking inside the modal
        document.querySelector('.modal').addEventListener('click', function(e) {
            e.stopPropagation();
        });

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

        // Form submission
        document.getElementById('notebook-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Notebook registrado com sucesso!');
            this.reset();
        });

        // Keyboard accessibility - close modal with Escape key
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape' && modalOverlay.classList.contains('active')) {
                closeModal();
            }
        });
    </script>
</body>
</html>
```
