---
title: Building a GenAI Chatbot on Google Cloud Platform

slug: building-a-chatbot-on-google-cloud-platform

description: Describes the steps of building a Chatbot agent on Google Cloud Platform with Vertex AI with RAG

keywords: chatbot, GenAI, GCP, RAG

page_purpose: Gives guidelines on how to build Generative AI chatbot with GCP Vertex AI

audience: developer

author: Shelly Han

content_owner: Poornima Sivanand

sort_order: 3
---

# Building a Chatbot on Google Cloud
Last updated: **June 4, 2024**

If you are looking for building a GenAI chatbot with on Retrieval-Augmented Generation (RAG) on Google Cloud Platform (GCP), here are some steps to get started!

## On this page

- **[Prerequisites](#prerequisites)**
- **[Preparation](#preparation)**
- **[Building the Agent](#building-the-agent)**
- **[Maintenance](#maintenance)**

## Prerequisites
1. First thing first, you need to request for a Public Cloud project set on GCP. Currently this has been disabled until further notice, you should be able to find updated information from the [Public Cloud website](https://digital.gov.bc.ca/cloud/services/public/). **Important**: Please make sure to discuss the usage with your MISO before starting! <!-- TODO: Add link to doc that talks about AI project prerequisites later on -->
1. We will be leveraging Agent Builder from GCP Vertex AI service for simple and quick setup. You can find out the [official Google doc](https://cloud.google.com/products/agent-builder?hl=en) as well. <!-- TODO: Shall we talk about pricing? -->

## Preparation
1. Identify the needs - There are twp types of agents you can create:
  - search: if you just have one central website, use search bot for quick and easy setup. Please note that the website needs to be public.
  - chat: if you are looking for a GenAI chatbot that offers conversational interaction, pick the `chat` type instead. You could also provide multiple data stores.
1. Identify your knowledge base for RAG. Those could be websites, html files, FAQs, PDF and Words documents, etc.
1. Now it's time to prepare the [Data Stores](https://cloud.google.com/dialogflow/vertex/docs/concept/data-store):
  - for a `search` agent, you just need to verify the public website domain for Google to be able to index it. [Here](https://cloud.google.com/generative-ai-app-builder/docs/domain-verification) are the detailed steps. If you are indexing a BCGov website, high chance you'll need to access RemedyApp for the change.
  - for a `chat` agent, you could create three data stores:
    - Website: exactly as how the `search` agent works by indexing a website
    - Unstructured documents: great for HTML exports, CSV and PDF files. Note that if the files have metadata, (i.e.: the actual URL for each HTML files), you can use a JSONL file to capture those information following [this post](https://cloud.google.com/dialogflow/vertex/docs/concept/data-store#with-metadata).
    - FAQ documents: typically expect for structured documents, in the formation of "question","answer","title","url". [More details here](https://cloud.google.com/dialogflow/vertex/docs/concept/data-store#structured).
  - You could also consider layout parsing (such as removing header and footer from the HTML files) and data chunking to improve the performance of the chatbot. [More reading](https://cloud.google.com/generative-ai-app-builder/docs/parse-chunk-documents).

## Building the Agent
1. For a `chat` agent, you can design how the chatbot interacts with clients from [DialogFlow CX](https://cloud.google.com/dialogflow?hl=en). Here are some useful settings you can config:
  - pick a LLM for the chatbot to use. This is part of the agent settings, as of today there are three models available:
    - text-bison@002
    - gemini-1.0-pro-001
    - gemini-1.5-flash-001 (preview)
  - select different data stores to use for knowledge base
  - design the flow:
    - define how the chatbot response in the situation with no user input or no match found. For example, direct to a human support if no answers found.
    - create prompt and template. For example, if you could just like the chatbot to provide URL instead of text for response.
    - condition based routes. For example, if there are multiple ares of different supports you'd like the chatbot to provide, it could route users to different context based on the keywords captured.
1. To test agent, you can initiate a simulator for quick testing within DialogFLow CX, where you can ask questions defined from the test plan and evaluate the result. <!-- TODO: Maybe some more information about testing? --> Afterwards, you can publish the agent for production usage.
1. When the agent is ready, it's time to integrate it to your system! There is a list of ready-to-go third party integrations available, such as Slack. But if you are looking to add the agent into your system, here are the some common methods:
  - To embed the conversation modal into a website: when publishing the agent, it comes with HTML code block that you can add to the website directly.
  - To use the API for the integration: refer to the [Agent Builder API doc](https://cloud.google.com/generative-ai-app-builder/docs/apis), there are client libraries ready for use as well!

## Maintenance
Now you have a chatbot working, let's talk about maintenance.
1. updating LLM: when there are newer and better LLMs available for the agent, you can make the switch directly from the agent settings. Changes are immediate, which can be tested right away.
1. updating data stores: if there are new contents that you'd like to include for the chatbot knowledge base, you can re-upload them to the data stores. If this happens frequently, you should consider automating the process from data collection to data upload. Leverage the [Agent Builder API](https://cloud.google.com/generative-ai-app-builder/docs/apis) for the automation task.
