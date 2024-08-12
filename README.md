<h2>Mercado de Livro</h2>

O mercado de livro é uma API em Koktin que usa do Framework spring que consiste em um sitema onde podemos inserir, deleter e ver (CRUD) nossos clientes e livros.
<br>
<b>
<p>Configuração usada:</p>
<P>IDE intellij</P>
<p>Sdk java 11.0.10;</p>
<p>Gradle 6.8.2;</p>
<p>Banco de dados Mysql;</p>
<p>Postman para teste.</p>
</b>
<br>

No mercado de livros também foi feito um sistema de login onde temos que ter um usuario com email e senha para acessarmos o nosso registro é gerado um token para acesso. Para conseguirmos o Token o nosso usuario e senha tem que ser igual ao criado e sem o Token não conseguimos acessar os registros. As senhas são criptografados na base de dados.

Foi feito também um sistema de status para esses livros ao invés de excluirmos de fato da base e mudado seu status para clientes muda para "INAPTO" e para livros muda para "CANCELADO".

Para testar o sistema e ver suas funcionalidades faça o passo a passo abaixo:

*Ops usamos também json para pasarmos nossas informações para teste no Postman.

<b>Passo 1.1:</b> Criando usuario na tabela cliente

<br>

![image](https://github.com/user-attachments/assets/5b999258-9f6c-4f13-aa88-0701bafd58d7)

<br>

Senha criptografada no banco de dados.

<br>

![image](https://github.com/user-attachments/assets/ddd46765-b3c4-47b5-8c24-44d03f588bd3)

<br>

<b>Passo 1.2:</b> Fazendo login

![image](https://github.com/user-attachments/assets/289617d2-d747-47c6-a63a-f1478e2b17cb)

<br>

No Headers copie o Token de Autorização para usarmos no passo seguinte.

<b>Passo 1.3:</b> nos autenticando e consutando nossos registros na tabela cliente

![image](https://github.com/user-attachments/assets/7750bc6f-fa62-4779-a5fc-84ed36692a60)

<br>

Coloque a opção "Authorization" e o Token gerado no login anterior.

<b>Passo 1.4:</b> Atualizando o registro de Pedro para Fagner

![image](https://github.com/user-attachments/assets/12c9fbc5-5336-4494-8564-a94e766f5222)

<br>

Registro atual

<br>

![image](https://github.com/user-attachments/assets/f853a8f4-d445-4627-a247-e32078f2b2f1)

<br>

Mudando nome e email

<br>

![image](https://github.com/user-attachments/assets/4b2318ae-76d5-497e-9026-52282c654a71)

<br>

Registro alterado para os do Fagner

<b>Passo 1.5:</b> Transformando Fagner em um cliente "INATIVO"

![image](https://github.com/user-attachments/assets/84308cfe-f08a-472b-834b-47daa598d1a3)

<br>

Ao Deletarmos o registro 4 que é o do Fagner por boas praticas não o retiramos, mas mudamos seu Status

<br>

![image](https://github.com/user-attachments/assets/3e3e1f80-19a7-41b0-a866-c49cb27c764b)

<br>

Fagner esta inativo em nosso banco de dados conforme teste
<br>
<h3>CRUD de Livro</h3>
<br>
<b>Passo 2.1:</b> Criando um novo livro

![image](https://github.com/user-attachments/assets/6e0289de-5437-4f6e-b25a-db6a426990dd)

<br>

Para criação de um novo livro é necessario colocar um ID de um cliente no exemplo colocamos o ID 3 do cliente Gabriel. OPS o cliente não pode estar INAPITO no caso Fagner não funcionaria

<br>

![image](https://github.com/user-attachments/assets/1c3ef549-3fdd-49e7-bff6-b5a6c920ecd9)

<br>

Novo livro criado

<b>Passo 2.2:</b> Atualizando Livro

<br>

![image](https://github.com/user-attachments/assets/3c5ce248-7040-42d7-ac46-52956372c76b)

<br>

No exemplo acima atualizamos o Livro de id 4 "Kotlin com spring" para "Fundamento estag itau" e o preço para R$100

<br>

![image](https://github.com/user-attachments/assets/aacdff29-761f-466e-a6a9-18e283721d28)

<br>

Registro atualizado conforme

<b>Passo 2.3:</b> Mudando o status do livro para cancelado

<br>

![image](https://github.com/user-attachments/assets/b72128ee-ad05-451f-8162-17009194f143)

<br>

Deletando o livro de id 4 do banco por motivos de boas praticas igual o de clientes mantemos o registro apenas mudamos o status para "cancelado".

<br>

![image](https://github.com/user-attachments/assets/dceb1a9a-a3fc-412a-8742-75fc2871a796)

<br>

Livro de id 4 com status cancelado conforme


























