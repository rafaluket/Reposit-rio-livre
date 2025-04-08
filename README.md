<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Como Encontrar o Número de Série - ServiceNow</title>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@400;600;700&display=swap">
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body style="font-family: 'Source Sans Pro', sans-serif; margin: 0; padding: 0; background-color: #f5f5f5; color: #2e2e2e; line-height: 1.5;">
    <!-- Header -->
    <header style="background-color: #2e2e2e; color: white; padding: 12px 20px; display: flex; align-items: center;">
        <div style="display: flex; align-items: center;">
            <img src="https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/images/company-library/logo/servicenow-logo-white.svg" alt="ServiceNow Logo" style="height: 30px; margin-right: 15px;">
            <span style="font-size: 18px; font-weight: 600;">Suporte de TI</span>
        </div>
    </header>

    <!-- Breadcrumb -->
    <div style="background-color: #f1f1f1; padding: 8px 20px; border-bottom: 1px solid #ddd; font-size: 14px;">
        <a href="#" style="color: #2e2e2e; text-decoration: none;">Home</a> &gt; 
        <a href="#" style="color: #2e2e2e; text-decoration: none;">Catálogos</a> &gt; 
        <a href="#" style="color: #2e2e2e; text-decoration: none;">Microinformática</a> &gt; 
        <span style="color: #2e2e2e;">Como Encontrar o Número de Série</span>
    </div>

    <!-- Main Content -->
    <main style="max-width: 800px; margin: 20px auto; padding: 0 20px;">
        <div style="background-color: white; border-radius: 4px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24); padding: 25px; margin-bottom: 20px;">
            <h1 style="color: #2e2e2e; font-size: 24px; margin-top: 0; margin-bottom: 20px; font-weight: 600; border-bottom: 1px solid #eee; padding-bottom: 15px;">
                Como Encontrar o Número de Série do Notebook via CMD
            </h1>

            <p style="color: #666; margin-bottom: 25px;">
                Siga este guia passo a passo para encontrar o número de série do seu notebook usando o Prompt de Comando (CMD) do Windows. Este número é essencial para o registro e suporte do seu equipamento.
            </p>

            <!-- Step 1 -->
            <div style="margin-bottom: 30px;">
                <div style="display: flex; align-items: flex-start; margin-bottom: 10px;">
                    <div style="background-color: #2196F3; color: white; width: 28px; height: 28px; border-radius: 50%; display: flex; justify-content: center; align-items: center; margin-right: 15px; flex-shrink: 0;">
                        1
                    </div>
                    <h3 style="margin: 0; font-size: 18px; font-weight: 600; color: #2e2e2e;">Abra o Prompt de Comando (CMD)</h3>
                </div>
                <div style="margin-left: 43px;">
                    <p style="margin-top: 5px; color: #555;">
                        Pressione a tecla <strong>Windows + R</strong>, digite <strong>cmd</strong> e pressione <strong>Enter</strong>.
                    </p>
                    <div style="background-color: #f9f9f9; border: 1px solid #eee; border-radius: 4px; padding: 15px; text-align: center; margin-top: 10px;">
                        <i class="fas fa-terminal" style="font-size: 40px; color: #2196F3;"></i>
                    </div>
                </div>
            </div>

            <!-- Step 2 -->
            <div style="margin-bottom: 30px;">
                <div style="display: flex; align-items: flex-start; margin-bottom: 10px;">
                    <div style="background-color: #2196F3; color: white; width: 28px; height: 28px; border-radius: 50%; display: flex; justify-content: center; align-items: center; margin-right: 15px; flex-shrink: 0;">
                        2
                    </div>
                    <h3 style="margin: 0; font-size: 18px; font-weight: 600; color: #2e2e2e;">Digite o comando para obter o número de série</h3>
                </div>
                <div style="margin-left: 43px;">
                    <p style="margin-top: 5px; color: #555;">
                        Digite o seguinte comando e pressione <strong>Enter</strong>:
                    </p>
                    <div style="background-color: #2e2e2e; color: white; border-radius: 4px; padding: 15px; font-family: monospace; margin-top: 10px; position: relative;">
                        <code style="display: block; white-space: pre-wrap;">wmic bios get serialnumber</code>
                        <button id="copyButton" style="position: absolute; top: 8px; right: 8px; background: none; border: none; color: #aaa; cursor: pointer; font-size: 16px;">
                            <i class="fas fa-copy"></i>
                        </button>
                    </div>
                    <p style="margin-top: 10px; color: #555;">
                        Este comando exibirá o número de série do seu notebook diretamente no prompt de comando.
                    </p>
                </div>
            </div>

            <!-- Step 3 -->
            <div style="margin-bottom: 30px;">
                <div style="display: flex; align-items: flex-start; margin-bottom: 10px;">
                    <div style="background-color: #2196F3; color: white; width: 28px; height: 28px; border-radius: 50%; display: flex; justify-content: center; align-items: center; margin-right: 15px; flex-shrink: 0;">
                        3
                    </div>
                    <h3 style="margin: 0; font-size: 18px; font-weight: 600; color: #2e2e2e;">Resultado esperado</h3>
                </div>
                <div style="margin-left: 43px;">
                    <p style="margin-top: 5px; color: #555;">
                        Você verá uma saída semelhante a esta:
                    </p>
                    <div style="background-color: #2e2e2e; color: white; border-radius: 4px; padding: 15px; font-family: monospace; margin-top: 10px;">
                        <code style="display: block; white-space: pre-wrap;">SerialNumber
