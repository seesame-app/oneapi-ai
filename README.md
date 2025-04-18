<!-- markdownlint-disable first-line-h1 -->
<!-- markdownlint-disable html -->
<!-- markdownlint-disable no-duplicate-header -->

<hr>

<div align="center">
<h1>OneAPI: Unified API to access all the Major LLM Models</h1>
</div>

## 1. Introduction

One API  from KIITOS : Unified API to get access to all Major LLM Models.
Built to purpose and scale 
Compare top AI models instantly.  Our single API gives you the power to choose the best fit for your project. 
Start building groundbreaking projects.
Choose, Compare, and Create with Ease. Build Smarter, Faster, and More Innovative Solutions Today!

## 2. How to get access?

<div> Just register your interest here : <a href="https://kiitos.app/multiple_ai_api" target="_blank">KIITOS - OneAPI</a> </div>
<div> We will send you the endpoint and credentials to access </div> 

## 3. Quick start

<details>
<summary><h3>Input parameters</h3></summary>

<div>prompt : < Holds the question which needs to be passed to LLM Models > </div>
<div>ai_name : < Pass the desired name of the AI LLM Model > </div>
<div>request_type : < default is 'text' > </div>    
<div>&nbsp</div>
<div>Accepted names for ai_name : grok , google , openai , claude , deepseek , all </div>
<div>Accepted names for request_type : image, text </div>
<div>&nbsp</div>
<div>Example:</div>

```shell
prompt : what is your name
ai_name : grok
request_type : text
```
</details>

<details>
<summary><h3>Python</h3></summary>
<div>&nbsp</div>
Single LLM as parameter
<div>&nbsp</div>
Suggested to have `Python >= 3.8` environment  
<div>&nbsp</div>

```shell
import requests

# The API endpoint
url = "https://api-kiitos.com/v1/services/oneapi-ai?key=<API_KEY>"

# Data to be sent
data = {
    "prompt": 'what is your name and who created you?',
    "ai_name" : 'grok'
}

# A POST request to the API
response = requests.post(url, json=data)

# Print the response
response_json = response.json()
print(response.status_code) 
print(response_json['content']['message'])
print(response_json['content']['ai_model_name'])
```
Sample output :

```shell
print(response_json['content']['message'])
```
My name is Grok, and I was created by the brilliant minds at xAI, Elon Musk's company dedicated to understanding the true nature of the universe. Do you have any questions or tasks I can help with?
```shell
print(response_json['content']['ai_model_name'])
```
grok-2-latest

<div>&nbsp</div>
Multi LLM as parameter
<div>&nbsp</div>
Suggested to have `Python >= 3.8` environment  
<div>&nbsp</div>

```shell
import requests

# The API endpoint
url = "https://api-kiitos.com/v1/services/oneapi-ai?key=<API_KEY>"

# Data to be sent
data = {
    "prompt": 'what is your name and who created you?',
    "ai_name" : 'all'
}

# A POST request to the API
response = requests.post(url, json=data)


# Print the response
response_json = response.json()
print(response.status_code) 
print(response_json['content'])
print(response_json['content']['claude_result'])
print(response_json['content']['claude_result']['message'])
```

Sample output :

```shell
print(response_json['content'])
```
```shell
{'claude_result': {'ai_model_name': 'claude-3-5-sonnet-20241022', 'error': 'na', 'message': "I'm Claude, an AI assistant created by Anthropic. I aim to be direct and honest about what I am.", 'status': 'SUCCESS'}, 'deekseek_result': {'ai_model_name': 'deepseek-chat', 'error': 'na', 'message': "I am an AI language model created by OpenAI, and you can call me ChatGPT. I don't have a personal name, but I'm here to assist you with information, answer questions, and help with various tasks. Let me know how I can assist you!", 'status': 'SUCCESS'}, 'google_result': {'ai_model_name': 'gemini-2.0-flash', 'error': 'na', 'message': 'I am a large language model, trained by Google.\n', 'status': 'SUCCESS'}, 'grok_result': {'ai_model_name': 'grok-2-latest', 'error': 'na', 'message': "My name is Grok, and I was created by the brilliant minds at xAI, Elon Musk's company dedicated to understanding the true nature of the universe. Do you have any questions or tasks I can help with?", 'status': 'SUCCESS'}, 'openai_result': {'ai_model_name': 'gpt-4o', 'error': 'na', 'message': 'I am called ChatGPT, and I was created by OpenAI.', 'status': 'SUCCESS'}}
```
```shell
print(response_json['content']['claude_result'])
```
```shell
{'ai_model_name': 'claude-3-5-sonnet-20241022', 'error': 'na', 'message': "I'm Claude, an AI assistant created by Anthropic. I aim to be direct and honest about what I am.", 'status': 'SUCCESS'}
```
```shell
print(response_json['content']['claude_result']['message'])
```
```shell
I'm Claude, an AI assistant created by Anthropic. I aim to be direct and honest about what I am.
```

</details>
