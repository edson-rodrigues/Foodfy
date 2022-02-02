## Foodfy

Repositório do desafio final do Bootcamp Launchbase.
<br>
##Como subir em desenvolvimento

Para clonar e executar essa aplicação você vai precisar dos seguintes softwares instalados em seu computador: 
- Git
- Node
- PostgreSQL(Versão 12.9!)

### Instalar dependências

```bash
# Clonar este repositório:
$ git clone https://github.com/i-ramoss/Foodfy.git

# Entrar no repositório:
$ cd Foodfy

# Instalar as dependências:
$ npm install
```

### Configuração do Banco de Dados

Além do [PostgreSQL], instale o [Postbird][postbird] para gerenciamento e visualização do BD numa interface gráfica. <br>
Após essas instalações, ligue o PostgreSQL.

#### Windows:

1. Abra o Powershell como administrador, e navegue até a pasta de instalação:
```bash
$ cd "C:\Program Files\PostgreSQL\13\bin\"
```

2. Inicie o postgres com o comando abaixo:
```bash
$ .\pg_ctl.exe -D "C:\Program Files\PostgreSQL\13\data" start
```

3. Após o uso, o comando para desligá-lo é:
```bash
$ .\pg_ctl.exe -D "C:\Program Files\PostgreSQL\13\data" stop
```

### Criando a base no Postbird

Após ligar o Postgres, abra o Postbird e crie um banco de dados, de nome foodfy. *As informações de usuário e senha do postgres estão no arquivo src/config/db.js*. <br>
Quando conectado, crie um banco de dados com o nome de foodfy. Após isso, importe um arquivo .sql e utilize o que está na raiz deste repositório. <br>
Se não for possível realizar a importação, abra o arquivo sql e *copie toda a query* para a sessão de Query do Postbird e clique em Run Query<br>
Caso as tabelas tenham sido criadas, a importação ocorreu com sucesso.

### Executar a aplicação
```bash
# Entre no repositório:
$ cd Foodfy

# Inicie a aplicação:
$ npm start

# A aplicação estará rodando na porta 5000 (http://localhost:5000/)

# Popule o DB com dados falsos, utilizando o Faker.js
$ node seeds.js
```
