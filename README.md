# Meta-Llama-3.2

This repository contains project and use cases based on usage and application of Meta's LLM - Llama 3.2.

## Llama 3.2
Llama is Meta's Open Source Large Langauge Model for performing Generative AI tasks and build Gen AI Applications. The Llama 3.2 is the latest model version that incorporates the following features:

-   Open-source
-   _Lightweight text only_
-   _Multimodal_
-   _Multilingual_

The two largest models of the Llama 3.2 collection, 11B and 90B, support image reasoning use cases, such as document-level understanding including charts and graphs, captioning of images, and visual grounding tasks such as directionally pinpointing objects in images based on natural language descriptions. The 11B and 90B models can also bridge the gap between vision and language by extracting details from an image, understanding the scene, and then crafting a sentence or two that could be used as an image caption to help tell the story.

The lightweight 1B and 3B models are highly capable with multilingual text generation and tool calling abilities. These models empower developers to build personalized, on-device agentic applications with strong privacy where data never leaves the device.

Source:  [https://ai.meta.com/blog/llama-3-2-connect-2024-vision-edge-mobile-devices/](https://ai.meta.com/blog/llama-3-2-connect-2024-vision-edge-mobile-devices/)

### Models

Llama 3.2 is a collection of 8 large language models (LLMs):

#### Pretrained & Instruct Models:

1.  `llama-3.2-1b`  (text only) - Lightweight, most cost-efficient pretrained 1 billion parameter model, you can run anywhere on mobile and on edge devices.
2.  `llama-3.2-3b`  (text only) - Lightweight, cost-efficient pretrained 3 billion parameter model, you can run anywhere on mobile and on edge devices.
3.  `llama-3.2-11b`  (text+image input; text output) - multimodal pretrained 11 billion parameter model
4.  `llama-3.2-90b`  (text+image input; text output) - multimodal pretrained 90 billion parameter model

#### Latest release - October 24th

We released quantized  `1B`  and  `3B`  models.

[Model Card](https://github.com/meta-llama/llama-models/blob/main/models/llama3_2/MODEL_CARD.md#instruction-tuned-models)

1.  `llama-3.2-1b-QLORA_INT4_EO8`
2.  `llama-3.2-3b-QLORA_INT4_EO8`
3.  `llama-3.2-1b-SpinQuant_INT4_EO8`
4.  `llama-3.2-3b-SpinQuant_INT4_EO8`

This project was part of the Meta hands-on workshop conducted by Varun Vonmitta at ODSC 2024. LLM model: -Llama 3.2 The project uses Together.AI hosted API to use Llama 3.2.

 

## **Cooking Assitant using Llama 3.2 Python Notebook**

 
This source code module illustrates the use case of building a multimodal Generative AI application using Llama 3.2 The use case involves providing the LLM with an input image of a grocery basket with some ingredients requried for cooking a meal. Using chain of thought and prompt engineering, the model is made to generate a meal plan based on the ingredients in the image, identify missing items needed for the meal plan, count calories of the meal and finally generate recipes based on the ingredients. The project demonstrates MULTIMODALITY in LLAMA 3.2 with providing image and text as inputs, as well as illustrates chain of thought and effective prompt engineering to build generative AI applications.

## **Multimodal use cases using Llama 3.2 Python Notebook**

This source code module is the original notebook from the ODSC hands-on workshop by Varun Vontimitta. illustrates other usecases to use Multimodal LLama 3.2 Model.

 - **Image Captioning**
Describe an image or asking questions about an image.

 - **Plant Identification**
Perform advanced specialized plant recognition and care instruction generation. 

 - **Scene Understanding & Travel Plan Recommendation**
Comprehend the context, objects and activities within an image and get recommendations for where we can get the same experience depicted in the picture Llama 3.2 recognizes the objects in the scene and counts number of objects in the picture.

 - **OCR and Question Answering**
Extract the textual info from scanned documents or images which contain text.

 - **Tool Calling**
Meta Llama 3.2 can perform a web search by calling appropriate tools when the question prompt base don input image is out of the scope of trained data limits. Prompt the model to reason about the image and then prompt it separately to make the tool call. The use case demonstrated here is -  "Validate if hot air balloon festival really happens in Albuquerque in October" with an image of hot air balloon festival, you need to get the model to get the event name, venue and date and then prompt it again for tool calling response. To answer the user's question, Llama 3.2 uses in built brave search tool to find the answer for the input prompt.

**Llama Stack**
The notebook also provides an overview on Llama Stack. Llama Stack defines and standardizes the components required for building agentic, retrieval-augmented generation (RAG), and conversational Llama apps with system level safety framework. The notebook illustrates Llama Stack Inference, Llama Stack Agent, Llama Stack Safety and Calling Llama 3.2 vision model using LlamaStack.  