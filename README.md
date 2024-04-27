# Arquitetura_MVC

# Nome do Projeto: INSPA Animal Welfare Analysis Tool

## Descrição
Este projeto é uma aplicação web responsiva projetada para coletar dados sobre a adoção, compra e abandono de cães e gatos. O objetivo é entender os motivos subjacentes a essas ações para reduzir a negligência e os maus-tratos. A aplicação é compatível com navegadores Chrome e Firefox e otimizada para dispositivos móveis e desktops.

## Arquitetura: MVC (Model-View-Controller)
### Ferramenta de Diagramação: draw.io

### Modelos (Models):
- **Usuários**: Inclui informações como `id`, `nome`, `role`, `email`, e `senha`.
- **Formulários**: Contém campos como `id`, `respostas`, `dados das respostas (data, motivo, tipo de evento)`.

Relações:
- **Usuários** são responsáveis por gerenciar os **Formulários** preenchidos pelos participantes, que podem incluir detalhes sobre adoção, compra e abandono de animais.

### Controladores (Controllers):
- **Users Controller**: 
  - `Procurar`: Localiza usuários no sistema.
  - `Autenticar`: Realiza a autenticação e sessão do usuário.
  - `Atualizar`: Permite a usuários atualizar seus próprios perfis.
- **Dashboard ADM Controller**: 
  - `Procurar`: Filtra e encontra dados específicos para análise.
  - `Listar`: Apresenta dados agregados e individuais para administração.
- **Forms Controller**:
  - `Listar`: Exibe os formulários para serem preenchidos ou revisados.
  - `Gravar`: Registra as respostas submetidas nos formulários.
  - `Procurar`: Procura por respostas específicas para análises detalhadas.

Interações:
- **Controllers** coordenam a entrada dos usuários e a manipulação de dados entre **Models** e **Views**.

### Views (Views):
- **Tela Inicial**: Apresenta a visão geral do projeto e acesso aos formulários.
- **Página de Login**: Interface para entrada segura de usuários administrativos.
- **Página do ADM**: Dashboard administrativo para análise e gerenciamento dos dados coletados.

### Infraestrutura:
- **Servidor**: Hospedagem na nuvem com Node.js e Sails.js, fornecendo um backend robusto e escalável.
- **Banco de Dados**: Banco de dados relacional para armazenamento seguro e estruturado dos dados coletados.

Integração:
- A infraestrutura selecionada permite uma integração eficiente da arquitetura MVC, suportando a escalabilidade necessária e a manutenção facilitada da aplicação.

### Implicações da Arquitetura:
- **Escalabilidade**: A aplicação foi projetada para crescer e se adaptar à medida que novas informações e padrões de dados são identificados.
- **Manutenção**: Com uma arquitetura clara e divisão de responsabilidades, a manutenção torna-se mais direta e menos propensa a erros.
- **Testabilidade**: A modularidade proporcionada pelo MVC facilita a implementação de testes unitários e de integração.
