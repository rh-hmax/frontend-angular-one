# CRUD Frontend integrado à API

## História
Temos uma API para uma loja genérica e precisamos de um Frontend que nos permita interagir com esta API, conforme os requisitos abaixo:

### Requisitos funcionais
	1. Como GERENTE gostaria de INCLUIR um novo produto ao catálogo da loja
	2. Como GERENTE gostaria de ALTERAR um produto existente no catálogo
	3. Como GERENTE gostaria de REMOVER o produto do meu catálogo da loja
	4. Como GERENTE gostaria de LISTAR produtos cadastrados
	5. Como GERENTE gostaria de BUSCAR produtos pela sua DESCRIÇÃO
 	6. Como GERENTE gostaira que os resultados da LISTA fossem PAGINADOS
  	7. Como CLIENTE gostaria de VISUALIZAR a LISTA de produtos cadastrados

### Regras de negócio
	- Só USUÁRIOS AUTENTICADOS podem acessar o sistema
	- Só um GERENTE pode ter acesso para INCLUIR, ALTERAR ou REMOVER produtos 	

### Requisitos não funcionais
	- Precisa ser desenvolvido em Angular
 	- Precisa utilizar Tailwind para estilização
 	- Views (telas) devem ser componentes

### Entrega
	- O projeto deve ser entregue em um repositório GitHub
	- O link do repositório deve ser enviado para `desenvolvimento@hmax.com.br`
	- O Readme deve ter as instruções e comando para rodar o projeto e não depender de plugins da IDE para sua excecução.
	- O ambiente da aplicação precisa estar rodando e funcionando
	
### Critérios de avaliação
	- Entendimento dos requisitos
	- Afinidade com a ferramenta utilizada
	- Organização de arquivos e pastas
 	- Nomenclatura de métodos
	- Padrão e clareza de escrita do código

# Sobre a API
Se você está realizando este desafio, deve receber o `endpoint` da API assim como os exemplos das requisições em um arquivo json que você poderá importar para seu Insomnia se desejar.

### Token
Todas as requisições devem ter a tag `token` no header contendo o token que você deve receber por email ou mensagem no slack ou whatsapp, ou a API retornará `Invalid token`.

### Objeto Product

```
{
	"id": "646e18655527cf4595ea378a",
	"name": "Guaraná Antartica",
	"unit": "Lata",
	"price": 3.55,
	"active": true
}
```

Detalhes do objeto **PRODUCT**

| Campo | Tipo | Descrição |
|---|---|---|
| id | string | Código do produto |
| name | string | Nome/Descrição do produto |
| unit | string | Unidade do produto. Ex.: Lata, Caixa, Unidade, etc |
| price | number | Preço de venda do produto |
| active | boolean | Define se o produto está ativo |

**Atenção!** O id dos objetos virá no Response, mas não devem ser informados no Body das requisições. Em vez disso, no caso de alteração ou deleção, o id deve ser enviado na url logo após o nome do recurso, conforme padrões RESTFul. Ex.:
`https://.../products/646e18655527cf4595ea378a`

### Objeto User

```
{
	"id": "646e18655527cf4595ea378a",
	"name": "Winston Churchill",
	"login": "winston@teste.com",
	"password": "789456",
	"rules": ["MANAGER", "BASIC"],
	"active": true
}
```

Detalhes do objeto **USER**

| Campo | Tipo | Descrição |
|---|---|---|
| id | string | Código do usuário |
| name | string | Nome do usuário |
| login | string | Email utilizado para login |
| password | string | Senha do usuário (descriptografada) |
| rules | array de string | Papéis do usuário que definem suas permissões |
| active | boolean | Define se o produto está ativo |
