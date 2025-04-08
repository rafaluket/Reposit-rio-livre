# Reposit-rio-livre
Livre
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ServiceNow - Notebook Management</title>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap">
    <style>
        /* Reset and base styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.5;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 24px;
        }

        /* Header styles */
        .header {
            display: flex;
            align-items: center;
            margin-bottom: 24px;
        }

        .header img {
            width: 40px;
            height: 40px;
            margin-right: 12px;
        }

        .header h1 {
            font-size: 24px;
            font-weight: 700;
        }

        /* Card styles */
        .card {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            padding: 24px;
            margin-bottom: 24px;
        }

        .card-title {
            font-size: 20px;
            font-weight: 600;
            margin-bottom: 8px;
        }

        .card-description {
            color: #666;
            margin-bottom: 24px;
        }

        /* Tab styles */
        .tabs {
            margin-bottom: 24px;
        }

        .tab-list {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 8px;
            margin-bottom: 24px;
        }

        .tab-button {
            padding: 12px;
            background-color: #f5f5f5;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.2s;
        }

        .tab-button:hover {
            background-color: #e5e5e5;
        }

        .tab-button.active {
            background-color: #3b82f6;
            color: white;
            border-color: #3b82f6;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        /* Form styles */
        .form-group {
            margin-bottom: 16px;
        }

        .form-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 24px;
        }

        @media (min-width: 768px) {
            .form-grid {
                grid-template-columns: 1fr 1fr;
            }
        }

        .form-space {
            display: flex;
            flex-direction: column;
            gap: 16px;
        }

        label {
            display: block;
            font-weight: 500;
            margin-bottom: 8px;
        }

        input, select, textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-family: inherit;
            font-size: 14px;
        }

        textarea {
            min-height: 100px;
            resize: vertical;
        }

        /* Button styles */
        .button {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 10px 16px;
            background-color: #3b82f6;
            color: white;
            border: none;
            border-radius: 4px;
            font-weight: 500;
            cursor: pointer;
            transition: background-color 0.2s;
        }

        .button:hover {
            background-color: #2563eb;
        }

        .button:disabled {
            background-color: #93c5fd;
            cursor: not-allowed;
        }

        .button-outline {
            background-color: transparent;
            color: #3b82f6;
            border: 1px solid #3b82f6;
        }

        .button-outline:hover {
            background-color: #f0f7ff;
        }

        .button-link {
            background: none;
            color: #3b82f6;
            padding: 0;
            font-size: 14px;
            text-decoration: underline;
        }

        .button-link:hover {
            background: none;
            color: #2563eb;
        }

        .button-ghost {
            background: none;
            color: #333;
            padding: 6px;
        }

        .button-ghost:hover {
            background-color: #f5f5f5;
        }

        .button-icon {
            margin-right: 8px;
        }

        /* File upload styles */
        .file-upload {
            border: 2px dashed #ddd;
            border-radius: 8px;
            padding: 24px;
            text-align: center;
        }

        .file-upload-icon {
            font-size: 40px;
            color: #aaa;
            margin-bottom: 8px;
        }

        .file-list {
            margin-top: 16px;
            text-align: left;
        }

        .file-item {
            display: flex;
            align-items: center;
            font-size: 14px;
            color: #666;
        }

        .file-item-icon {
            color: #22c55e;
            margin-right: 4px;
        }

        /* Alert styles */
        .alert {
            padding: 16px;
            border-radius: 4px;
            margin-bottom: 16px;
            display: flex;
            align-items: flex-start;
        }

        .alert-icon {
            margin-right: 12px;
            flex-shrink: 0;
        }

        .alert-content {
            flex: 1;
        }

        .alert-title {
            font-weight: 600;
            margin-bottom: 4px;
        }

        .alert-error {
            background-color: #fee2e2;
            color: #b91c1c;
        }

        .alert-info {
            background-color: #e0f2fe;
            color: #0369a1;
        }

        /* Table styles */
        .table-container {
            border: 1px solid #ddd;
            border-radius: 4px;
            overflow-x: auto;
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }

        th, td {
            padding: 12px 16px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }

        th {
            font-weight: 600;
            background-color: #f9fafb;
        }

        tr:last-child td {
            border-bottom: none;
        }

        .status-badge {
            display: inline-block;
            padding: 2px 8px;
            border-radius: 9999px;
            font-size: 12px;
            font-weight: 500;
        }

        .status-assigned {
            background-color: #dcfce7;
            color: #166534;
        }

        .status-available {
            background-color: #dbeafe;
            color: #1e40af;
        }

        .status-maintenance {
            background-color: #fef9c3;
            color: #854d0e;
        }

        /* Accordion styles */
        .accordion {
            border: 1px solid #ddd;
            border-radius: 4px;
            margin-bottom: 16px;
        }

        .accordion-header {
            padding: 12px 16px;
            font-weight: 500;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .accordion-header:hover {
            background-color: #f9fafb;
        }

        .accordion-content {
            padding: 16px;
            border-top: 1px solid #ddd;
            display: none;
        }

        .accordion-content.active {
            display: block;
        }

        /* Serial number guide styles */
        .guide-step {
            margin-bottom: 20px;
        }

        .step-number {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 24px;
            height: 24px;
            background-color: #dbeafe;
            color: #1e40af;
            border-radius: 50%;
            margin-right: 8px;
            font-size: 14px;
        }

        .step-title {
            font-weight: 500;
            display: flex;
            align-items: center;
            margin-bottom: 8px;
        }

        .step-content {
            margin-left: 32px;
        }

        .code-block {
            background-color: #000;
            color: #fff;
            padding: 12px;
            border-radius: 4px;
            font-family: monospace;
            margin: 8px 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .flex-end {
            display: flex;
            justify-content: flex-end;
        }

        .mt-6 {
            margin-top: 24px;
        }

        .hidden {
            display: none;
        }

        /* Icons */
        .icon {
            display: inline-block;
            width: 1em;
            height: 1em;
            stroke-width: 0;
            stroke: currentColor;
            fill: currentColor;
            vertical-align: middle;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <img src="https://cdn-icons-png.flaticon.com/512/2748/2748558.png" alt="ServiceNow Logo">
            <h1>ServiceNow - Notebook Management</h1>
        </div>

        <div class="card">
            <h2 class="card-title">Revisão de cadastro dos equipamentos de microinformática para agência física</h2>
            <p class="card-description">
                Esta oferta é referente a correção a atribuição de equipamentos de microinformática e telefonia móvel
                associados a determinado colaborador ou estrutura.
            </p>

            <div class="tabs">
                <div class="tab-list">
                    <button class="tab-button active" data-tab="register">Registrar Notebook</button>
                    <button class="tab-button" data-tab="assign">Atribuir Notebook</button>
                    <button class="tab-button" data-tab="unassign">Devolver Notebook</button>
                    <button class="tab-button" data-tab="inventory">Consultar Inventário</button>
                </div>

                <!-- Register Tab -->
                <div id="register-tab" class="tab-content active">
                    <div class="alert alert-info">
                        <span class="alert-icon">ℹ️</span>
                        <div class="alert-content">
                            <p>Preencha o formulário abaixo para solicitar o cadastro de um novo notebook no sistema.</p>
                        </div>
                    </div>

                    <div id="registration-form">
                        <form id="notebook-registration-form">
                            <div class="form-grid">
                                <div class="form-space">
                                    <div class="form-group">
                                        <label for="model">Modelo do Notebook</label>
                                        <select id="model" required>
                                            <option value="" disabled selected>Selecione o modelo</option>
                                            <option value="dell-latitude">Dell Latitude</option>
                                            <option value="dell-xps">Dell XPS</option>
                                            <option value="hp-elitebook">HP EliteBook</option>
                                            <option value="lenovo-thinkpad">Lenovo ThinkPad</option>
                                            <option value="macbook-pro">MacBook Pro</option>
                                            <option value="outro">Outro (especificar)</option>
                                        </select>
                                    </div>

                                    <div class="form-group">
                                        <label for="serial">Número de Série</label>
                                        <input type="text" id="serial" placeholder="Ex: ABC123XYZ" required>
                                        <button type="button" class="button-link" id="show-serial-guide">
                                            Como encontrar o número de série?
                                        </button>
                                    </div>

                                    <div class="form-group">
                                        <label for="processor">Processador</label>
                                        <select id="processor">
                                            <option value="" disabled selected>Selecione o processador</option>
                                            <option value="intel-i3">Intel Core i3</option>
                                            <option value="intel-i5">Intel Core i5</option>
                                            <option value="intel-i7">Intel Core i7</option>
                                            <option value="intel-i9">Intel Core i9</option>
                                            <option value="amd-ryzen">AMD Ryzen</option>
                                            <option value="apple-m1">Apple M1</option>
                                            <option value="apple-m2">Apple M2</option>
                                            <option value="outro">Outro (especificar)</option>
                                        </select>
                                    </div>

                                    <div class="form-group">
                                        <label for="memory">Memória RAM</label>
                                        <select id="memory">
                                            <option value="" disabled selected>Selecione a quantidade de memória</option>
                                            <option value="4gb">4GB</option>
                                            <option value="8gb">8GB</option>
                                            <option value="16gb">16GB</option>
                                            <option value="32gb">32GB</option>
                                            <option value="outro">Outro (especificar)</option>
                                        </select>
                                    </div>
                                </div>

                                <div class="form-space">
                                    <div class="form-group">
                                        <label for="storage">Armazenamento</label>
                                        <select id="storage">
                                            <option value="" disabled selected>Selecione o tipo de armazenamento</option>
                                            <option value="ssd-256">SSD 256GB</option>
                                            <option value="ssd-512">SSD 512GB</option>
                                            <option value="ssd-1tb">SSD 1TB</option>
                                            <option value="hdd-500">HDD 500GB</option>
                                            <option value="hdd-1tb">HDD 1TB</option>
                                            <option value="outro">Outro (especificar)</option>
                                        </select>
                                    </div>

                                    <div class="form-group">
                                        <label for="branch">Agência</label>
                                        <input type="text" id="branch" placeholder="Código da agência" required>
                                    </div>

                                    <div class="form-group">
                                        <label for="notes">Observações</label>
                                        <textarea id="notes" placeholder="Informações adicionais sobre o equipamento"></textarea>
                                    </div>
                                </div>
                            </div>

                            <div class="card">
                                <label for="file-upload" class="form-group">Anexar foto do número de série</label>
                                <div class="file-upload">
                                    <input type="file" id="file-upload" accept="image/*" multiple class="hidden">
                                    <div>
                                        <div class="file-upload-icon">📷</div>
                                        <p>Tire uma foto do número de série ou</p>
                                        <button type="button" class="button button-outline" id="select-file-button">
                                            <span class="button-icon">📤</span>
                                            Selecionar arquivo
                                        </button>
                                    </div>
                                    <div id="file-list" class="file-list hidden">
                                        <p><strong>Arquivos selecionados:</strong></p>
                                        <ul id="selected-files"></ul>
                                    </div>
                                </div>
                            </div>

                            <div class="accordion">
                                <div class="accordion-header" id="accordion-trigger">
                                    Por que precisamos da foto do número de série?
                                    <span>▼</span>
                                </div>
                                <div class="accordion-content">
                                    <p>
                                        A foto do número de série é necessária para confirmar a identidade do equipamento
                                        e garantir que as informações fornecidas estão corretas. Isso ajuda a manter
                                        nosso inventário preciso e facilita o suporte técnico quando necessário.
                                    </p>
                                </div>
                            </div>

                            <div class="flex-end">
                                <button type="submit" class="button" id="register-submit">
                                    Solicitar cadastro
                                </button>
                            </div>
                        </form>
                    </div>

                    <!-- Serial Number Guide -->
                    <div id="serial-number-guide" class="hidden">
                        <div class="card">
                            <div style="display: flex; align-items: center; margin-bottom: 16px;">
                                <button class="button button-ghost" id="close-guide">
                                    ←
                                </button>
                                <h3 style="font-size: 18px; font-weight: 500;">Como encontrar o número de série do notebook via CMD</h3>
                            </div>

                            <div>
                                <div class="guide-step">
                                    <h4 class="step-title">
                                        <span class="step-number">1</span>
                                        Abra o Prompt de Comando (CMD)
                                    </h4>
                                    <div class="step-content">
                                        <p>Pressione a tecla Windows + R, digite "cmd" e pressione Enter.</p>
                                        <div style="background-color: #f5f5f5; padding: 16px; border-radius: 8px; text-align: center; margin-top: 8px;">
                                            <span style="font-size: 40px;">⌨️</span>
                                        </div>
                                    </div>
                                </div>

                                <div class="guide-step">
                                    <h4 class="step-title">
                                        <span class="step-number">2</span>
                                        Digite o comando para obter o número de série
                                    </h4>
                                    <div class="step-content">
                                        <div class="code-block">
                                            <span>wmic bios get serialnumber</span>
                                            <button class="button button-ghost" id="copy-command">📋</button>
                                        </div>
                                        <p>
                                            Este comando exibirá o número de série do seu notebook diretamente no prompt de comando.
                                        </p>
                                    </div>
                                </div>

                                <div class="guide-step">
                                    <h4 class="step-title">
                                        <span class="step-number">3</span>
                                        Resultado esperado
                                    </h4>
                                    <div class="step-content">
                                        <div class="code-block">
                                            <div>
                                                <p>SerialNumber</p>
                                                <p>ABC123XYZ</p>
                                            </div>
                                        </div>
                                        <p>
                                            O número abaixo de "SerialNumber" é o número de série do seu notebook.
                                        </p>
                                    </div>
                                </div>

                                <div class="guide-step">
                                    <h4 class="step-title">
                                        <span class="step-number">4</span>
                                        Tire uma captura de tela do resultado
                                    </h4>
                                    <div class="step-content">
                                        <p>
                                            <strong>Método 1:</strong> Pressione a tecla "Print Screen" ou "PrtScn" no seu teclado para copiar a
                                            tela inteira.
                                        </p>
                                        <p>
                                            <strong>Método 2:</strong> Pressione "Windows + Shift + S" para usar a ferramenta de captura do Windows
                                            e selecionar apenas a área do CMD.
                                        </p>
                                        <div style="background-color: #f5f5f5; padding: 16px; border-radius: 8px; text-align: center; margin-top: 8px;">
                                            <span style="font-size: 40px;">📷</span>
                                        </div>
                                    </div>
                                </div>

                                <div class="guide-step">
                                    <h4 class="step-title">
                                        <span class="step-number">5</span>
                                        Salve a captura de tela
                                    </h4>
                                    <div class="step-content">
                                        <p>
                                            <strong>Se usou o método 1:</strong> Abra o Paint (pressione Windows + R, digite "mspaint" e pressione
                                            Enter), cole a imagem (Ctrl+V) e salve-a (Ctrl+S).
                                        </p>
                                        <p>
                                            <strong>Se usou o método 2:</strong> Após selecionar a área, a imagem será copiada para a área de
                                            transferência. Você pode colá-la diretamente no formulário ou salvá-la primeiro em um editor de imagens.
                                        </p>
                                    </div>
                                </div>

                                <div class="guide-step">
                                    <h4 class="step-title">
                                        <span class="step-number">6</span>
                                        Método alternativo: PowerShell
                                    </h4>
                                    <div class="step-content">
                                        <p>
                                            Se o comando WMIC não funcionar, você pode usar o PowerShell. Pressione Windows + X e selecione "Windows
                                            PowerShell" ou "Terminal".
                                        </p>
                                        <div class="code-block">
                                            <span>Get-WmiObject win32_bios | Select-Object SerialNumber</span>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <div class="mt-6 flex-end">
                                <button class="button" id="close-guide-button">Entendi, voltar ao formulário</button>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Assign Tab -->
                <div id="assign-tab" class="tab-content">
                    <div class="alert alert-info">
                        <span class="alert-icon">ℹ️</span>
                        <div class="alert-content">
                            <p>Atribua um notebook a um colaborador preenchendo o formulário abaixo.</p>
                        </div>
                    </div>

                    <div class="card">
                        <div class="form-grid" style="grid-template-columns: 1fr 2fr;">
                            <div class="form-group">
                                <label for="search-by">Buscar por</label>
                                <select id="search-by">
                                    <option value="serial">Número de Série</option>
                                    <option value="tag">Tag de Patrimônio</option>
                                    <option value="model">Modelo</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label for="search-term">Termo de busca</label>
                                <div style="display: flex; gap: 8px;">
                                    <input type="text" id="search-term" placeholder="Ex: ABC123XYZ">
                                    <button type="button" class="button" id="search-button">🔍</button>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div id="notebook-not-found" class="alert alert-error hidden">
                        <span class="alert-icon">⚠️</span>
                        <div class="alert-content">
                            <h4 class="alert-title">Notebook não encontrado</h4>
                            <p>
                                Não foi possível encontrar um notebook com os critérios informados. Verifique as informações e tente
                                novamente ou registre um novo notebook.
                            </p>
                        </div>
                    </div>

                    <div id="notebook-found" class="hidden">
                        <form id="assignment-form">
                            <div class="card">
                                <h3 style="font-weight: 500; margin-bottom: 16px;">Detalhes do Notebook</h3>
                                <div class="form-grid">
                                    <div>
                                        <label style="color: #666; font-size: 14px;">Número de Série</label>
                                        <p style="font-weight: 500;" id="found-serial">ABC123XYZ</p>
                                    </div>
                                    <div>
                                        <label style="color: #666; font-size: 14px;">Modelo</label>
                                        <p style="font-weight: 500;" id="found-model">Dell Latitude 5420</p>
                                    </div>
                                    <div>
                                        <label style="color: #666; font-size: 14px;">Status</label>
                                        <p style="font-weight: 500;" id="found-status">Disponível</p>
                                    </div>
                                    <div>
                                        <label style="color: #666; font-size: 14px;">Último Atribuído</label>
                                        <p style="font-weight: 500;" id="found-last-assigned">N/A</p>
                                    </div>
                                </div>
                            </div>

                            <div class="form-grid">
                                <div class="form-space">
                                    <h3 style="font-weight: 500;">Informações do Colaborador</h3>
                                    <div class="form-group">
                                        <label for="employee-id">Matrícula</label>
                                        <input type="text" id="employee-id" placeholder="Ex: F12345" required>
                                    </div>
                                    <div class="form-group">
                                        <label for="employee-name">Nome Completo</label>
                                        <input type="text" id="employee-name" placeholder="Nome do colaborador" required>
                                    </div>
                                    <div class="form-group">
                                        <label for="employee-department">Departamento</label>
                                        <input type="text" id="employee-department" placeholder="Ex: TI, RH, Financeiro" required>
                                    </div>
                                </div>

                                <div class="form-space">
                                    <h3 style="font-weight: 500;">Informações da Agência</h3>
                                    <div class="form-group">
                                        <label for="branch-code">Código da Agência</label>
                                        <input type="text" id="branch-code" placeholder="Ex: 1234" required>
                                    </div>
                                    <div class="form-group">
                                        <label for="branch-name">Nome da Agência</label>
                                        <input type="text" id="branch-name" placeholder="Nome da agência" required>
                                    </div>
                                    <div class="form-group">
                                        <label for="assignment-reason">Motivo da Atribuição</label>
                                        <select id="assignment-reason" required>
                                            <option value="" disabled selected>Selecione o motivo</option>
                                            <option value="new-employee">Novo Colaborador</option>
                                            <option value="replacement">Substituição de Equipamento</option>
                                            <option value="transfer">Transferência de Agência</option>
                                            <option value="other">Outro</option>
                                        </select>
                                    </div>
                                </div>
                            </div>

                            <div class="flex-end mt-6">
                                <button type="submit" class="button" id="assign-submit">
                                    Atribuir Notebook
                                </button>
                            </div>
                        </form>
                    </div>
                </div>

                <!-- Unassign Tab -->
                <div id="unassign-tab" class="tab-content">
                    <div class="alert alert-info">
                        <span class="alert-icon">ℹ️</span>
                        <div class="alert-content">
                            <p>Devolva um notebook preenchendo o formulário abaixo.</p>
                        </div>
                    </div>

                    <div class="card">
                        <div class="form-grid" style="grid-template-columns: 1fr 2fr;">
                            <div class="form-group">
                                <label for="unassign-search-by">Buscar por</label>
                                <select id="unassign-search-by">
                                    <option value="serial">Número de Série</option>
                                    <option value="tag">Tag de Patrimônio</option>
                                    <option value="employee">Matrícula do Colaborador</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label for="unassign-search-term">Termo de busca</label>
                                <div style="display: flex; gap: 8px;">
                                    <input type="text" id="unassign-search-term" placeholder="Ex: ABC123XYZ">
                                    <button type="button" class="button" id="unassign-search-button">🔍</button>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div id="unassign-notebook-not-found" class="alert alert-error hidden">
                        <span class="alert-icon">⚠️</span>
                        <div class="alert-content">
                            <h4 class="alert-title">Notebook não encontrado</h4>
                            <p>
                                Não foi possível encontrar um notebook com os critérios informados. Verifique as informações e tente
                                novamente.
                            </p>
                        </div>
                    </div>

                    <div id="unassign-notebook-found" class="hidden">
                        <form id="unassignment-form">
                            <div class="card">
                                <h3 style="font-weight: 500; margin-bottom: 16px;">Detalhes do Notebook</h3>
                                <div class="form-grid">
                                    <div>
                                        <label style="color: #666; font-size: 14px;">Número de Série</label>
                                        <p style="font-weight: 500;" id="unassign-found-serial">ABC123XYZ</p>
                                    </div>
                                    <div>
                                        <label style="color: #666; font-size: 14px;">Modelo</label>
                                        <p style="font-weight: 500;" id="unassign-found-model">Dell Latitude 5420</p>
                                    </div>
                                    <div>
                                        <label style="color: #666; font-size: 14px;">Status</label>
                                        <p style="font-weight: 500;" id="unassign-found-status">Atribuído</p>
                                    </div>
                                    <div>
                                        <label style="color: #666; font-size: 14px;">Atribuído a</label>
                                        <p style="font-weight: 500;" id="unassign-found-assigned-to">João Silva</p>
                                    </div>
                                    <div>
                                        <label style="color: #666; font-size: 14px;">Matrícula</label>
                                        <p style="font-weight: 500;" id="unassign-found-employee-id">F12345</p>
                                    </div>
                                    <div>
                                        <label style="color: #666; font-size: 14px;">Agência</label>
                                        <p style="font-weight: 500;" id="unassign-found-branch">Agência Central (1234)</p>
                                    </div>
                                </div>
                            </div>

                            <div class="form-space">
                                <h3 style="font-weight: 500;">Informações da Devolução</h3>
                                <div class="form-group">
                                    <label for="return-reason">Motivo da Devolução</label>
                                    <select id="return-reason" required>
                                        <option value="" disabled selected>Selecione o motivo</option>
                                        <option value="employee-exit">Desligamento do Colaborador</option>
                                        <option value="replacement">Substituição de Equipamento</option>
                                        <option value="transfer">Transferência de Agência</option>
                                        <option value="repair">Envio para Reparo</option>
                                        <option value="other">Outro</option>
                                    </select>
                                </div>
                                <div class="form-group">
                                    <label for="device-condition">Condição do Equipamento</label>
                                    <select id="device-condition" required>
                                        <option value="" disabled selected>Selecione a condição</option>
                                        <option value="excellent">Excelente</option>
                                        <option value="good">Bom</option>
                                        <option value="fair">Regular</option>
                                        <option value="poor">Ruim</option>
                                        <option value="damaged">Danificado</option>
                                    </select>
                                </div>
                                <div class="form-group">
                                    <label for="return-notes">Observações</label>
                                    <textarea id="return-notes" placeholder="Descreva detalhes sobre a condição do equipamento ou outras informações relevantes"></textarea>
                                </div>
                            </div>

                            <div class="card">
                                <label for="condition-photos" class="form-group">Anexar fotos da condição atual</label>
                                <div class="file-upload">
                                    <input type="file" id="condition-photos" accept="image/*" multiple class="hidden">
                                    <div>
                                        <p>Anexe fotos mostrando a condição atual do notebook</p>
                                        <button type="button" class="button button-outline" id="select-condition-photos-button">
                                            <span class="button-icon">📤</span>
                                            Selecionar arquivos
                                        </button>
                                    </div>
                                    <div id="condition-file-list" class="file-list hidden">
                                        <p><strong>Arquivos selecionados:</strong></p>
                                        <ul id="selected-condition-files"></ul>
                                    </div>
                                </div>
                            </div>

                            <div class="flex-end mt-6">
                                <button type="submit" class="button" id="unassign-submit">
                                    Registrar Devolução
                                </button>
                            </div>
                        </form>
                    </div>
                </div>

                <!-- Inventory Tab -->
                <div id="inventory-tab" class="tab-content">
                    <div class="alert alert-info">
                        <span class="alert-icon">ℹ️</span>
                        <div class="alert-content">
                            <p>Consulte o inventário de notebooks e filtre por diferentes critérios.</p>
                        </div>
                    </div>

                    <div class="card">
                        <div class="form-grid">
                            <div class="form-group">
                                <label for="search-inventory">Buscar</label>
                                <input type="text" id="search-inventory" placeholder="Número de série, modelo, colaborador...">
                            </div>
                            <div class="form-group">
                                <label for="filter-status">Filtrar por Status</label>
                                <select id="filter-status">
                                    <option value="all">Todos</option>
                                    <option value="assigned">Atribuídos</option>
                                    <option value="available">Disponíveis</option>
                                    <option value="maintenance">Em Manutenção</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label for="filter-branch">Filtrar por Agência</label>
                                <input type="text" id="filter-branch" placeholder="Nome ou código da agência">
                            </div>
                        </div>
                    </div>

                    <div class="table-container">
                        <table>
                            <thead>
                                <tr>
                                    <th>Número de Série</th>
                                    <th>Modelo</th>
                                    <th>Status</th>
                                    <th>Atribuído a</th>
                                    <th>Agência</th>
                                    <th>Última Atualização</th>
                                </tr>
                            </thead>
                            <tbody id="inventory-table-body">
                                <!-- Table rows will be populated by JavaScript -->
                            </tbody>
                        </table>
                    </div>

                    <div class="flex-end mt-6">
                        <button type="button" class="button button-outline" id="export-button">
                            <span class="button-icon">📥</span>
                            Exportar Relatório
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Mock data for demonstration
        const mockNotebooks = [
            {
                id: 1,
                serial: "ABC123XYZ",
                model: "Dell Latitude 5420",
                status: "Atribuído",
                assignedTo: "João Silva",
                employeeId: "F12345",
                branch: "Agência Central (1234)",
                lastUpdated: "10/04/2023"
            },
            {
                id: 2,
                serial: "DEF456UVW",
                model: "HP EliteBook 840",
                status: "Disponível",
                assignedTo: "N/A",
                employeeId: "N/A",
                branch: "Estoque TI",
                lastUpdated: "15/03/2023"
            },
            {
                id: 3,
                serial: "GHI789RST",
                model: "Lenovo ThinkPad T14",
                status: "Em manutenção",
                assignedTo: "N/A",
                employeeId: "N/A",
                branch: "Suporte Técnico",
                lastUpdated: "22/03/2023"
            },
            {
                id: 4,
                serial: "JKL012MNO",
                model: "Dell XPS 13",
                status: "Atribuído",
                assignedTo: "Maria Oliveira",
                employeeId: "F67890",
                branch: "Agência Norte (5678)",
                lastUpdated: "05/04/2023"
            },
            {
                id: 5,
                serial: "PQR345STU",
                model: "MacBook Pro 13",
                status: "Atribuído",
                assignedTo: "Carlos Santos",
                employeeId: "F13579",
                branch: "Agência Central (1234)",
                lastUpdated: "01/04/2023"
            }
        ];

        // Tab functionality
        document.querySelectorAll('.tab-button').forEach(button => {
            button.addEventListener('click', () => {
                // Remove active class from all tabs
                document.querySelectorAll('.tab-button').forEach(btn => {
                    btn.classList.remove('active');
                });
                document.querySelectorAll('.tab-content').forEach(content => {
                    content.classList.remove('active');
                });

                // Add active class to clicked tab
                button.classList.add('active');
                document.getElementById(`${button.dataset.tab}-tab`).classList.add('active');
            });
        });

        // Accordion functionality
        document.getElementById('accordion-trigger').addEventListener('click', function() {
            const content = this.nextElementSibling;
            content.classList.toggle('active');
            this.querySelector('span').textContent = content.classList.contains('active') ? '▲' : '▼';
        });

        // Serial Number Guide
        document.getElementById('show-serial-guide').addEventListener('click', function() {
            document.getElementById('registration-form').classList.add('hidden');
            document.getElementById('serial-number-guide').classList.remove('hidden');
        });

        document.getElementById('close-guide').addEventListener('click', function() {
            document.getElementById('registration-form').classList.remove('hidden');
            document.getElementById('serial-number-guide').classList.add('hidden');
        });

        document.getElementById('close-guide-button').addEventListener('click', function() {
            document.getElementById('registration-form').classList.remove('hidden');
            document.getElementById('serial-number-guide').classList.add('hidden');
        });

        // Copy command functionality
        document.getElementById('copy-command').addEventListener('click', function() {
            navigator.clipboard.writeText('wmic bios get serialnumber');
            this.textContent = '✓';
            setTimeout(() => {
                this.textContent = '📋';
            }, 2000);
        });

        // File upload functionality
        document.getElementById('select-file-button').addEventListener('click', function() {
            document.getElementById('file-upload').click();
        });

        document.getElementById('file-upload').addEventListener('change', function(e) {
            const fileList = document.getElementById('file-list');
            const selectedFiles = document.getElementById('selected-files');
            
            if (this.files.length > 0) {
                fileList.classList.remove('hidden');
                selectedFiles.innerHTML = '';
                
                Array.from(this.files).forEach(file => {
                    const li = document.createElement('li');
                    li.className = 'file-item';
                    li.innerHTML = `<span class="file-item-icon">✓</span> ${file.name}`;
                    selectedFiles.appendChild(li);
                });
            } else {
                fileList.classList.add('hidden');
            }
        });

        // Condition photos upload
        document.getElementById('select-condition-photos-button').addEventListener('click', function() {
            document.getElementById('condition-photos').click();
        });

        document.getElementById('condition-photos').addEventListener('change', function(e) {
            const fileList = document.getElementById('condition-file-list');
            const selectedFiles = document.getElementById('selected-condition-files');
            
            if (this.files.length > 0) {
                fileList.classList.remove('hidden');
                selectedFiles.innerHTML = '';
                
                Array.from(this.files).forEach(file => {
                    const li = document.createElement('li');
                    li.className = 'file-item';
                    li.innerHTML = `<span class="file-item-icon">✓</span> ${file.name}`;
                    selectedFiles.appendChild(li);
                });
            } else {
                fileList.classList.add('hidden');
            }
        });

        // Registration form submission
        document.getElementById('notebook-registration-form').addEventListener('submit', function(e) {
            e.preventDefault();
            const submitButton = document.getElementById('register-submit');
            submitButton.disabled = true;
            submitButton.innerHTML = '<span class="button-icon">✓</span> Enviado com sucesso!';
            
            setTimeout(() => {
                submitButton.disabled = false;
                submitButton.textContent = 'Solicitar cadastro';
                this.reset();
                document.getElementById('file-list').classList.add('hidden');
            }, 3000);
        });

        // Search notebook for assignment
        document.getElementById('search-button').addEventListener('click', function() {
            const searchTerm = document.getElementById('search-term').value;
            const notFoundAlert = document.getElementById('notebook-not-found');
            const notebookFound = document.getElementById('notebook-found');
            
            // Mock search functionality
            if (searchTerm.includes('ABC')) {
                notFoundAlert.classList.add('hidden');
                notebookFound.classList.remove('hidden');
                
                // Populate found notebook details
                document.getElementById('found-serial').textContent = 'ABC123XYZ';
                document.getElementById('found-model').textContent = 'Dell Latitude 5420';
                document.getElementById('found-status').textContent = 'Disponível';
                document.getElementById('found-last-assigned').textContent = 'N/A';
            } else {
                notFoundAlert.classList.remove('hidden');
                notebookFound.classList.add('hidden');
            }
        });

        // Assignment form submission
        document.getElementById('assignment-form').addEventListener('submit', function(e) {
            e.preventDefault();
            const submitButton = document.getElementById('assign-submit');
            submitButton.disabled = true;
            submitButton.innerHTML = '<span class="button-icon">✓</span> Atribuído com sucesso!';
            
            setTimeout(() => {
                submitButton.disabled = false;
                submitButton.textContent = 'Atribuir Notebook';
                this.reset();
                document.getElementById('notebook-found').classList.add('hidden');
            }, 3000);
        });

        // Search notebook for unassignment
        document.getElementById('unassign-search-button').addEventListener('click', function() {
            const searchTerm = document.getElementById('unassign-search-term').value;
            const notFoundAlert = document.getElementById('unassign-notebook-not-found');
            const notebookFound = document.getElementById('unassign-notebook-found');
            
            // Mock search functionality
            if (searchTerm.includes('ABC')) {
                notFoundAlert.classList.add('hidden');
                notebookFound.classList.remove('hidden');
                
                // Populate found notebook details
                document.getElementById('unassign-found-serial').textContent = 'ABC123XYZ';
                document.getElementById('unassign-found-model').textContent = 'Dell Latitude 5420';
                document.getElementById('unassign-found-status').textContent = 'Atribuído';
                document.getElementById('unassign-found-assigned-to').textContent = 'João Silva';
                document.getElementById('unassign-found-employee-id').textContent = 'F12345';
                document.getElementById('unassign-found-branch').textContent = 'Agência Central (1234)';
            } else {
                notFoundAlert.classList.remove('hidden');
                notebookFound.classList.add('hidden');
            }
        });

        // Unassignment form submission
        document.getElementById('unassignment-form').addEventListener('submit', function(e) {
            e.preventDefault();
            const submitButton = document.getElementById('unassign-submit');
            submitButton.disabled = true;
            submitButton.innerHTML = '<span class="button-icon">✓</span> Devolução registrada com sucesso!';
            
            setTimeout(() => {
                submitButton.disabled = false;
                submitButton.textContent = 'Registrar Devolução';
                this.reset();
                document.getElementById('unassign-notebook-found').classList.add('hidden');
                document.getElementById('condition-file-list').classList.add('hidden');
            }, 3000);
        });

        // Inventory table functionality
        function populateInventoryTable(notebooks) {
            const tableBody = document.getElementById('inventory-table-body');
            tableBody.innerHTML = '';
            
            if (notebooks.length === 0) {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td colspan="6" style="text-align: center; padding: 16px; color: #666;">
                        Nenhum notebook encontrado com os critérios de busca.
                    </td>
                `;
                tableBody.appendChild(row);
                return;
            }
            
            notebooks.forEach(notebook => {
                const row = document.createElement('tr');
                
                let statusClass = '';
                if (notebook.status === 'Atribuído') {
                    statusClass = 'status-assigned';
                } else if (notebook.status === 'Disponível') {
                    statusClass = 'status-available';
                } else if (notebook.status === 'Em manutenção') {
                    statusClass = 'status-maintenance';
                }
                
                row.innerHTML = `
                    <td style="font-weight: 500;">${notebook.serial}</td>
                    <td>${notebook.model}</td>
                    <td><span class="status-badge ${statusClass}">${notebook.status}</span></td>
                    <td>${notebook.assignedTo}</td>
                    <td>${notebook.branch}</td>
                    <td>${notebook.lastUpdated}</td>
                `;
                
                tableBody.appendChild(row);
            });
        }

        // Initial population of inventory table
        populateInventoryTable(mockNotebooks);

        // Inventory search and filter functionality
        function filterInventory() {
            const searchTerm = document.getElementById('search-inventory').value.toLowerCase();
            const statusFilter = document.getElementById('filter-status').value;
            const branchFilter = document.getElementById('filter-branch').value.toLowerCase();
            
            const filteredNotebooks = mockNotebooks.filter(notebook => {
                const matchesSearch = 
                    notebook.serial.toLowerCase().includes(searchTerm) ||
                    notebook.model.toLowerCase().includes(searchTerm) ||
                    notebook.assignedTo.toLowerCase().includes(searchTerm) ||
                    notebook.branch.toLowerCase().includes(searchTerm);
                
                const matchesStatusFilter = 
                    statusFilter === 'all' ||
                    (statusFilter === 'assigned' && notebook.status === 'Atribuído') ||
                    (statusFilter === 'available' && notebook.status === 'Disponível') ||
                    (statusFilter === 'maintenance' && notebook.status === 'Em manutenção');
                
                const matchesBranchFilter = 
                    branchFilter === '' ||
                    notebook.branch.toLowerCase().includes(branchFilter);
                
                return matchesSearch && matchesStatusFilter && matchesBranchFilter;
            });
            
            populateInventoryTable(filteredNotebooks);
        }

        document.getElementById('search-inventory').addEventListener('input', filterInventory);
        document.getElementById('filter-status').addEventListener('change', filterInventory);
        document.getElementById('filter-branch').addEventListener('input', filterInventory);

        // Export functionality
        document.getElementById('export-button').addEventListener('click', function() {
            alert('Relatório exportado com sucesso!');
        });
    </script>
</body>
</html>
