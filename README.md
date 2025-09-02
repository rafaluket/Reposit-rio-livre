PROMPT 1
Você é um especialista em desenvolvimento ágil de produtos digitais.
Vamos trabalhar juntos para montar um documento que reflita a criação de uma primeira versão do nosso produto para validação.


Para isso, já pensei em alguns pontos, e quero sua ajuda para duas coisas.
1. Para entender se existe alguma ambiguidade ou dúvida no que escrevi,
2. Para apontar se estou esquecendo de algo, ou algo está muito abrangente ainda.

Segue aqui o que pensei (tire dúvidas):
# Objetivo e sucesso
Plataforma de lembranças, uma capsula digital chamada CronoLove, de um lado realizado por um namorado(a)/casado(a), e do outro a pessoa a quem se destina a lembrança
Foco em realizar uma forma de capsula digital onde consegue adicionar “Nossa Jornada” (Momentos especiais que marcaram a história do casal), playlist, mapa interativo de lugares visitados, fotos, mensagem final de declaração, etc
Criar uma versão ínicial com funções importantes, sucesso é ter os primeiros usuários dos dois lados utilizando


Dúvidas
Faz sentido eu nichar mais do que isso? Que opções eu tenho?


# Quem vai usar
Namorados/casais:
Gostaria de dar um presente digital em forma de capsula para lembrar momentos importantes
# Jobs / Funções
Uma IA para ajudar o usuario a saber se a declaração final está boa
Fazer autenticação
##Na criação da capsula
Escolher tema da capsula
Criar a jornada do casal com a opção de adicionar algumas fotos e descrição básica do lugar, data
Criar album de fotos
Criar mapa interativo de lugares visitados
Criar playlist
Criar declaração final 
Permitir visualização da capsula
Salvamento automático de rascunho


Dúvidas:
Será que está faltando algo?

# Métricas de acompanhamento
O que deveriamos medir?


# O que não precisamos fazer agora, mas pode ser que faça sentido um dia
Prepare caminho para um sistema de pagamento, integração com Stripe ou alguma ferramenta de pagamento mais barato, podendo ser um gerador de pix.
PROMPT 2
#O que significa "utilizando"?
Utilizando, seria criando a capsula, gerando o link e o recebedor abrindo o link.

#Qual é a proposta de valor essencial?
Imagino que todas as citadas devem ser essenciais, pois agregam valor direto ao produto.

#Como o destinatário é notificado?
A capsula pode ser compartilhada por email, whatsapp, copia do link ou até mesmo gerar um QRCODE de impressão para o usuário.

#A cápsula pode ser aberta a qualquer momento ou é "trancada" até uma data específica? (Isso é crucial para o conceito de "cápsula do tempo").
A capsula pode ter as duas formas, tanto trancada quanto aberta. Na aberta o usuário consegue visualizar imediatamente, porém na trancada o usuário recebedor verá um timer de contagem de quando a capsula será liberada.

#A experiência de visualização é em um site, em um app? É interativa?
A experiência será em um site e deve ser totalmente interativa, com elementos que chamam a atenção e emocionam.


#Funcionalidades
##Autenticação
O usuário deve ser capaz de se autenticar

## Criação de uma capsula
Tema padrão muito criativo, interativo e animado(amoroso)
Criar a jornada do casal com a opção de adicionar algumas fotos e descrição básica do lugar, data
Criar album de fotos
Criar mapa interativo de lugares visitados utilizando um sistema de mapa gratuito
Criar playlist
Criar declaração final 
Permitir visualização da capsula
Salvamento de rascunho
Gerar pagamento
Finalizar com gerador de link/QR CODE após o pagamento
##Dashboard do usuário
Exibir capsulas criadas e em rascunho, e outras informações importantes para o usuário.


# Sobre as métricas
Boas ideias, vamos anotar para criar em outro momento.
Próximos passos:
Com essas respostas que te dei, eu quero que você elabore um documento de uma página (one pager), que tem as decisões que conversamos.
As perguntas que não respondi, são pois não sei a resposta e/ou descobriremos juntos durante a jornada
Esse documento será a base para montarmos PRDs de forma inteligente, onde os primeiros PRDs das funcionalidades pensam quais serão as próximas.

PROMPT 3

Elabore os PRDs. Suas instruções são as seguintes:
O objetivo dos PRDs agora será passar para uma IA fazer o desenvolvimento do prototipo. A IA vai escolher as ferramentas e estrutura final, nosso objetivo é definir as funcionalidades e telas.
Pense em como vai quebrar os PRDs para que façam sentido para o desenvolvimento em ordem.
O primeiro PRD deve ter o contexto do que conversamos.

