# Exploring Azure OpenAI

Azure OpenAI Service brings the generative AI models developed by OpenAI to the Azure platform, enabling you to develop AI solutions with the benefits provided by the Azure cloud platform.

## Before you start!
You will need an __Azure subscription that has been approved for access to the Azure OpenAI service__ for both text and code models, and DALL-E image generation models.
To request access to the Azure OpenAI service, visit https://aka.ms/oaiapply.

## Provision an Azure OpenAI resource
Before using Azure OpenAI models, you must provision an Azure OpenAI resource in your Azure subscription.

Sign into the Azure portal.
Create an Azure OpenAI resource with the following settings:

- Subscription: An Azure subscription that has been approved for access to the Azure OpenAI service.
- Resource group: Choose an existing resource group or create a new one with a name of your choice.
- Region: Choose any available region.
- Name: A unique name of your choice.
- Pricing tier: Standard S0

## Explore Azure OpenAI Studio
You can deploy, manage, and explore models in your Azure OpenAI Service by using __Azure OpenAI Studio__.
On the __Overview__ page for your Azure OpenAI resource, use the Explore button to open Azure OpenAI Studio in a new browser tab. Alternatively, navigate to Azure OpenAI Studio directly.

### Deploy a model for language generation
To experiment with natural language generation, you must first deploy a model.

1) On the Models page view the available models in your Azure OpenAI service instance.
2) Select any of the gpt-35-turbo models for which the Deployable status is __Yes__, and then select __Deploy__:
3) Create a new deployment with the following settings:
- Model: gpt-35-turbo
- Model version: Auto-update to default
- Deployment name: A unique name for your model deployment

## Use the Chat playground to work with the model
Now that you have deployed a model, you can use it in the __Chat playground__ to generate natural language output from prompts that you submit in a chat interface.

1) In Azure OpenAI Studio, navigate to the __Chat playground__ in the left pane. The Chat playground provides a chatbot interface with which you can interact with your deployed model
2) In the Configuration pane, ensure that __your model deployment is selected__.
3) In the Assistant setup pane, select the Default system message template, and view the system message this template creates. The system message defines how the model will behave in your chat session.
4) In the Chat session section, enter the following user message.

```
What is generative AI?
```

5) Observe the output returned by the model, which should provide a definition of generative AI.
6) Enter the following user message as a follow-up question:

```
What are three benefits it provides?
```

7) Review the output, noting that the chat session has kept track of the previous input and response to provide context (so it correctly interprets “it” as referring to “generative AI”) and that it provides a suitable response based on what was requested (it should return three benefits of generative AI).

## Use the DALL-E playground to generate images
In addition to language generation models, Azure OpenAI Service supports the DALL-E 2 model for image generation.

1) In Azure OpenAI Studio, navigate to the DALL-E playground in the left pane. Enter the following prompt:

```
 A blue hedgehog piloting an airplane
```

![sonicinairplane](C:\Users\Giovani\Downloads\56b31a20-3324-47b3-87f3-3c2933ed6cb1)

2) Select Generate and view the results, which should consist of an image based on the description you provided in the prompt.
3) Generate a second image by modifying the prompt to:

```
 A vintage microphone robot, digital art
```

![microrobot](C:\Users\Giovani\Downloads\faf07dab-a8fd-442d-bb33-34da9d1fc17d)

Verify that the new image matches the requirements of the prompt.



