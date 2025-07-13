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

<div> Get your Instant API Key here : <a href="https://kiitos.app/oneapi_ai" target="_blank">KIITOS - OneAPI</a> </div>

## 3. Quick start

<details>
<summary><h3>Input parameters</h3></summary>

<div>prompt : < Holds the question which needs to be passed to LLM Models > </div>
<div>ai_name : < Pass the desired name of the AI LLM Model > </div>
<div>request_type : < default is 'text' > </div>    
<div>&nbsp</div>
<div>TEXT LLM Models</div>
<div>Accepted names for ai_name : grok , google , openai , claude , deepseek </div>
<div>Accepted names for request_type : text </div>
<div>&nbsp</div>
<div>IMAGE LLM Models</div>
<div>Accepted names for ai_name : openai, grok , google-imagen </div>
<div>Accepted names for request_type : image </div>
<div>&nbsp</div>   
<div>Example:</div>

```shell
prompt : what is your name
ai_name : grok
request_type : text
```

```shell
prompt : cat and dog talking to each other
ai_name : grok
request_type : image
```

</details>

<details>
<summary><h3>Python - LLM Text Output </h3></summary>
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
print(response_json['content']['error'])
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

</details>
<details>
<summary><h3>Python - LLM Image Output</h3></summary>
<div>&nbsp</div>    
Suggested to have `Python >= 3.8` environment
<div>&nbsp</div>

    
```
    import requests
    # The API endpoint
    url = "https://api-kiitos.com/v1/services/oneapi-ai?key=<API_KEY>"
    
    # Data to be sent
    data = {
        "prompt": 'dog relaxing on a beach',
        "ai_name": 'grok',
        "request_type": 'image'
    }
    
    # A POST request to the API
    response = requests.post(url, json=data)
    
    # Print the response
    response_json = response.json()
    print(response.status_code) 
    print(response_json['content']['message'])
    print(response_json['content']['ai_model_name'])
    print(response_json['content']['error'])
```
Sample output :

```
print(response_json['content']['message'])
https://storage.googleapis.com/get-ai-images/ai_image_0df09366-b8e0-4bb4-af66-ed3de830d245-20250418183152128.jpeg
```
<p align="center">
  <img width="80%" src="https://storage.googleapis.com/get-ai-images/ai_image_0df09366-b8e0-4bb4-af66-ed3de830d245-20250418183152128.jpeg">
</p>

<div>&nbsp</div>
</details>

<details>
<summary><h3>Python - Generate AI Videos</h3></summary>
<div>&nbsp</div>    
Suggested to have `Python >= 3.8` environment
<div>&nbsp</div>
    
```
    import requests
    # The API endpoint
    url = "https://api-kiitos.com/v1/services/oneapi-ai?key=<API_KEY>"
    
    # Data to be sent
    data = {
        "prompt": 'ddragon flaying over a mountain landscape, cinematic, high quality, 4k resolution, epic fantasy scene, vibrant colors, detailed textures, dramatic lighting, wide shot, dynamic composition, majestic atmosphere, digital art style',
        "request_type": 'video'
        "ai_name" : 'google'
    }
    
    # A POST request to the API
    try:
        response = requests.post(url, json=data)
    except Exception as e:
        print('Error:', e)
        response = None
    
    # Print the response
    response_json = response.json()
    print(response.status_code) 
    print(response_json['content']['message'])
    print(response_json['content']['ai_model_name'])
    print(response_json['content']['error'])
    print(response_json['status'])
```
Sample output :

```
<Response [200]>
200
https://storage.googleapis.com/api_ai_videos/videos/video_file_afae154f-6262-49bb-af5e-25a0dd34d0a2-20250711172749001.mp4
veo-2
na
PROGRESS
```
Click to watch the video  :

[![Watch the video](https://github.com/seesame-app/oneapi-ai/blob/main/assets/Screenshot%202025-07-12%20013926.png)](https://storage.googleapis.com/api_ai_videos/videos/video_file_afae154f-6262-49bb-af5e-25a0dd34d0a2-20250711172749001.mp4)

<div>&nbsp</div>
</details>


<details>
<summary><h3>Python - Live search - WIP</h3></summary>
<div>&nbsp</div>    
Suggested to have `Python >= 3.8` environment
<div>&nbsp</div>



<div>&nbsp</div>
</details>
