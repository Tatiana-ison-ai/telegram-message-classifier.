---
name: telegram-message-classifier
description: Classifies Telegram messages as questions, complaints, suggestions, or other messages. Use when asked to classify a message, identify its intent, categorize a Telegram message, or prepare a message category for a spreadsheet. Do not use when asked to write a reply, edit text, or create a social media post.
---

# Telegram Message Classifier

## Purpose
Identify the primary intent of a Telegram message.

## Categories

- вопрос — the author asks for information or clarification, even without a question mark.
- жалоба — the author reports a problem, expresses dissatisfaction, or complains about a service.
- предложение — the author suggests an improvement, change, or new idea.
- другое — greetings, thanks, neutral messages, or messages that cannot confidently be assigned to another category.

## Instructions

1. Read the entire message.
2. Determine the author's intent from meaning and context, not punctuation alone.
3. Return exactly one category.
4. If the message is ambiguous and context is insufficient, return другое.
5. Do not invent missing facts.
6. If multiple intents are present, select the primary intent. If it cannot be determined, return другое.

## Output format

Return only one lowercase word:

вопрос
жалоба
предложение
другое

Do not include explanations, quotation marks, or additional text.

## Do not use this skill when

- The user asks you to write a reply to a message.
- The user asks to edit or rewrite text.
- The user asks to create a social media post.
- The task is unrelated to classifying messages.
