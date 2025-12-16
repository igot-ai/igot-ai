# Collection

<figure><img src="../.gitbook/assets/Screenshot 2025-12-10 at 13.18.36.png" alt=""><figcaption></figcaption></figure>

### Key concepts

Within each Project, Collections act as containers for related data. If you're familiar with databases, a Collection works like a **Table in SQL**. If you think in terms of file systems, it's similar to a **Folder in your operating system**.

Every file or record you upload into a Collection becomes an **Asset**—a single unit of data ready for processing, analysis, and knowledge extraction.

***

#### Collection Modes

Each Collection operates in one of two modes, depending on how you want to use the data:

| Mode      | Purpose                                         | Knowledge Graph |
| --------- | ----------------------------------------------- | --------------- |
| **Table** | Structured data storage with custom columns     | Not supported   |
| **Agent** | Structured storage + builds shareable knowledge | Supported       |

**Table Mode**

Data is stored directly in a SQL database. You define as many columns as needed to capture the specific information you care about. Best for structured records where you need fast queries but don't require AI-driven knowledge sharing.

**Agent Mode**

Includes everything Table mode offers, plus one critical addition: the Collection builds a **private knowledge graph**. This knowledge can be shared with other Collections, allowing AI agents to connect insights across your organization.

Use Agent mode when your data contains domain expertise that other teams or processes should access.

***

#### Columns

Columns define what information you want to capture from each Asset in your Collection. When raw data enters DATALOG, columns determine how that data gets structured and what insights get extracted.

There are **7 column types** divided into two categories:

***

**Primitive Types (Extracted from Raw Data)**

These columns capture information directly from your uploaded files and records.

| Type       | Description                            | Example                           |
| ---------- | -------------------------------------- | --------------------------------- |
| **Date**   | Timestamps, deadlines, effective dates | Invoice date, contract expiry     |
| **Number** | Quantities, amounts, measurements      | Total amount, quantity ordered    |
| **Text**   | Names, descriptions, categories        | Vendor name, product description  |
| **Table**  | Nested tabular data within a document  | Line items in an invoice          |
| **JSON**   | Structured data objects                | API responses, configuration data |

***

**Advanced Types (System-Enhanced)**

These columns go beyond extraction—they add intelligence and automation to your data.

| Type       | Description                                                                                | Example                                                |
| ---------- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------ |
| **Static** | Fixed values set manually by users or via API                                              | Status flags, manual classifications, department codes |
| **Agent**  | Delegates another AI Agent to review each Asset and populate the column with analyzed data | Risk assessment, sentiment analysis, compliance check  |

**Agent columns are powerful.** Instead of manually reviewing thousands of documents, you assign a specialized Agent to analyze each Asset and fill in the column automatically. For example, an Agent could read every contract and populate a "Risk Level" column with High, Medium, or Low based on your custom criteria.



### Agent Knowledge (RAG) <a href="#agent-knowledge-rag" id="agent-knowledge-rag"></a>

Assume your organization has a very high frequency update based on Product and Merchant policy.

<figure><img src="../.gitbook/assets/Screenshot 2025-12-16 at 13.10.37.png" alt=""><figcaption></figcaption></figure>
