# API Auto Documentation
This repository uses Gemini 1.5 Flash to convert documentation about NCBI's EUtils API into structured JSON that is compliant with [API Zoo](https://github.com/ShishirPatil/gorilla/tree/main/data) JSON format. In addition, it generates a list of queries that would require invoking the API to solve. 

In order to run this code, you will need an API key to access Gemini. Google provides [free API access](https://ai.google.dev/gemini-api/docs/get-started/tutorial?lang=python#setup_your_api_key) to Gemini 1.5 Flash at a rate of 15 Requests Per Minute, 1 million Tokens Per Minute, and 1,500 Requests Per Day. After creating a gemini API key, save it within a `.env` file as `GEMINI_API_KEY`.

```
GEMINI_API_KEY=your_super_secret_key_goes_here
```
## Draft Workflow
```mermaid
graph LR;
  raw_text["Raw Text"] --> table_context["Table Context"];
  table_context --> md["Markdown"];
  md --> json["JSON"];
  md --> api_examples["API Examples"];
  md --> verbalized_query["Verbalized Query"];
  verbalized_query --> complex_queries["Complex Queries"];
  api_examples --> bio_entrez_examples["BioEntrez Examples"];
  api_examples --> complex_api_examples["Complex API Examples"];
```


## To Do:
  - Augment first pass of instructions with multihop data from NCBI tutorials.
  - Increase complexity and diversity of instructions a la WizardLM and MagicCoder. 
  - Get documentation for all of BioPython
