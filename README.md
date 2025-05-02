Abaixo o diagrama de alto nível da arquitetura:
![arquitetura_thera](https://github.com/user-attachments/assets/70ca7c14-bb55-4952-87af-7139fdbdc912)

Bronze (Raw)

Ingest raw data directly from APIs (e.g., currency pairs, commodities).

Write into Delta tables in Unity Catalog (raw schema).

Silver (Transformation)

Cleanse, validate, and enforce data typing.

Write into Delta tables in the silver schema.


Orchestration

Sequential jobs and dependencies managed via Databricks Workflows.

Scheduling, retries and alerting configured.

Governance

Unity Catalog for access control and data lineage.


git clone https://github.com/seu-usuario/seu-repo.git
cd seu-repo

Load and Configure the Architecture Diagram
Place the architecture.png file inside the docs/ folder.

Configure Databricks Workflows

Access your Databricks workspace.

Import the pipeline definition from workflows/pipeline_workflow.json.

Adjust any environment variables (URLs, credentials) as needed.

Run the Jobs

In Databricks Workflows, trigger manually or schedule.

Monitor job status, logs and outputs.

References

Databricks Delta Lake

Unity Catalog

Databricks Workflows
