# API Auto Documentation
This repository uses Gemini 1.5 Flash to convert documentation about NCBI's EUtils API into structured JSON that is compliant with [API Zoo](https://github.com/ShishirPatil/gorilla/tree/main/data) JSON format.

In order to run this code, you will need an API key to access Gemini. Google provides [free API access](https://ai.google.dev/gemini-api/docs/get-started/tutorial?lang=python#setup_your_api_key) to Gemini 1.5 Flash at a rate of 15 Requests Per Minute, 1 million Tokens Per Minute, and 1,500 Requests Per Day.

## To Do:
  - Augment first pass of instructions with multihop data from NCBI tutorials.
  - Increase complexity of instructions ala WizardLM and MagicCoder. 