ABC123XYZ</code>
                    </div>
                    <p style="margin-top: 10px; color: #555;">
                        O número abaixo de "SerialNumber" é o número de série do seu notebook.
                    </p>
                </div>
            </div>

            <!-- Step 4 -->
            <div style="margin-bottom: 30px;">
                <div style="display: flex; align-items: flex-start; margin-bottom: 10px;">
                    <div style="background-color: #2196F3; color: white; width: 28px; height: 28px; border-radius: 50%; display: flex; justify-content: center; align-items: center; margin-right: 15px; flex-shrink: 0;">
                        4
                    </div>
                    <h3 style="margin: 0; font-size: 18px; font-weight: 600; color: #2e2e2e;">Tire uma captura de tela do resultado</h3>
                </div>
                <div style="margin-left: 43px;">
                    <div style="background-color: #e8f4fd; border-left: 4px solid #2196F3; padding: 15px; margin: 15px 0;">
                        <h4 style="margin-top: 0; margin-bottom: 10px; color: #2e2e2e; font-size: 16px;">
                            <i class="fas fa-info-circle" style="color: #2196F3; margin-right: 8px;"></i>
                            Método 1: Print Screen
                        </h4>
                        <p style="margin: 0; color: #555;">
                            Pressione a tecla <strong>Print Screen</strong> ou <strong>PrtScn</strong> no seu teclado para copiar a tela inteira.
                        </p>
                    </div>
                    
                    <div style="background-color: #e8f4fd; border-left: 4px solid #2196F3; padding: 15px; margin: 15px 0;">
                        <h4 style="margin-top: 0; margin-bottom: 10px; color: #2e2e2e; font-size: 16px;">
                            <i class="fas fa-info-circle" style="color: #2196F3; margin-right: 8px;"></i>
                            Método 2: Ferramenta de Captura
                        </h4>
                        <p style="margin: 0; color: #555;">
                            Pressione <strong>Windows + Shift + S</strong> para usar a ferramenta de captura do Windows e selecionar apenas a área do CMD.
                        </p>
                    </div>
                </div>
            </div>

            <!-- Step 5 -->
            <div style="margin-bottom: 30px;">
                <div style="display: flex; align-items: flex-start; margin-bottom: 10px;">
                    <div style="background-color: #2196F3; color: white; width: 28px; height: 28px; border-radius: 50%; display: flex; justify-content: center; align-items: center; margin-right: 15px; flex-shrink: 0;">
                        5
                    </div>
                    <h3 style="margin: 0; font-size: 18px; font-weight: 600; color: #2e2e2e;">Salve a captura de tela</h3>
                </div>
                <div style="margin-left: 43px;">
                    <p style="margin-top: 5px; color: #555;">
                        <strong>Se usou o método 1:</strong> Abra o Paint (pressione Windows + R, digite "mspaint" e pressione Enter), cole a imagem (Ctrl+V) e salve-a (Ctrl+S).
                    </p>
                    <p style="margin-top: 10px; color: #555;">
                        <strong>Se usou o método 2:</strong> Após selecionar a área, a imagem será copiada para a área de transferência. Você pode colá-la diretamente no formulário ou salvá-la primeiro em um editor de imagens.
                    </p>
                </div>
            </div>

            <!-- Alternative Method -->
            <div style="margin-top: 40px; background-color: #f9f9f9; border: 1px solid #eee; border-radius: 4px; padding: 20px;">
                <h3 style="margin-top: 0; color: #2e2e2e; font-size: 18px; font-weight: 600; margin-bottom: 15px;">
                    <i class="fas fa-lightbulb" style="color: #FFC107; margin-right: 10px;"></i>
                    Método alternativo: PowerShell
                </h3>
                <p style="color: #555; margin-bottom: 15px;">
                    Se o comando WMIC não funcionar, você pode usar o PowerShell. Pressione <strong>Windows + X</strong> e selecione "Windows PowerShell" ou "Terminal".
                </p>
                <div style="background-color: #2e2e2e; color: white; border-radius: 4px; padding: 15px; font-family: monospace;">
                    <code style="display: block; white-space: pre-wrap;">Get-WmiObject win32_bios | Select-Object SerialNumber</code>
                </div>
            </div>

            <!-- Action Buttons -->
            <div style="margin-top: 30px; display: flex; justify-content: flex-end; border-top: 1px solid #eee; padding-top: 20px;">
                <button id="backButton" style="background-color: #f5f5f5; border: 1px solid #ddd; color: #333; padding: 10px 20px; border-radius: 4px; font-weight: 600; cursor: pointer; margin-right: 10px;">
                    Voltar
                </button>
                <button id="doneButton" style="background-color: #2196F3; border: none; color: white; padding: 10px 20px; border-radius: 4px; font-weight: 600; cursor: pointer;">
                    Entendi, concluir
                </button>
            </div>
        </div>

        <!-- Help Box -->
        <div style="background-color: white; border-radius: 4px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24); padding: 20px;">
            <h3 style="margin-top: 0; color: #2e2e2e; font-size: 18px; font-weight: 600; margin-bottom: 15px;">
                <i class="fas fa-question-circle" style="color: #2196F3; margin-right: 10px;"></i>
                Precisa de ajuda?
            </h3>
            <p style="color: #555; margin-bottom: 15px;">
                Se você estiver com dificuldades para encontrar o número de série do seu notebook, entre em contato com o suporte de TI.
            </p>
            <div style="display: flex; flex-wrap: wrap; gap: 15px;">
                <div style="display: flex; align-items: center;">
                    <i class="fas fa-phone" style="color: #2196F3; margin-right: 8px;"></i>
                    <span style="color: #555;">Ramal: 1234</span>
                </div>
                <div style="display: flex; align-items: center;">
                    <i class="fas fa-envelope" style="color: #2196F3; margin-right: 8px;"></i>
                    <span style="color: #555;">suporte.ti@empresa.com.br</span>
                </div>
            </div>
        </div>
    </main>

    <!-- Toast Notification -->
    <div id="toast" style="position: fixed; bottom: 20px; right: 20px; background-color: #323232; color: white; padding: 12px 24px; border-radius: 4px; box-shadow: 0 2px 5px rgba(0,0,0,0.3); display: none; z-index: 1000;">
        <span id="toastMessage">Comando copiado para a área de transferência!</span>
    </div>

    <script>
        // Copy command functionality
        document.getElementById('copyButton').addEventListener('click', function() {
            const command = 'wmic bios get serialnumber';
            navigator.clipboard.writeText(command).then(function() {
                // Show toast notification
                const toast = document.getElementById('toast');
                toast.style.display = 'block';
                
                // Change icon to check
                document.getElementById('copyButton').innerHTML = '<i class="fas fa-check"></i>';
                
                // Hide toast after 3 seconds
                setTimeout(function() {
                    toast.style.display = 'none';
                    // Change icon back to copy
                    document.getElementById('copyButton').innerHTML = '<i class="fas fa-copy"></i>';
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
