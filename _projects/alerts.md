---
layout: default
order: 2
current: true
title: Emergency Alert Translation and Generation Using LLMs 
description: Design and implement a multilingual pipeline for emergency-alert translation and message generation, integrating commercial MT and LLM APIs (OpenAI/Azure OpenAI, Google Gemini, DeepSeek, Google Translate, DeepL). Develop an evaluation framework to determine whether outputs are safe and usable for time-critical alerts, including checks for clarity, fidelity, and potential risk flags. Collaborate with emergency management officials to identify communication gaps and pilot AI-assisted crisis messaging workflows in real operational settings. Invited talk and poster.
thumbnail: ../assets/images/people.jpg
---
<img src="../assets/images/paper_title.png" alt="Paper title" style="display:block; margin:0 auto; max-width:100%; height:auto; border:1px solid #ccc; padding:4px; box-sizing:border-box;">

Emergency alerts in the United States are an essential means of delivering important information in the case of a local or national emergency. These messages are sent in English, which means that millions of people are not receiving alerts in languages they can understand, putting their life and health at significant risk. In this paper, we examine the language and associated risk gaps with current emergency alert systems and evaluate solutions to improve reach. We assessed machine-generated translations of emergency messages using BLEU, COMET, BERTScore, and ROUGE to compare the performance of DeepSeek, Gemini, ChatGPT, and Google Translate. We find that overall Google Translate has the most reliable performance.
