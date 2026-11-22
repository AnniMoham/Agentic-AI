[🇬🇧 English](README.md) | [🇮🇷 فارسی](README.fa.md) 


# Agentic AI Learning Roadmap

## From Chatbot to AI Agent

This repository documents the learning path for building AI Agents with
Python, LLMs, OpenRouter, LangChain, LangGraph, and MCP.

## What is the difference between a Chatbot and an Agent?

A normal chatbot mainly answers questions:

    User
     ↓
    Question
     ↓
    LLM
     ↓
    Answer
     ↓
    Stop

An AI Agent receives a goal and works toward completing it:

    User Goal
     ↓
    Reasoning
     ↓
    Tool Usage
     ↓
    Result Evaluation
     ↓
    Next Decision
     ↓
    Completion

The main difference:

-   Chatbot: Answers questions
-   Agent: Completes tasks

------------------------------------------------------------------------

# How an AI Agent Works

An Agent usually follows a continuous loop:

## 1. Perception

The Agent understands:

-   User goal
-   Available information
-   Environment
-   Available tools

Example:

> "Find a good Italian restaurant in New York for tonight at 7 PM."

The Agent identifies what needs to be done.

------------------------------------------------------------------------

## 2. Reasoning

The LLM acts as the Agent's brain.

It decides:

-   What is the first step?
-   Which tool is needed?
-   What information is missing?
-   What should happen next?

Example:

    I need to:
    1. Search restaurants
    2. Check availability
    3. Make a reservation
    4. Send confirmation

------------------------------------------------------------------------

## 3. Action (Tool Calling)

This is the point where an Agent becomes different from a simple
chatbot.

The Agent can use tools:

-   Web search
-   APIs
-   Databases
-   Code execution
-   Email
-   Calendar
-   File systems

Example:

    LLM
     ↓
    Search Tool
     ↓
    Restaurant API
     ↓
    Reservation Tool
     ↓
    Email Tool

The Agent does not only generate text; it can perform actions.

------------------------------------------------------------------------

## 4. Evaluation

After performing an action, the Agent checks the result.

Example:

    Tool Result:
    No available table at 7 PM

The Agent can decide:

    Try 7:30 PM
    or
    Find another restaurant

This creates an iterative loop.

------------------------------------------------------------------------

# Important Concept

Every application using an LLM is not an Agent.

This code:

``` python
response = client.chat.completions.create(
    model="model-name",
    messages=[
        {
            "role": "user",
            "content": "Explain AI agents"
        }
    ]
)
```

is only an LLM application.

It becomes an Agent when we add:

-   Tools
-   Decision making
-   Planning
-   Memory
-   Execution loop

Architecture:

    Python Application
            |
            |
        OpenAI SDK
            |
            |
        OpenRouter
            |
            |
           LLM

# Final Architecture of an AI Agent

                 User Goal
                    |
                    ↓
                 Agent
                    |
            ----------------
            |              |
        Reasoning        Memory
            |
            ↓
           Tools
            |
            ↓
        External World
            |
            ↓
        Evaluation Loop
------------------------------------------------------------------------

# Agent Development Roadmap

## Step 1 - Python Basics

Required skills:

-   Variables
-   Functions
-   Classes
-   Modules
-   Error handling
-   Working with APIs


# Goal of This Repository

This repository is a practical journey from:

    LLM Application
            ↓
    Tool Calling
            ↓
    AI Agent
            ↓
    Advanced Agent Systems

The final goal is building real-world AI Agents using Python.
