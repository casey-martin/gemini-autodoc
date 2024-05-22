# Question:

You will be given some unstructured documentation for an API. Your task is to structure the reference material. Give your response in JSON format that **adheres to the specification** given in the following table:

**JSON Specification**

| Field | Type | Description/Options |
|---|:---:|---|
| user_name | String | Name of User |
| api_name | String | Name of API (maximum 20 words) |
| api_call | String | One line of code that starts with the function call, followed by a full list of argument names and values |
| api_version | String | Version of API |
| api_arguments | JSON | JSON of all the restricted keywords in the arguments list. Document their types and whether they are required or not. Be descriptive yet concise. Imagine as if you are writing this for someone who has never used this API before, and they must complete a task with it using your documentation. If there are uncommon abbreviations, give the full term before abbreviating. |
| functionality | String | Short description of the function (maximum 20 words) |
| env_requirements | List[String] | List of all the library dependencies |
| example_code | String | A string containing example code to use the API |
| meta_data | JSON | A JSON file of containing additional information about the API |
| Questions | List[String] | Pretend you are a domain expert trying to solve a technical problem. Generate tasks, questions, and instructions (anywhere from 4 to 7) that would be resolved the returned values from this API. This set of diversely worded tasks (some issued as instructions, others as questions) should cover the API's parameter space. **DO NOT MENTION ANY API NAMES.** |

**Example Documentation**
Kubernetes Read Pod
Read
read the specified Pod

HTTP Request
GET /api/v1/namespaces/{namespace}/pods/{podName}

Path Parameters
Parameter	Description
podName	name of the Pod
namespace	object name and auth scope, such as for teams and projects
Query Parameters
Parameter	Description
pretty	If 'true', then the output is pretty printed. Defaults to 'false' unless the user-agent indicates a browser or command-line HTTP tool (curl and wget).
Response
Code	Description
200
Pod	OK

HTTP Request
GET /api/v1/namespaces/{namespace}/pods

Path Parameters
Parameter	Description



**Example Answer**.

```python
[
   {
    "user_name": "template_usrname",
    "api_name": "Kubernetes Read Pod",
    "api_call": "GET /api/v1/namespaces/{namespace}/pods/{podName}",
    "api_version": "1.0",
    "api_arguments": {
      "namespace": "string (The namespace where the Pod is located)",
      "podName": "string (The name of the Pod to read)"
    },
    "functionality": "Reads information about a specified Kubernetes Pod in REST format",
    "env_requirements": ["kubectl"],
    "example_code": "import requests\n\n# Read a Pod in a namespace\napi_url = 'https://your-kubernetes-api-server/api/v1/namespaces/your-namespace/pods/your-pod-name'\nheaders = {'Authorization': 'Bearer your-auth-token'}\nresponse = requests.get(api_url, headers=headers)\nprint(response.json())",
    "meta_data": {
      "description": "This API method allows users to read information about a specified Kubernetes Pod using RESTful API calls.",
      "documentation": "https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#get"
    },
    "questions": [
      "How can I retrieve information about a specific Pod?",
      "What method should I use to programmatically access Pod details?",
      "I need to make sure that all the of the load_balancing pods in the research_team namespace spun up correctly."
      "I'm having problems connecting to the dataEgress pods in Production. Are they okay?"
    ]
  }
]
```

**Documentation**
{API_DOC}

# Answer: