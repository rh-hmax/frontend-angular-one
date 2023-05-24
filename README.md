# CRUD Frontend integrado à API

## História
Temos uma API para uma loja genérica e precisamos de um frontend que nos permita fazer o CRUD utilizando esta API, conforme os requisitos abaixo:

### Requisitos funcionais
	- Como gerente gostaria de incluir um novo produto ao catálogo da loja
	- Como gerente gostaria de alterar um produto existente no catálogo
	- Como gerente gostaria de remover o produto do meu catálogo da loja
	- Como gerente gostaria de recuperar uma lista com os produtos disponíveis
	- Como gerente gostaria de buscar produtos pela sua descrição

### Requisitos não funcionais
	- O frontend precisa ser desenvolvido em Angular

### Entrega
	- O projeto deve ser entregue em um repositório GitHub
	- O link do repositório deve ser enviado para `desenvolvimento@hmax.com.br`
	- O Readme deve ter as instruções e comando para rodar o projeto
	- É esperado que o ambiente esteja rodando a aplicação
	
### Critérios de avaliação
	- Entendimento dos requisitos
	- Afinidade com a ferramenta utilizada
	- Nomenclatura de métodos, arquivos e pastas
	- Padrão e clareza de escrita do código

# Sobre a API
Se você está realizando este desafio, deve receber o `endpoint` da API assim como os exemplos da requisição.

### Token
Cada requisição deve enviar a tag `token` no seu header contendo o token que você recebeu em seu email, ou a API retornará `Invalid token`.

### Objeto Product

Segue abaixo um exemplo do objeto completo que será usado nas requests e responses. 

**Atenção!** O id virá no Response, mas não deve ser informado no Body das requisições. Em vez disso, no caso de alteração ou deleção, o id deve ser enviado na url logo após o nome do recurso. Ex.:
`https://.../products/646e18655527cf4595ea378a`

```
{
	"id": "646e18655527cf4595ea378a",
	"name": "Sprite",
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