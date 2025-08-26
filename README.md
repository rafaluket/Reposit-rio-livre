graph TD
    subgraph Frontend
        User[Usuário] -->|Acessa o site| CloudFront[CloudFront (CDN)];
        CloudFront -->|Busca arquivos estáticos| S3[S3 (React Frontend)];
    end

    subgraph Backend Serverless
        API_Gateway[API Gateway] -->|Dispara função| Lambda[AWS Lambda (Funções de Negócio)];
        User -->|Faz requisições de API| API_Gateway;
    end

    subgraph Gerenciamento e Dados
        Lambda -->|Consulta/Grava| RDS_SQL_Server[RDS para SQL Server];
        Lambda -->|Busca credenciais| Secrets_Manager[Secrets Manager];
        User -->|Autentica| Cognito[Amazon Cognito];
        API_Gateway -->|Autoriza| Cognito;
    end
