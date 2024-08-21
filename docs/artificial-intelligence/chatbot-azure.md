---
title: Building a GenAI Chatbot on Public Cloud Azure

slug: building-a-chatbot-on-public-cloud-azure

description: Describes the steps of building a Chatbot agent on Public Cloud Azure with OpenAI Studio

keywords: chatbot, GenAI, Azure, RAG, GPT

page_purpose: Gives guidelines on how to build Generative AI chatbot with Azure OpenAI Studio

audience: developer

author: Shelly Han

content_owner: Poornima Sivanand

sort_order: 3
---

# Building a Chatbot on Public Cloud Azure
Last updated: **Aug 14, 2024**

If you are looking for building a GenAI chatbot with on Retrieval-Augmented Generation (RAG) on Azure OpenAI Studio (AOAI), here are some steps to get started!

## On this page

- **[Prerequisites](#prerequisites)**
- **[Preparation](#preparation)**
- **[Building the Agent](#building-the-agent)**

## Prerequisites
1. First thing first, you need to request for a Public Cloud project set on Azure Landing Zone LIVE. You should be able to find more information from the [Public Cloud website](https://digital.gov.bc.ca/cloud/services/public/). **Important**: Please make sure to discuss the usage with your MISO before starting! <!-- TODO: Add link to doc that talks about AI project prerequisites later on -->
1. If you are going to use OpenAI in Azure, you do NOT need to accept additional T&C as the use of OpenAI is included in the standard Azure T&C that are covered by the enterprise agreement with Microsoft. However, there is a Code of Conduct that all Open AI users are implicitly agreeing to. Please check it out first before proceed! https://learn.microsoft.com/en-us/legal/cognitive-services/openai/code-of-conduct
1. We will be leveraging Azure OpenAI Studio (AOAI) for simple and quick setup. However, AOAI is not the only AI service available for building a chatbot on Azure, before you settle with AOAI, make sure to look at all the other options [here](https://ai.azure.com/)!
1. Check out about [pricing](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/openai-service/)

## Preparation
1. First you need to create an Azure OpenAI instance:
  - head over to Azure and select the corresponding subscription: https://portal.azure.com/#home
  - search for `Azure OpenAI`
  - click on "+ Create" and complete the form. *Note* that currently GPT models are only available in `Canada East` region!
1. make sure to install Azure CLI `az` as it's very useful. It's okay to start with the console and get familiar, but please note that the Azure AI services are evolving fast and the pages will be looking quite differently from time to time. It's always more reliable to use `az` in that case!
1. It's also a good idea to setup an budget alert so you are aware of the current usage as development goes, and the ability to prep for the project budget based on the forecast.

## Building the Agent
Azure has very good coverage from their documentation, we won't duplicate the same content over here. Now please go ahead and follow [this quick start guide](https://learn.microsoft.com/en-us/azure/ai-services/openai/use-your-data-quickstart) to build a chatbot using your own knowledge base!
