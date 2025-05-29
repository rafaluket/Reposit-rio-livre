HTML
```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Política PR-200 - Uma Máquina por Colaborador</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.7;
            background-color: #f8f9fa;
            color: #2c3e50;
        }
        
        .email-container {
            max-width: 600px;
            margin: 40px auto;
            background-color: #ffffff;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
        }
        
        .header {
            background: linear-gradient(135deg, #EC7000 0%, #FF8C42 100%);
            padding: 40px 30px;
            text-align: center;
            position: relative;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse"><path d="M 10 0 L 0 0 0 10" fill="none" stroke="rgba(255,255,255,0.1)" stroke-width="0.5"/></pattern></defs><rect width="100" height="100" fill="url(%23grid)"/></svg>');
            opacity: 0.3;
        }
        
        .header-content {
            position: relative;
            z-index: 1;
        }
        
        .logo {
            font-size: 32px;
            font-weight: 900;
            color: white;
            margin-bottom: 8px;
            letter-spacing: -1px;
        }
        
        .subtitle {
            color: rgba(255, 255, 255, 0.9);
            font-size: 16px;
            font-weight: 500;
        }
        
        .content {
            padding: 50px 40px;
        }
        
        .greeting {
            font-size: 18px;
            color: #EC7000;
            font-weight: 600;
            margin-bottom: 8px;
        }
        
        .itubers {
            font-size: 24px;
            color: #003366;
            font-weight: 700;
            margin-bottom: 30px;
            position: relative;
        }
        
        .itubers::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 60px;
            height: 3px;
            background: linear-gradient(90deg, #EC7000, #FF8C42);
            border-radius: 2px;
        }
        
        .main-text {
            font-size: 16px;
            line-height: 1.8;
            color: #34495e;
            margin-bottom: 30px;
        }
        
        .main-text p {
            margin-bottom: 20px;
        }
        
        .policy-highlight {
            background: linear-gradient(135deg, #003366 0%, #004080 100%);
            color: white;
            padding: 25px;
            border-radius: 8px;
            text-align: center;
            margin: 30px 0;
            position: relative;
            overflow: hidden;
        }
        
        .policy-highlight::before {
            content: '📋';
            font-size: 24px;
            position: absolute;
            top: 15px;
            right: 20px;
            opacity: 0.3;
        }
        
        .policy-text {
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 8px;
        }
        
        .policy-subtext {
            font-size: 14px;
            opacity: 0.9;
        }
        
        .links-section {
            background-color: #f8f9fa;
            padding: 25px;
            border-radius: 8px;
            border-left: 4px solid #EC7000;
            margin: 25px 0;
        }
        
        .links-title {
            color: #003366;
            font-weight: 600;
            margin-bottom: 15px;
            font-size: 16px;
        }
        
        .link-item {
            display: block;
            color: #EC7000;
            text-decoration: none;
            padding: 8px 0;
            border-bottom: 1px solid #e9ecef;
            transition: all 0.3s ease;
            font-weight: 500;
        }
        
        .link-item:hover {
            color: #d65a00;
            padding-left: 10px;
        }
        
        .link-item:last-child {
            border-bottom: none;
        }
        
        .cta-section {
            text-align: center;
            margin: 40px 0;
        }
        
        .cta-text {
            font-size: 18px;
            color: #003366;
            font-weight: 600;
            margin-bottom: 20px;
        }
        
        .security-badge {
            display: inline-flex;
            align-items: center;
            background: linear-gradient(135deg, #28a745 0%, #20c997 100%);
            color: white;
            padding: 12px 24px;
            border-radius: 25px;
            font-weight: 600;
            font-size: 14px;
        }
        
        .security-badge::before {
            content: '🔒';
            margin-right: 8px;
            font-size: 16px;
        }
        
        .footer {
            background-color: #003366;
            color: white;
            padding: 30px;
            text-align: center;
        }
        
        .footer-logo {
            font-size: 28px;
            font-weight: 900;
            color: #EC7000;
            margin-bottom: 10px;
        }
        
        .footer-text {
            font-size: 14px;
            opacity: 0.8;
            line-height: 1.5;
        }
        
        @media (max-width: 600px) {
            .email-container {
                margin: 20px;
                border-radius: 8px;
            }
            
            .content {
                padding: 30px 25px;
            }
            
            .header {
                padding: 30px 20px;
            }
            
            .logo {
                font-size: 28px;
            }
            
            .itubers {
                font-size: 20px;
            }
            
            .main-text {
                font-size: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="email-container">
        <!-- Header -->
        <div class="header">
            <div class="header-content">
                <div class="logo">Itaú</div>
                <div class="subtitle">Política Interna PR-200</div>
            </div>
        </div>
        
        <!-- Content -->
        <div class="content">
            <div class="greeting">Olá!</div>
            <div class="itubers">Itubers,</div>
            
            <div class="main-text">
                <p>Estamos reforçando a importância de seguir a <strong>política interna PR-200</strong>, que estabelece que cada colaborador deve utilizar <strong>única e exclusivamente uma máquina</strong> para realizar suas atividades.</p>
                
                <p>Essa medida visa garantir a <strong>segurança das informações</strong>, a <strong>integridade dos dados</strong> e a <strong>eficiência operacional</strong>. O uso de mais de uma máquina por colaborador pode gerar inconsistências e riscos para o ambiente corporativo.</p>
                
                <p>Pedimos que todos revisem suas práticas e certifiquem-se de estar em conformidade com a PR-200. Em caso de dúvidas ou necessidade de suporte, consulte os links:</p>
            </div>
            
            <!-- Policy Highlight -->
            <div class="policy-highlight">
                <div class="policy-text">Uma Máquina = Um Colaborador</div>
                <div class="policy-subtext">Política PR-200 em vigor</div>
            </div>
            
            <!-- Links Section -->
            <div class="links-section">
                <div class="links-title">📚 Links de Suporte e Informações:</div>
                <a href="#" class="link-item">Portal Interno - Política PR-200</a>
                <a href="#" class="link-item">Suporte TI - Dúvidas Técnicas</a>
                <a href="#" class="link-item">FAQ - Perguntas Frequentes</a>
                <a href="mailto:suporte.ti@itau.com.br" class="link-item">Contato Direto - suporte.ti@itau.com.br</a>
            </div>
            
            <div class="main-text">
                <p><strong>Contamos com a colaboração de todos para mantermos um ambiente seguro e organizado.</strong></p>
            </div>
            
            <!-- CTA Section -->
            <div class="cta-section">
                <div class="cta-text">Juntos por um ambiente mais seguro</div>
                <div class="security-badge">Conformidade Garantida</div>
            </div>
        </div>
        
        <!-- Footer -->
        <div class="footer">
            <div class="footer-logo">Itaú</div>
            <div class="footer-text">
                Tecnologia da Informação<br>
                Comunicado oficial sobre Política PR-200
            </div>
        </div>
    </div>
</body>
</html>
```
