# Desafio-3-metodologias-ageis
Desafio III Metodologias Ágeis e Gerenciamento de Projetos do Hackathon 2024 da Santo Digital
# AdventureWorks Data Analysis Application

Este repositório contém a aplicação web de análise de dados desenvolvida para a empresa fictícia AdventureWorks. A aplicação permite que os stakeholders visualizem e interajam com os dados de vendas de maneira intuitiva e informativa.

## Índice
- [Visão Geral do Projeto](#visão-geral-do-projeto)
- [Decisões de Design e Tecnologias](#decisões-de-design-e-tecnologias)
- [Desenvolvimento da Solução](#desenvolvimento-da-solução)
- [Desafios e Soluções](#desafios-e-soluções)
- [Como Executar](#como-executar)
- [Contribuindo](#contribuindo)
- [Licença](#licença)

## Visão Geral do Projeto

A aplicação foi desenvolvida para atender aos seguintes requisitos de negócio:
1. **Visualização de Vendas Totais ao Longo do Tempo:** Com filtros avançados e granularidade ajustável.
2. **Produtos Mais Vendidos por Categoria:** Visualizações dinâmicas com métricas adicionais.
3. **Desempenho de Vendas por Vendedor:** KPIs e análise de funil de vendas.
4. **Vendas por Região:** Mapas interativos e previsões baseadas em machine learning.
5. **CRUD para Registros de Produtos:** Gestão robusta e auditada de produtos.

## Decisões de Design e Tecnologias

### 1. **Frontend:**
- **Framework Utilizado:** React foi escolhido pela sua capacidade de criar interfaces dinâmicas e interativas, o que é essencial para visualizações de dados complexas e responsivas.
- **Biblioteca de Visualização:** D3.js foi integrada ao React para renderizar gráficos interativos que suportam múltiplas formas de visualização (linhas, barras, mapas, etc.), o que permite uma análise detalhada e visualmente atraente dos dados.
- **Gerenciamento de Estado:** Utilizamos Redux para o gerenciamento de estado, garantindo que todos os componentes tenham acesso aos dados necessários de forma eficiente.

### 2. **Backend:**
- **Plataforma e Framework:** Node.js com Express foi selecionado para construir uma API RESTful que serve como intermediária entre o front-end e o banco de dados. Node.js é altamente performático e se integra bem com sistemas baseados em JavaScript, como o React.
- **Banco de Dados:** PostgreSQL foi escolhido pela sua robustez e capacidade de lidar com consultas complexas e análises de dados. Além disso, é compatível com JSON, o que facilita o armazenamento de estruturas de dados mais complexas.
- **Machine Learning:** Modelos de previsão de vendas e detecção de outliers foram implementados em Python, utilizando bibliotecas como scikit-learn e pandas, e executados através de serviços API no backend.

### 3. **DevOps e Infraestrutura:**
- **Contêineres:** Docker foi utilizado para containerizar a aplicação, garantindo que ela possa ser executada em qualquer ambiente de forma consistente. Docker Compose foi usado para orquestrar o frontend, backend e banco de dados.
- **CI/CD:** GitHub Actions foi configurado para realizar integração e entrega contínuas, executando testes automaticamente a cada novo push para o repositório.

## Desenvolvimento da Solução

O desenvolvimento foi organizado em sprints de duas semanas, seguindo a metodologia ágil, para garantir entregas frequentes e incrementais de funcionalidades. Abaixo, detalhamos como cada sprint foi executada:

### Sprint 1: Visualização de Vendas Totais e Exportação de Relatórios

- **Objetivo:** Implementar a visualização das vendas totais ao longo do tempo e permitir a exportação dos dados.
- **Tarefas Realizadas:**
  1. **API de Vendas Totais:** Desenvolvemos uma rota RESTful para buscar dados de vendas, com suporte a múltiplos filtros e granularidade (diária, semanal, mensal, etc.).
  2. **Detecção de Tendências e Anomalias:** Um modelo de machine learning foi treinado para identificar padrões de vendas e detectar outliers, utilizando séries temporais.
  3. **Frontend Interativo:** Criamos componentes de gráficos interativos em React usando D3.js, permitindo que o usuário aplique filtros e ajuste a granularidade dos dados.
  4. **Exportação de Dados:** Implementamos funcionalidades de exportação para CSV, Excel e PDF, e configuramos um serviço de agendamento de relatórios por email.

### Sprint 2: Produtos Mais Vendidos e Desempenho de Vendedores

- **Objetivo:** Desenvolver funcionalidades para visualizar os produtos mais vendidos e o desempenho de cada vendedor.
- **Tarefas Realizadas:**
  1. **API de Produtos Mais Vendidos:** Criamos endpoints para consultar produtos mais vendidos por categoria, com suporte a filtros avançados.
  2. **Dashboard de Vendas por Vendedor:** Desenvolvemos um dashboard que exibe KPIs de vendas por vendedor, utilizando gráficos comparativos.
  3. **Funil de Vendas:** Implementamos uma análise detalhada do funil de vendas, incluindo o tempo médio para conversão e identificação de gargalos.
  4. **Testes Automatizados:** Adicionamos testes unitários e de integração para garantir a qualidade das novas funcionalidades.

### Sprint 3: Vendas por Região e CRUD de Produtos

- **Objetivo:** Implementar visualizações de vendas por região e a funcionalidade de CRUD para registros de produtos.
- **Tarefas Realizadas:**
  1. **Mapas Interativos:** Desenvolvemos um mapa interativo utilizando D3.js para visualizar as vendas por região, incluindo previsões baseadas em algoritmos de machine learning.
  2. **Funcionalidade CRUD:** Criamos uma interface robusta para o gerenciamento de produtos, incluindo validações, controle de versão, importação em massa de dados e auditoria.
  3. **Previsões de Vendas:** Implementamos modelos de previsão de vendas utilizando dados históricos, integrados ao back-end para consultas em tempo real.
  4. **Configuração de Infraestrutura:** Ajustamos o ambiente de produção para suportar todas as novas funcionalidades, incluindo a configuração de balanceamento de carga e escalabilidade horizontal.

## Desafios e Soluções

1. **Desafio: Integração de Machine Learning ao Backend:**
   - **Solução:** Utilizamos APIs RESTful para expor modelos de machine learning treinados em Python. Isso permitiu que os modelos fossem executados de forma assíncrona, minimizando o impacto no desempenho do backend principal.

2. **Desafio: Performance de Visualizações Interativas:**
   - **Solução:** Optamos pelo uso de D3.js juntamente com React para renderização eficiente de gráficos complexos. Utilizamos técnicas de virtualização para lidar com grandes conjuntos de dados, garantindo que a aplicação permanecesse responsiva.

3. **Desafio: Manutenção de Coerência de Dados em Operações CRUD:**
   - **Solução:** Implementamos controle de versão e auditoria detalhada para todas as operações de CRUD, garantindo que qualquer alteração fosse registrada com informações sobre quem fez a mudança, quando e o que foi alterado.


