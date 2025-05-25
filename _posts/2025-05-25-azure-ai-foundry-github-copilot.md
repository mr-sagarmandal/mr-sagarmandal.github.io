---
layout: post
title:  "using azure ai foundry hosted models for github copilot"
date:   2025-05-25 00:15:00 -0700
categories: [azure, azure ai foundry, github, github copilot, copilot, azureaifoundry, openai, gpt4o, o3, vscode]
---

## Why bother
Why would we want to use Azure AI Foundry-hosted models as the base model for GitHub Copilot? There are a few good reasons.

Sometimes, we might hit the dreaded quota limit, which seems to apply even to enterprise GitHub Copilot subscriptions. Or maybe we are resource constrained and don’t want to pay for both Azure AI Foundry models and GitHub Copilot seats.

Another case: we might be working on a sensitive codebase and don’t want to share our code with whichever server Copilot uses for its default base models. This is pretty common in large organizations. Since Azure AI Foundry models keep data and prompts within the tenant, they make a perfect backing LLM.

## Steps
This took me some experimenting to get it to work. And did not find any official documentation for this. 

1) Install the Azure Extension in VS Code. And sign in and make sure you can see your subscriptions listed.
![aifoundryextension](/assets/images/posts/aifoundrygithubcopilot/aifoundryextension.png)

2) Open the Github Copilot (Ctrl + Alt + i) and click on `manage models` in the model selector dropdown.
![copilotmanagemodels](/assets/images/posts/aifoundrygithubcopilot/copilotmanagemodels.png)

3) Select Azure and write a model id that will be used to identify the model.
![selectazuremodelid](/assets/images/posts/aifoundrygithubcopilot/selectazuremodelid.png)

4) Get the AI Foundry model target uri and API key from AI Foundry and paste it.
![aifoundryapitoken](/assets/images/posts/aifoundrygithubcopilot/aifoundryapitoken.png)

After these steps the model is ready to be used. A pop up usually appears indicating the success/failure.
![success](/assets/images/posts/aifoundrygithubcopilot/success.png)

The model can then be selected from the model selector drop down.
![modelselectionaifoundry](/assets/images/posts/aifoundrygithubcopilot/modelselectionaifoundry.png)

And now, we can code away!

Note: These features are still a work in progress, and newer models may not be fully supported yet.