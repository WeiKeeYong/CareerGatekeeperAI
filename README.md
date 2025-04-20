# Career Gatekeeper AI

A proof-of-concept (POC) for filtering job prospects using a Telegram bot, n8n workflows, OpenAI's API, and Airtable for data storage. This project leverages an AI prompt to represent a tech leader (e.g., Bruce Lee) in evaluating job opportunities from headhunters or HR representatives, ensuring alignment with their skills and preferences.

## Overview

Career Gatekeeper AI automates the process of screening job offers by:
- Receiving job inquiries via a Telegram bot.
- Processing them through n8n workflows integrated with OpenAI's API.
- Using an AI prompt to filter jobs based on a tech leader’s profile, rejecting unsuitable roles (e.g., sales).
- Storing job details (e.g., job scope, salary, headhunter name) in Airtable for review.

The POC is designed for tech professionals, developers, and HR enthusiasts interested in AI-driven recruitment tools. The included XML prompt (`job_filter_prompt.xml`) is tailored for a tech leader with expertise in AI, cloud computing, and project management, but it can be customized for other profiles.

## Prerequisites

To set up and run Career Gatekeeper AI, you need:

1. **Telegram Bot**:
   - Create a Telegram bot using [BotFather](https://core.telegram.org/bots#6-botfather).
   - Obtain the bot’s API key.
   - Reference this [YouTube tutorial](https://www.youtube.com/watch?v=UQrcOj63S2o) for step-by-step guidance.

2. **OpenAI API Key**:
   - Sign up at [OpenAI](https://platform.openai.com/) and generate an API key.
   - Ensure sufficient credits for API usage.

3. **n8n with Publicly Accessible Webhook**:
   - Install and configure [n8n](https://n8n.io/) (self-hosted or cloud).
   - Set up a publicly accessible webhook on ports 443, 8443, 80, or 88 (Telegram does not support port 5678).
   - See this [dev.to article](https://dev.to/aimes/telegram-webhook-3p0) for Telegram webhook setup tips.

4. **Airtable Account and API Key**:
   - Sign up at [Airtable](https://airtable.com/) and create a base named `Agent Memory`.
   - Get API
   - Create a table named `job_prospect` with at least the following fields:
     - `social_id` (Single line text): Stores the sender’s Telegram ID or chat ID.
     - `messages` (Single line text): Stores job-related details or messages.
   - Obtain your Airtable API key from your [Airtable account](https://airtable.com/account).
   - Optionally, add fields like `job_scope`, `salary`, or `headhunter_name` for structured storage.

5. **Basic Technical Knowledge**:
   - Familiarity with JSON, webhooks, API integration, and XML editing.
   - Basic understanding of Airtable for data storage.
