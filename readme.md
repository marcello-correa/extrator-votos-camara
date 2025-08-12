# **Extrator de Votos da Câmara dos Deputados**

Uma aplicação web simples, de front-end, para buscar, visualizar e exportar em formato de planilha (XLSX) os registros de votos de qualquer votação da Câmara dos Deputados do Brasil.

Este projeto foi criado com o objetivo de facilitar o acesso e a análise de dados públicos, permitindo que qualquer cidadão possa, de forma rápida e intuitiva, transformar os dados brutos da API da Câmara em uma planilha organizada.

## **✨ Funcionalidades**

* **Busca de Votações por Data:** Encontre todas as votações ocorridas em um intervalo de datas específico.  
* **Atalho "Hoje":** Preenche automaticamente as datas para buscar as votações do dia atual.  
* **Resultados Paginados:** A lista de votações encontradas é dividida em páginas para uma navegação mais limpa.  
* **Extração de Votos por ID:** Visualize a lista completa de votos (deputado, tipo de voto, partido e UF) para uma votação específica.  
* **Interface Intuitiva:** Um fluxo de dois passos guia o usuário desde a busca da votação até a extração dos dados.  
* **Exportação para Excel:** Baixe os dados dos votos em um arquivo .xlsx com um único clique.

## **🚀 Como Usar**

A aplicação é dividida em dois passos simples:

### **Passo 1: Encontrar o ID da Votação**

1. Use os campos **"Data Início"** e **"Data Fim"** para definir o período que deseja pesquisar.  
2. Clique em **"Buscar"**. Uma lista de votações do período aparecerá abaixo.  
3. Navegue pela lista (usando os botões de paginação, se necessário) e encontre a votação de seu interesse.

### **Passo 2: Extrair e Baixar os Votos**

1. Na lista de resultados, clique no botão **"Usar ID"** ao lado da votação desejada. O ID será copiado automaticamente para o campo do Passo 2\.  
2. Clique em **"Buscar Votos"**. A tabela com o detalhamento dos votos de cada deputado será exibida.  
3. Para salvar os dados, clique em **"Baixar Planilha (XLSX)"**. O download do arquivo Excel começará imediatamente.

## **🛠️ Tecnologias Utilizadas**

Este é um projeto puramente front-end, construído com tecnologias web padrão para garantir simplicidade e performance.

* **HTML5**  
* **Tailwind CSS:** Para a estilização e criação de uma interface limpa e responsiva.  
* **JavaScript (Puro):** Para toda a lógica da aplicação, incluindo as chamadas à API e a manipulação dos dados.  
* **SheetJS (xlsx.js):** Biblioteca utilizada para criar e exportar os arquivos de planilha no formato Excel.

## **🌐 Publicação (Deploy)**

O projeto está publicado na **Vercel** e configurado para integração contínua. Qualquer alteração enviada para a branch main deste repositório aciona um novo deploy automaticamente.

A comunicação com a API da Câmara dos Deputados é feita através de um *rewrite* configurado no arquivo vercel.json para contornar as restrições de CORS.

## **📄 Fonte dos Dados**

Todos os dados são obtidos em tempo real através da [API de Dados Abertos da Câmara dos Deputados](https://dadosabertos.camara.leg.br/swagger/api.html).