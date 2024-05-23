# Question:

You will be given some unstructured documentation for an API. Your task is to structure the reference material. Give your response in JSON format that **adheres to the specification** given in the following table:

**JSON Specification**

| Field | Type | Description/Options |
|---|:---:|---|
| user_name | String | Name of User |
| api_name | String | Name of API (maximum 20 words) |
| api_call | String | One line of code that starts with the function call, followed by a full list of argument names and values |
| api_version | String | Version of API |
| api_arguments | JSON | JSON of all the restricted keywords in the arguments list. Document their types and whether they are required or not. Be descriptive yet concise. Imagine as if you are writing this for someone who has never used this tool before, and they must complete a task with it using your documentation. If there are uncommon abbreviations, give the full term before abbreviating. |
| functionality | String | Short description of the function (maximum 20 words) |
| env_requirements | List[String] | List of all the library dependencies |
| example_code | String | A string containing example code to use the API |
| meta_data | JSON | A JSON file of containing additional information about the API |
| Questions | List[String] | Pretend you are a domain expert trying to solve a technical problem, but they are unaware that this API exists.. Generate tasks, questions, and instructions that this expert would give (anywhere from 3 to 6) that would be resolved the returned values from this API. This set of diversely worded tasks (some issued as instructions, others as questions) should cover the API's parameter space. **DO NOT MENTION THE TOOL NAME IN YOUR INSTRUCTION/QUESTION.** |

**Example Documentation**
ECitMatch
Base URL
https://eutils.ncbi.nlm.nih.gov/entrez/eutils/ecitmatch.cgi

Function
Retrieves PubMed IDs (PMIDs) that correspond to a set of input citation strings.

Required Parameters
db
Database to search. The only supported value is ‘pubmed’.

rettype
Retrieval type. The only supported value is ‘xml’.

bdata
Citation strings. Each input citation must be represented by a citation string in the following format:

journal_title|year|volume|first_page|author_name|your_key|

Multiple citation strings may be provided by separating the strings with a carriage return character (%0D). The your_key value is an arbitrary label provided by the user that may serve as a local identifier for the citation, and it will be included in the output. Be aware that all spaces must be replaced by ‘+’ symbols and that citation strings should end with a final vertical bar ‘|’.

https://eutils.ncbi.nlm.nih.gov/entrez/eutils/ecitmatch.cgi?db=pubmed&retmode=xml&bdata=proc+natl+acad+sci+u+s+a|1991|88|3248|mann+bj|Art1|%0Dscience|1987|235|182|palmenberg+ac|Art2|

**Example Sumbission**
```
  {
    "user_name": "ncbi_usrname",
    "api_name": "NCBI E-utilities ECitMatch",
    "api_call": "https://eutils.ncbi.nlm.nih.gov/entrez/eutils/ecitmatch.cgi?db=pubmed&retmode=xml&bdata=journal_title|year|volume|first_page|author_name|your_key|%0D...",
    "api_version": "N/A",
    "api_arguments": {
      "db": "string (The database to search. The only supported value is 'pubmed')",
      "rettype": "string (The retrieval type. The only supported value is 'xml')",
      "bdata": "string (Citation strings. Each input citation must be represented by a citation string in the following format: journal_title|year|volume|first_page|author_name|your_key|. Multiple citation strings may be provided by separating the strings with a carriage return character (%0D). The your_key value is an arbitrary label provided by the user that may serve as a local identifier for the citation, and it will be included in the output. Be aware that all spaces must be replaced by '+' symbols and that citation strings should end with a final vertical bar '|')"
    },
    "functionality": "Retrieves PubMed IDs (PMIDs) that correspond to a set of input citation strings.",
    "env_requirements": [],
    "example_code": "import requests\n\n# Example citation string\ncitation_string = 'proc+natl+acad+sci+u+s+a|1991|88|3248|mann+bj|Art1|'\n\n# Construct the API URL\napi_url = 'https://eutils.ncbi.nlm.nih.gov/entrez/eutils/ecitmatch.cgi?db=pubmed&retmode=xml&bdata=' + citation_string\n\n# Make the API request\nresponse = requests.get(api_url)\n\n# Print the response\nprint(response.text)",
    "meta_data": {
      "description": "The ECitMatch function retrieves PubMed IDs (PMIDs) that correspond to a set of input citation strings. It is a useful tool for researchers who need to find the PMIDs for a set of citations.",
      "documentation": "https://www.ncbi.nlm.nih.gov/books/NBK25499/"
    },
    "questions": [
      "I have a list of citations in a specific format. How can I automatically retrieve the corresponding PubMed IDs for these citations?",
      "I need to programmatically access PubMed IDs based on citation information. What API can I use for this purpose?",
      "Given a set of journal articles, how can I efficiently obtain their PubMed IDs using a web service?",
      "I'm working with a database of scientific publications and need to link them to their respective PubMed IDs. Is there a way to do this automatically?",
      "I have a list of citations in a specific format. How can I use a web service to retrieve the corresponding PubMed IDs?"
    ]
  }
```