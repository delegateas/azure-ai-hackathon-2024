# AI Hackaton 2024
Here's some different challenges to pick between that all involves working with AI in the Microsoft eco-system. 

Several of the challenges are about RAG architectures, if you are new to that, you can read the a primer here https://learn.microsoft.com/en-us/azure/ai-studio/concepts/retrieval-augmented-generation 

There are many technical componants that can help you build a AI solutions. For the challenges just pick a single tool stack a stick with that otherwise you end up spending all time on comparing the different tools, and for a first time experience it is less important whether you use Azure AI search, Kusto, CosmosDB, or some other tool. Try to focus on getting to an end-to-end working solution. 

## How to
1. Pick a challenge (technology) that you want to work with
2. Get the sample working (feel free to pick a sample that you find interesting)
3. Turn the sample into something unique, try to solve something real (remember it is a hackaton it doesn't have to be perfect)
4. Prepare a short presentation, max 2-3 minutes, preferably make a few slides or a video, so we can show it to people not present 



## Open AI API Access  

For all the challenges you need access to either an OpenAI API key or an Azure OpenAI API key and a deployment name. If you have your own Azure OpenAI service use that. You can request access to Azure OpenAI on any Azure subscription here: https://aka.ms/oai/access (02/06/2024 it is still not enabled per default). 

If you don't have access you can use the shared one, but be mindful of how many API calls you make as we pay for them. 

_Note on deployments:_ please consult https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/models#model-summary-table-and-region-availability to check if a model is available in the region that you are working. E.g. GPT4o is only available in US regions currently. 

| Deployment name | Model | Endpoint | Secret |
| - | - | - | - |
| dggpt35-turbo-16k | gpt-35-turbo-16k (0613) | `https://dgopenai-us.openai.azure.com/` | Vault/Demo Environments/AzureOpenAI/us-key |
| gpt4functioncalling | gpt-4 (0613) | `https://dgopenai-us.openai.azure.com/` |Vault/Demo Environments/AzureOpenAI/us-key |
| text-embedding-ada-002 | text-embedding-ada-002 | `https://dgopenai-us.openai.azure.com/` | Vault/Demo Environments/AzureOpenAI/us-key |
| gpt4o | gpt-4o (2024-05-13) |  `https://dgopenai-us.openai.azure.com/` | Vault/Demo Environments/AzureOpenAI/us-key |
| Dalle3 | dall-e-3 (3.0) |  `https://dgopenai-us.openai.azure.com/` | Vault/Demo Environments/AzureOpenAI/us-key  |
| gpt35-turbo-instruct | gpt-35-turbo-instruct (0914) | `https://dgopenai-us.openai.azure.com/` | Vault/Demo Environments/AzureOpenAI/us-key  |
| text-embedding-ada-002 | text-embedding-ada-002 | `https://dgopenai.openai.azure.com/` | Vault/Demo Environments/AzureOpenAI/eu-key  |
| gpt-35-turbo | gpt-35-turbo | `https://dgopenai.openai.azure.com/` | Vault/Demo Environments/AzureOpenAI/eu-key |

dgopenai = west europe <br>
dgopenai-us = east us


## Challenges 

I have listed 4 different challenges you can pick from, but you are also free to create your own. They are listed from simplest to most advanced, however for all the challenges you should be able to get it up and running within the time we have today. 

## 1. Azure Open AI studio 
A UI based platform for getting into all the AI offerings Azure have. You can test and fine tune models directly from the browser. Good way to familiarize yourself, with scenarious and services Microsofts thinks AI is good for.  

Prerequisites: 
- Azure Subscription with access to Azure Open AI

Documentation: https://learn.microsoft.com/en-us/azure/ai-studio/

## 2. Open AI Azure Functions Bindings 

**Prerequisites:**
- Azure Functions CLI

**Examples:** <br>
https://github.com/Azure/azure-functions-openai-extension/tree/main/samples

**Readme:** <br>
https://learn.microsoft.com/en-us/azure/azure-functions/functions-bindings-openai?tabs=isolated-process&pivots=programming-language-csharp

**My pick:** <br>
RAG with Kusto: https://github.com/Azure/azure-functions-openai-extension/tree/main/samples/rag-kusto - Kusto is a powerful tool, that we should get more experience with, not just for AI. 

## 3. Kernel Memory
Kernel Memory (KM) is a multi-modal AI Service specialized in the efficient indexing of datasets through custom continuous data hybrid pipelines, with support for Retrieval Augmented Generation (RAG), synthetic memory, prompt engineering, and custom semantic memory processing.

KM is available as a Web Service, as a Docker container, a Plugin for ChatGPT/Copilot/Semantic Kernel, and as a .NET library for embedded applications.

**Examples:** <br>
https://github.com/microsoft/kernel-memory/tree/main/examples 
**Readme:**<br>
https://github.com/microsoft/kernel-memory 

**My pick:**<br>
Simple starter that shows you some of the configuration parameters (there's a lot) https://github.com/microsoft/kernel-memory/tree/main/examples/203-dotnet-using-core-nuget

## 4. LLaMa Sharp 
LLamaSharp is a cross-platform library to run 🦙LLaMA/LLaVA model (and others) on your local device. Based on llama.cpp, inference with LLamaSharp is efficient on both CPU and GPU. With the higher-level APIs and RAG support, it's convenient to deploy LLMs (Large Language Models) in your application with LLamaSharp.


**Documentation:**<br>
https://scisharp.github.io/LLamaSharp/0.12.0/QuickStart/ 

**Examples:**<br>
https://github.com/SciSharp/LLamaSharp/tree/master/LLama.Examples 

**My pick:**<br>
I got it up and running with a local LLM with a this setup: https://github.com/sjkp/sharpllama-example 

## 5. Create your own
If you none of the challenges above is spicy enough you are welcome to go completely off script. However the end goal is still that you have something demonstrable at the end of the day. 
