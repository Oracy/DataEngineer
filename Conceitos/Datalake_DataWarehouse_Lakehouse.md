### 1. **Data Warehouse (Armazém de Dados)**
Um **Data Warehouse** é um sistema centralizado que armazena dados estruturados de forma organizada, geralmente usados para relatórios e análises. O foco é em **alta performance** para consultas analíticas (OLAP).

- **Prós**:
  - Dados organizados e otimizados para consulta.
  - Alto desempenho em consultas complexas.
  - Confiabilidade e governança de dados.
  - Bom suporte a BI e ferramentas analíticas.
  
- **Contras**:
  - Estrutura rígida (dados devem ser limpos e transformados).
  - Custo elevado para armazenamento e processamento.
  - Não lida bem com dados não estruturados (ex: imagens, logs).
  
- **Exemplo**:
  - Um armazém de dados para uma empresa de varejo, contendo tabelas estruturadas sobre vendas, clientes, produtos, que são usadas para relatórios de desempenho.

### 2. **Data Lake**
Um **Data Lake** armazena dados em seu estado bruto, sejam eles estruturados, semi-estruturados ou não estruturados. A ideia é manter uma grande quantidade de dados de várias fontes em um só lugar, permitindo transformações posteriores conforme a necessidade.

- **Prós**:
  - Flexibilidade para armazenar todos os tipos de dados (estruturados e não estruturados).
  - Mais barato em termos de armazenamento, pois não exige processamento imediato.
  - Suporte a machine learning, big data, e análises exploratórias.
  
- **Contras**:
  - Dados podem virar “swamp” (lago pantanoso) se não forem organizados, dificultando a consulta.
  - Menor performance em consultas complexas comparado ao Data Warehouse.
  - Governança e controle de qualidade dos dados podem ser mais difíceis.

- **Exemplo**:
  - Uma empresa de mídia armazena vídeos, logs de acesso e dados estruturados sobre seus usuários em um Data Lake para análise posterior por equipes de machine learning.

### 3. **Lakehouse**
O **Lakehouse** é um modelo híbrido que combina as vantagens do Data Warehouse e do Data Lake. Ele permite armazenar dados não estruturados como um Data Lake, mas também oferece suporte a consultas estruturadas e desempenho similar ao de um Data Warehouse.

- **Prós**:
  - Combina a flexibilidade do Data Lake com a performance do Data Warehouse.
  - Suporte para análises em dados brutos e organizados em um único sistema.
  - Reduz a duplicação de dados entre o Data Lake e o Data Warehouse.
  
- **Contras**:
  - Modelo mais novo, ainda amadurecendo em termos de ferramentas e melhores práticas.
  - Pode ser mais complexo de gerenciar que um Data Warehouse tradicional.
  
- **Exemplo**:
  - Uma empresa de e-commerce usa um Lakehouse para armazenar logs de navegação de usuários, junto com dados de vendas e inventário, permitindo consultas eficientes tanto de dados estruturados quanto não estruturados.

### Comparação Final:
- **Data Warehouse** é ideal para dados altamente organizados e análises rápidas.
- **Data Lake** é ótimo para armazenar grandes volumes de dados brutos e análises exploratórias.
- **Lakehouse** oferece uma abordagem equilibrada, permitindo a flexibilidade do Data Lake com a performance analítica do Data Warehouse.