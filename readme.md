# Testes Manuais - Advantage Online Shopping

Este repositório contém a documentação e as evidências dos testes manuais realizados no site [Advantage Online Shopping](https://advantageonlineshopping.com/), desenvolvidos como parte de um teste funcional.

## 📋 Sobre o Projeto

Os testes foram executados manualmente, seguindo cenários escritos em formato Gherkin. O projeto engloba testes de interface web e API, garantindo a qualidade das principais funcionalidades do site de e-commerce.

## 🎯 Objetivos dos Testes

- Validar a funcionalidade de busca de produtos
- Verificar o processo de adição de produtos ao carrinho
- Validar as informações exibidas na tela de checkout
- Testar as APIs de busca (originalmente de produtos, substituído por categorias devido a "internal error")

## 🛠️ Ferramentas Utilizadas

- **Navegador:** Google Chrome
- **Captura de Evidências:** GIF Recorder
- **Teste de API:** Postman
- **Documentação:** Formato Gherkin

## 📂 Estrutura do Repositório

```
TESTES-MANUAIS-INMETRICS/
│
├── evidencias/
│   ├── api/
│   │   └── teste-api.gif          # Evidência do teste de API
│   │
│   └── web/
│       ├── adicionar-carrinho.gif # Adição de produto ao carrinho
│       ├── busca-categoria.gif    # Busca por categoria
│       ├── busca-filtros.gif      # Busca com filtros
│       ├── busca-inexistente.gif  # Busca por produto inexistente
│       ├── busca-produto.gif      # Busca por produto existente
│       ├── checkout.gif           # Validação na tela de checkout
│       └── remover-produto.gif    # Remoção de produto do carrinho
│
└── plano-de-teste/
    └── cenarios-gherkin.md        # Cenários de teste em Gherkin
```

## 📝 Cenários de Teste

Os cenários de teste estão documentados em formato Gherkin no arquivo [cenarios-gherkin.md](./plano-de-teste/cenarios-gherkin.md), abrangendo:

### Testes Web
1. **Busca de produtos**
   - Busca por produto existente
   - Busca por produto inexistente
   - Busca por categoria
   - Busca com aplicação de filtros

2. **Gerenciamento do carrinho**
   - Adição de produto ao carrinho
   - Validação dos produtos no checkout
   - Remoção de produtos do carrinho

### Testes de API
- Consulta de categorias via API (alternativa utilizada devido ao erro 500 na API de busca de produtos)
- Validação do status code e formato da resposta

## 📊 Evidências

As evidências dos testes realizados estão disponíveis em formato GIF na pasta [evidencias](./evidencias/), organizadas por tipo de teste:

### Web
- **busca-produto.gif**: Demonstração da busca por produtos existentes
- **busca-inexistente.gif**: Demonstração da busca por produtos inexistentes
- **busca-categoria.gif**: Demonstração da navegação por categorias
- **busca-filtros.gif**: Demonstração da aplicação de filtros na busca
- **adicionar-carrinho.gif**: Demonstração do processo de adicionar produtos ao carrinho
- **checkout.gif**: Validação das informações na tela de checkout
- **remover-produto.gif**: Demonstração da remoção de produtos do carrinho

### API
- **teste-api.gif**: Demonstração do teste de API via Postman

## 📌 Observações

- Durante a execução dos testes de API, foi identificado que o endpoint original de busca de produtos (`/catalog/api/v1/products/search`) estava retornando erro 500 ("internal error"). Como alternativa, foi utilizada a API de categorias, conforme orientação do teste que solicitava o uso de URLs similares disponíveis na internet em caso de indisponibilidade.

## 🧪 Como Reproduzir os Testes

1. Acesse o site [Advantage Online Shopping](https://advantageonlineshopping.com/)
2. Siga os cenários descritos no arquivo [cenarios-gherkin.md](./plano-de-teste/cenarios-gherkin.md)
3. Para testes de API, utilize o Postman com os endpoints documentados

---

Teste realizado por Jardel Lima - 06/03/2025
