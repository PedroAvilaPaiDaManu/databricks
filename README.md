[![Architecture Diagram](docs/architecture.png)](docs/architecture.png)


Abaixo o diagrama de alto nível da arquitetura:



Bronze (Raw)

Ingestão de dados brutos diretamente das APIs (ex.: pares de moedas, commodities).

Escrita em tabelas Delta no Unity Catalog (raw schema).

Silver (Transformation)

Limpeza, validação e tipagem dos dados.

Escrita em tabelas Delta no schema silver.

Gold (Consumption)

Agregação e geração de views/tabelas analíticas.

Escrita em tabelas Delta no schema gold.

Orquestração

Jobs sequenciais e dependências gerenciadas pelo Databricks Workflows.

Agendamentos, retries e alertas configurados.

Governança

Unity Catalog para controle de acesso e linagem de dados.


git clone https://github.com/seu-usuario/seu-repo.git
cd seu-repo

2. Carregar e Configurar a Imagem de Arquitetura

Coloque o arquivo architecture.png dentro da pasta docs/.

3. Configurar Workflows no Databricks

Acesse o workspace Databricks.

Importe o pipeline definido em workflows/pipeline_workflow.json.

Ajuste variáveis de ambiente (URLs, credenciais).

4. Executar os Jobs

No Databricks Workflows, acione manualmente ou agende.

Monitore status, logs e resultados.

📚 Referências

Databricks Delta Lake

Unity Catalog

Databricks Workflows
