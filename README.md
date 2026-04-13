<div align="center">
  <h1>Cardápio Digital - Tobias Lanches</h1>
  <p><b>Solução para gestão de produtos e integração de pedidos via WhatsApp</b></p>
  <br>
  <a href="https://vercel.app">
    <b>VISUALIZAR PROJETO ONLINE</b>
  </a>
</div>


## **Sobre o Projeto**
Criei este projeto com um objetivo bem claro: resolver a confusão dos pedidos por WhatsApp. Eu queria algo que fosse além de um PDF estático, uma ferramenta onde o cliente pudesse navegar com facilidade e que me desse a liberdade de alterar um preço ou trocar a descrição de um lanche sem precisar mexer em uma única linha de código.

## Por que construí isso?
Muitos **quiosques e lanchonetes** perdem vendas ou demoram a atender porque o processo é manual demais. Minha ideia foi centralizar tudo em uma interface web simples e rápida que já envia o pedido pronto para o atendente. O foco aqui é a experiência de quem está com fome: abrir o link, escolher o que quer e finalizar o pedido sem complicação.

## Funcionalidades Principais
<table width="100%">
  <tr>
    <td width="30%"><b>Integração WhatsApp</b></td>
    <td>Converte a seleção do cliente em uma mensagem formatada enviada diretamente para o quiosque.</td>
  </tr>
  <tr>
    <td width="30%"><b>Categorização</b></td>
    <td>Produtos organizados de forma lógica entre lanches, bebidas e adicionais.</td>
  </tr>
  <tr>
    <td width="30%"><b>Gestão Administrativa</b></td>
    <td>Painel exclusivo para cadastrar, editar ou remover itens sem alterar o código.</td>
  </tr>
  <tr>
    <td width="30%"><b>Atualização Dinâmica</b></td>
    <td>Todos os nomes, descrições e preços são consumidos em tempo real via API do Supabase.</td>
  </tr>
  <tr>
    <td width="30%"><b>Foco Mobile</b></td>
    <td>Interface totalmente responsiva e otimizada para smartphones dentro do estabelecimento.</td>
  </tr>
</table>

## Tecnologias Utilizadas
*   **Frontend:** HTML5, CSS3 e JavaScript Vanilla (ES6+).
*   **Backend e Banco de Dados:** Supabase (BaaS).
*   **Hospedagem:** Vercel.

## Configuração do Banco de Dados
Para o funcionamento correto da aplicação, é necessário configurar uma tabela chamada `produtos` no Supabase com a seguinte estrutura:

```sql
CREATE TABLE produtos (
  id int8 PRIMARY KEY GENERATED ALWAYS AS IDENTITY,
  nome TEXT NOT NULL,
  descricao TEXT,
  preco NUMERIC NOT NULL,
  categoria TEXT NOT NULL
);
