---
layout: post
title:  "using azure ai foundry hosted models for github copilot (2026 update)"
date:   2026-05-18 00:00:00 -0700
categories: [azure, azure ai foundry, github, github copilot, copilot, azureaifoundry, openai, vscode]
---

> This is an update to the original post: [using azure ai foundry hosted models for github copilot](/2025/05/25/azure-ai-foundry-github-copilot.html)

## new way to do so through visual studio code
Since my post last year, Visual Studio Copilot Chat along with Github Copilot has changed considerably. The new way to connect Azure AI Foundry aka Microsoft Foundry model is more config driven. 

## steps 
1) Deploy a model in Microsoft Foundry. 
2) In the Copilot Chat pane click on the gear icon from the model select dropdown.
![copilotmanagemodels2026](/assets/images/posts/aifoundrygithubcopilot/copilotmanagemodels2026.png)
3) In the pop up window for language models, select `Add Models` and then from the dropdown select `Azure`.
![languagemodelswindow](/assets/images/posts/aifoundrygithubcopilot/languagemodelswindow.png)
4) Add the group name e.g., `Microsoft Foundry`.
![groupname](/assets/images/posts/aifoundrygithubcopilot/groupname.png)
5) Enter API key or leave empty to use Entra ID.
![tokenprompt](/assets/images/posts/aifoundrygithubcopilot/tokenprompt.png)
For this get the token from the Microsoft Foundry page if using token:
![aifoundryapitoken](/assets/images/posts/aifoundrygithubcopilot/aifoundryapitoken2.png)
6) Configure the model in the configuration json. Get the URL link to the model deployment from Microsoft Foundry. Keep the ID consistent with the model deployment. 
![configuremodel](/assets/images/posts/aifoundrygithubcopilot/configuremodel.png)