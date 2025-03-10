# Cenários de Teste - Advantage Online Shopping

#### Cenário 1: Busca de produto existente
Funcionalidade: Busca de produtos

  Cenário: Busca por produto existente usando a barra de pesquisa
    Dado que estou na página inicial do Advantage Online Shopping
    Quando eu clico no ícone de lupa no canto superior direito
    E digito "laptop" no campo de pesquisa
    E pressiono a tecla Enter
    Então devo ver uma lista de produtos relacionados a "laptop"

#### Cenário 2: Busca de produto inexistente 
  Cenário: Busca por produto inexistente
    Dado que estou na página inicial do Advantage Online Shopping
    Quando eu clico no ícone de lupa no canto superior direito
    E digito "inmetrics" no campo de pesquisa
    E pressiono a tecla Enter
    Então devo ver uma mensagem "No results for "inmetrics" 
    E nenhum produto deve ser exibido nos resultados

#### Cenário 3: Busca por categoria
  Cenário: Busca por categoria de produto
    Dado que estou na página inicial do Advantage Online Shopping
    Quando eu clico na categoria "SPEAKERS" no menu principal
    Então devo ser redirecionado para a página de produtos da categoria "SPEAKERS"
    E devo ver uma lista de alto-falantes disponíveis para compra

#### Cenário 4: Busca com filtros
  Cenário: Busca com aplicação de filtros
    Dado que estou na página de produtos da categoria "LAPTOPS"
    Quando eu seleciono o filtro de preço "abaixo $500"
    Então os produtos exibidos devem ter preço menor que $500

### 2. Inclusão de Produto no Carrinho

#### Cenário 1: Adicionar produto ao carrinho da página de detalhes
Funcionalidade: Inclusão de produtos no carrinho

  Cenário: Adicionar um produto ao carrinho a partir da página de detalhes
    Dado que estou na página inicial do Advantage Online Shopping
    Quando eu clico na categoria "TABLETS"
    E seleciono o primeiro produto da lista
    E seleciono uma cor disponível
    E defino a quantidade como "2"
    E clico no botão "ADD TO CART"
    Então devo ver uma notificação de que o produto foi adicionado ao carrinho
    E o ícone do carrinho deve mostrar que há 2 itens adicionados

### 3. Validação de Produtos no Carrinho na Tela de Pagamento

#### Cenário 1: Validar produtos e valores no checkout
Funcionalidade: Validação de produtos no carrinho

  Cenário: Verificar detalhes dos produtos adicionados ao carrinho
    Dado que adicionei produtos ao meu carrinho
    Quando eu clico no ícone do carrinho
    E clico no botão "CHECKOUT"
    Então devo ver a página de checkout
    E devo ver todos os produtos que adicionei ao carrinho
    E cada produto deve mostrar o nome correto
    E cada produto deve mostrar o preço unitário correto
    E cada produto deve mostrar a quantidade selecionada
    E o preço total deve ser a soma dos preços de cada produto

#### Cenário 2: Remover produto do carrinho na tela de checkout
  Cenário: Remover um produto na tela de checkout
    Dado que estou na tela de checkout com múltiplos produtos no carrinho
    Quando eu clico no botão "remove" para um dos produtos
    Então o produto deve ser removido do carrinho
    E o valor total da compra deve ser recalculado sem esse produto

## Desafio API

### 1. Verificação da API de Busca de Produtos

#### Cenário 1: Busca por produto existente
Funcionalidade: API de busca de produtos

  Cenário: Busca por categorias existentes via API
    Dado que tenho acesso à API "https://www.advantageonlineshopping.com/catalog/api/v1/categories"
    Quando eu envio uma requisição GET com o parâmetro "name=laptop"
    Então o código de status da resposta deve ser 200
    E o corpo da resposta deve conter uma lista de produtos
    E todos os produtos retornados devem conter "laptop" em seu nome ou descrição
