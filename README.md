# 🚀️ Conceitos Node 🚀️


Este é o resultado do desafio do bootcamp GoStack da RocketSeat!
Trata-se de uma API Rest onde é possível cadastrar, listar, alterar e excluir repositórios, também é possível dar likes em um determinado repositório.


>#### 📋️ Requisitos:
> 
>- [Node.Js](https://nodejs.org/en/download/)
>- [Yarn](https://yarnpkg.com/lang/en/docs/install/)
>- [Insomnia](https://insomnia.rest/download/core/?&ref=)


#### 🤖️ Como utilizar:
- Faça o clone do projeto
- Navegue até o diretório do projeto com o terminal
- No terminal digite ` yarn ` para fazer o download das dependências
- Ainda no terminal digite ` yarn dev ` para inicializar o projeto
- Agora basta testar as rotas no Insomnia

>#### 📝️ Testando as rotas
> Abra o Insomnia
>###### Criando um repositório:
>1. Utilize a URL ` http://localhost:3333/repositories`
>2. Selecione o método **POST**
>3. Clique em **Body** e selecione a opção **JSON**
>> O corpo da requisição deve conter os seguintes campos:
>> ` { `
>>  `"title": "nome do repositório",`
>> `"url": "http://urldorepositorio.com",`
>>  `"techs": ["tecnologia1", "tecnologia2"] ` 
>> `} `
>4. Após preencher os campos, clique em send e o repositório será salvo
>###### Listando repositórios
>1. Utilize a URL ` http://localhost:3333/repositories`
>2. Selecione o método **GET**
>3. Clique em send, serão listados todos os repositórios cadastrados
>###### Alterando um repositório
>1. Utilize a URL  `http://localhost:3333/repositories/:id`
> Em **:id** insira o ID do repositório que deseja alterar, o ID pode ser obtido no cadastro do repositório ou na listagem de repositórios.
>2. Selecione o método **PUT**
>3. Clique em **Body** e selecione a opção **JSON**
>> No corpo da requisição é possivel alterar todos os campos ou apenas um campo
>> Exemplo:
>> `{`
>> `"title": "outro nome de repositório"`
>> `}`
>> Clicando em send será alterado apenas o campo *title* do repositório que foi informado o ID
>###### Deletando um repositório
>1. Utilize a URL  `http://localhost:3333/repositories/:id`
> Em **:id** insira o ID do repositório que deseja deletar, o ID pode ser obtido no cadastro do repositório ou na listagem de repositórios.
>2. Selecione o método **DELETE**
>3. Clique em send, caso o repositório exista será retornado o status ***204 No Content*** para indicar que o repositório foi deletado.
>###### Inserindo like
>1. Utilize a URL  `http://localhost:3333/repositories/:id/like`
> Em **:id** insira o ID do repositório que deseja deletar, o ID pode ser obtido no cadastro do repositório ou na listagem de repositórios.
>2. Selecione o método **POST**
>3. Clique em send, será retornado o repositório com o número de likes

## Obrigado por testar a API! 😁️