#PROMPT 4 - Definindo modelo de dados
##1. Contexto
O documento a seguir é um PRD (Product Requirements Document). A primeira e mais fundamental etapa do refinamento técnico é extrair todos os requisitos de dados para criar um Modelo de Dados completo. Este modelo servirá como a estrutura de banco de dados para toda a aplicação e será a base para todos os prompts de desenvolvimento de funcionalidades.
## 2. Objetivo
Gere um único e detalhado prompt de desenvolvimento que instrua uma IA, como o Lovable, a criar a estrutura completa do banco de dados (Modelo de Dados) no Supabase, com base no PRD fornecido. Siga as regras e o exemplo de saída abaixo.
## 3. Regras
Para gerar o prompt de saída, siga estritamente os seguintes passos de análise e formatação:
Análise Abrangente: Analise o PRD de ponta a ponta para identificar todas as necessidades de armazenamento de dados, mesmo as implícitas nas jornadas de usuário.
Identificação de Entidades (Tabelas): Identifique e liste as entidades centrais do sistema (ex: Equipamento,usuario, contrato, local/agencia, categoria de equipamento, grupo responsavel). Cada entidade corresponderá a uma tabela no banco de dados.
Listagem de Atributos (Colunas): Para cada tabela, liste todos os seus atributos (campos) necessários, extraindo-os das descrições funcionais e listas de campos no PRD.
Mapeamento de Relacionamentos: Defina as conexões entre as tabelas usando chaves estrangeiras (ex: owner_id na tabela Capsule deve referenciar o id da tabela de usuários).
Especificação de Tipos e Restrições: Para cada atributo, especifique o tipo de dado mais apropriado (TEXT, NUMERIC, DATE, ENUM, ARRAY, etc.) e adicione quaisquer restrições de dados necessárias (não nulo, valor padrão, único, CHECK constraint).
Aplicação de Boas Práticas SQL: Incorpore as melhores práticas específicas do SQL, como o uso de uma tabela profiles para dados públicos de usuários vinculada à autenticação e a recomendação de habilitar Row Level Security (RLS).
Formatação do Prompt de Saída: O resultado final deve ser um texto de prompt único, formatado com clareza, usando títulos ## para tabelas e uma lista simples para os atributos, pronto para ser executado.

#PROMPT 5 - Plano de Desenvolvimento
# 1. Contexto
O documento a seguir é um PRD (Product Requirements Document) para uma nova aplicação de software. Ele precisa ser refinado e quebrado em um plano de desenvolvimento. O plano consistirá em uma lista ordenada de nomes de prompts, que serão enviados sequencialmente a um assistente de IA, como o Lovable, para construir a aplicação passo a passo.
# 2. Objetivo
Gere a lista de prompts que devem ser enviados a cada vez, seguindo as regras e o exemplo de saída a seguir.
# 3. Regras
Para criar a lista, você deve seguir estritamente os seguintes critérios pragmáticos e objetivos para o sequenciamento e agrupamento das funcionalidades:
O Modelo de Dados é Sempre o Primeiro: A sequência de prompts deve, invariavelmente, começar com o prompt de "Definição do Modelo de Dados", que abrange a análise de todo o escopo do PRD.
Agrupar por Jornada de Usuário: Todas as funcionalidades de interface e lógica subsequentes devem ser agrupadas em blocos que representem uma "Jornada de Usuário" completa e coesa. Se uma jornada for excessivamente complexa (especialmente em layout), ela deve ser dividida em prompts menores e mais focados.
Ordenar por Dependência Técnica: A ordem dos prompts de jornada deve seguir estritamente esta hierarquia de prioridade para garantir que cada bloco seja construído sobre uma fundação já funcional:
a. Jornada Pública (Leitura): Primeiro, construir a "vitrine" da aplicação, que expõe os dados ao público (ex: Home page com demonstração de uma capsula finalizada).
b. Jornada de Autenticação: Em seguida, implementar o "portão" de acesso, um pré-requisito para todas as ações restritas.
c. Jornada de Criação de Conteúdo (Escrita no Banco de Dados): Depois, os fluxos que permitem aos usuários "produtores" alimentar a plataforma com dados (ex: criar capsula digital).
d. Jornada de Transação: O "core loop" do negócio que conecta os usuários, criadores e visualizadores (ex: visualizar capsula criada).
Nomenclatura: Os nomes dos prompts devem ser curtos, intuitivos e descrever a principal entrega do bloco.

#PROMPT 6 - Contextualização e criação do modelo de dados
Vamos iniciar a criação de uma plataforma de capsula digital para casais. A primeira e mais importante etapa é definir toda a nossa estrutura de banco de dados no Supabase. Por favor, crie as tabelas e os relacionamentos conforme a especificação detalhada abaixo.

Resumo da Lógica:

A plataforma terá Users (usuários), que podem ser tanto criadores das capsulas quanto visualizadores.

Um User (criador) pode ter várias Capsules(capsulas).

Um User (visualizador) não precisa se autenticar e apenas vê as capsulas já criadas.


