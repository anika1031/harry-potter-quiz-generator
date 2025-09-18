# Harry Potter quiz-generator

# Generate-HarryPotter-Quiz-from-Story

This repository contains LangFlow flows that generate Harry Potter multiple-choice quizzes (MCQs) from story text stored in Astra DB → https://astra.datastax.com

# Quiz Generator with LangFlow

Create auto-generated multiple-choice quizzes (MCQs) based on the Harry Potter universe using a no-code/low-code GenAI pipeline in LangFlow.

# 🪄 Project Goal

Build a GenAI pipeline that:

Ingests a Harry Potter story into Astra DB

Retrieves relevant story context

Generates validated multiple-choice quiz questions with correct answers

# Key Features

 - Story-driven quiz generation → Questions come directly from Harry Potter stories

- Interactive Q&A → You can ask questions and get quiz-style answers

 - Configurable question count → Decide how many questions you want

 - Extendable → Replace Harry Potter text with any other book/topic

# Architecture (Flow Overview)

Ingest Flow (quiz_ingest.json)
Story File → Split Text → Astra DB (storage)

Retrieve Flow (quiz_retrieve.json)
Chat Input → Astra DB → Parser → Prompt Template → Groq LLM → Chat Output

# Components Used in LangFlow

Input: User’s story text or question

Astra DB: Stores the Harry Potter story chunks

Parser: Enforces schema & structure

Prompt Template: Custom instructions to generate MCQs

LLM: Groq (can be swapped with other LLMs)

Output: Display quiz with answers

# Tech Stack

- LangFlow (flow orchestration)

- Astra DB (vector DB for context storage & retrieval)

- Groq LLM (for question generation)

- Python 3.12.1
