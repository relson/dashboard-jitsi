# Telemed

Dashboard para consultas via plataforma Jitsi meet.

![](https://media.giphy.com/media/ZX8Pzv5NZeZQHhkaNO/giphy.gif)
![](https://media.giphy.com/media/OwoeqNSEubhpITPpNA/giphy.gif)

## Como Rodar o Projeto

### Pré-requisitos

É altamente recomendável usar o [NVM (Node Version Manager)](https://github.com/nvm-sh/nvm) para gerenciar a versão do Node.js. Este projeto foi desenvolvido e testado utilizando a versão **18.x** do Node.

- [Instale o NVM](https://github.com/nvm-sh/nvm#installing-and-updating)
- Após a instalação, rode os seguintes comandos para instalar e usar a versão correta do Node.js:
  ```bash
  nvm install 18
  nvm use 18
  ```

### Passos para Instalação

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/seu-usuario/dashboard-jitsi.git
    cd dashboard-jitsi
    ```

2.  **Instale as dependências:**
    O projeto utiliza `yarn` como gerenciador de pacotes.
    ```bash
    yarn install
    ```

3.  **Configure as variáveis de ambiente:**
    Copie o arquivo de exemplo `.env` e preencha com suas configurações locais (banco de dados, etc.).
    ```bash
    cp example.env .env
    ```
    **Atenção:** Abra o arquivo `.env` e configure as credenciais do seu banco de dados e outras informações sensíveis.

4.  **Rode as migrations do banco de dados:**
    Este comando irá criar as tabelas necessárias no seu banco de dados.
    ```bash
    node ace migration:run
    ```

5.  **(Opcional) Rode as seeds do banco de dados:**
    Este comando irá popular o banco de dados com dados iniciais (ex: usuários e perfis de acesso).
    ```bash
    node ace seed
    ```

6.  **Inicie o servidor:**
    ```bash
    yarn start
    ```

Após esses passos, a aplicação estará rodando no endereço e porta configurados (geralmente `http://127.0.0.1:3333`).