Configuração Inicial:
Habilitar RLS (Row Level Security) em todas as tabelas.
Criar um Storage Bucket para armazenar as imagens da aplicação (fotos das cápsulas).

#PROMPT 7 - Criando e Definindo o sistema
Vamos iniciar a criação de uma plataforma de capsula digital para casais. A primeira e mais importante etapa é definir toda a nossa estrutura de banco de dados no Supabase. Por favor, crie as tabelas e os relacionamentos conforme a especificação detalhada abaixo.

Resumo da Lógica:

A plataforma terá Users (usuários), que podem ser tanto criadores das capsulas quanto visualizadores.

Um User (criador) pode ter várias Capsules(capsulas).

Um User (visualizador) não precisa se autenticar e apenas vê as capsulas já criadas.


Configuração Inicial:
Habilitar RLS (Row Level Security) em todas as tabelas.
Criar um Storage Bucket para armazenar as imagens da aplicação (fotos das cápsulas).

# PROMPT 8 - Final
# 1. Contexto
Você está recebendo um PRD (Product Requirements Document) completo. Nesse momento, será feito o refinamento técnico para o trecho da jornada de [Fluxo de Checkout e Geração do Link]. 
# 2. Objetivo
Analisar o PRD fornecido e construir um único e detalhado prompt que contenha todos os requisitos presentes no PRD que tenham relação com o trecho da jornada que está sendo construído. Este prompt de saída será usado para instruir um assistente de IA, como o Lovable, para construir uma parte da aplicação. 
# 3. Regras
Para gerar o prompt de desenvolvimento, siga estritamente estas regras:
Foco Exclusivo: O prompt gerado deve conter instruções apenas para as funcionalidades descritas pelo "Nome do Prompt Alvo". Ignore todas as outras partes do PRD.
Abrangência: Se houver regras relacionadas à jornada que está sendo alvo da construção agora espalhadas em outros tópicos ou seções do PRD, inclua as respectivas regras no prompt, desde que sejam relevantes para o contexto atual.
Especificação da Interface Visual (Views): Extraia do PRD e detalhe todos os requisitos visuais para o escopo do prompt. Especifique:
Telas e Rotas: As páginas a serem criadas (ex: /login, /dashboard).
Layout: A estrutura de cada página (ex: duas colunas, blocos verticais).
Componentes: Elementos reutilizáveis (ex: PropertyCard) ou específicos (ex: formulários, modais, botões).
Estilo: Mencione a biblioteca de design a ser usada (ex: Shadcn/UI com Tailwind CSS).
Especificação da Lógica (Controllers): Extraia do PRD e detalhe todas as regras de comportamento. Especifique:
Ações do Usuário: O que acontece ao clicar em um botão ou submeter um formulário.
Manipulação de Dados: Como a interface interage com o banco de dados. Seja explícito sobre quais tabelas e colunas devem ser lidas (SELECT) ou escritas (INSERT, UPDATE).
Regras Condicionais: Lógica que depende de um estado (ex: se o usuário estiver logado..., se o status da reserva for 'Approved'...).
Navegação: Todos os redirecionamentos entre páginas.
Conexão Direta com Dados: O prompt deve instruir a IA a conectar todos os componentes diretamente ao banco de dados, sem usar dados fictícios (mock data).
# 4. Exemplo de Saída
O prompt que você gerar deve ter o mesmo formato e nível de detalhe do exemplo abaixo (que seria a saída para o alvo "Implementação do Sistema de Autenticação"):
Crie o sistema de autenticação completo da aplicação, cobrindo o fluxo de cadastro e login para todos os usuários. Utilize o Supabase Auth para a lógica de backend.
1. Crie a Página de Acesso (Rota: /login)
Esta página servirá tanto para login quanto para cadastro.
O layout principal deve conter um componente de Abas (Tabs), com "Entrar" e "Cadastrar". A aba "Entrar" deve ser a padrão.

2. Configure a Aba "Cadastrar"
Formulário: Campo para "Nome Completo", "E-mail", "Senha" e botão "Cadastrar".
Lógica Funcional (Supabase): Ao submeter, chame supabase.auth.signUp. Após o sucesso, insira uma nova linha na tabela public.profiles. Após o cadastro, redirecione o usuário para a Homepage (/).

3. Configure a Aba "Entrar"
Formulário: Campo para "E-mail", "Senha" e botão "Entrar".
Lógica Funcional (Supabase): Ao submeter, chame supabase.auth.signInWithPassword. Em caso de sucesso, redirecione para o /dashboard. Em caso de erro, mostre uma mensagem.

4. Gerenciamento de Sessão e Atualização do Header
Implemente um provedor de contexto para gerenciar o estado da sessão.
Modifique o componente de Cabeçalho para ser dinâmico: se logado, mostrar nome e "Sair"; se deslogado, mostrar "Entrar" e "Cadastrar".
A ação "Sair" deve chamar supabase.auth.signOut e redirecionar para a página inicial.


