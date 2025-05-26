---
layout: post
title:  "using azure ai foundry hosted models in cline or roo code"
date:   2025-05-25 06:19:00 -0700
categories: [azure, azure ai foundry, vscode, copilot, azureaifoundry, openai, gpt4o, o3, agentic, aiagent, agent, cline, roo]
---

## why
Refer to [my last post](/_posts/2025-05-25-azure-ai-foundry-github-copilot.md#why-bother)

## steps
**Note:** The screenshots are all from cline. Since Roo is a fork of Cline, the UI and the steps are very similar to that of Cline's.

Two ways to do this:

### Use models integrated to Github Copilot 
1) Carry out the steps described to integrate AI Foundry models with Github Copilot described in [my last post](/_posts/2025-05-25-azure-ai-foundry-github-copilot.md#steps)

2) Use it in Cline by clicking settings and selecting VS Code LM API.
![clinecopilotmodel](/assets/images/posts/aifoundrymodelscline/clinecopilotmodel.png)

### Add the models directly to cline
1) Click settings in Cline, and select OpenAI Compatible from the dropdown.
![clineopenaicompatible](/assets/images/posts/aifoundrymodelscline/clineopenaicompatible.png)

2) Go to your AI Foundry deployment and fill out the information needed.
![clineaifoundrydata](/assets/images/posts/aifoundrymodelscline/clineaifoundrydata.png)

In both Roo and Cline, for the Base URL field the Target URI copied from AI Foundry needs to be modified, to make it adhere to this format:
<br>`https://<RESOURCE NAME>.openai.azure.com/openai/deployments/<DEPLOYMENT NAME>`<br>
e.g., for my deployment the Base URL I extracted from AI Foundry Target URI was as follows.<br><br>
Target URI: `https://<RESOURCE NAME>.openai.azure.com/openai/deployments/o4-mini/chat/completions?api-version=2025-01-01-preview`<br>
Base URL: `https://<RESOURCE NAME>.openai.azure.com/openai/deployments/o4-mini`<br>


After completion:
![itworks](/assets/images/posts/aifoundrymodelscline/itworks.png)

**Note:** These features are still a work in progress, and newer models may not be fully supported yet.