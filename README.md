👨‍💻 Student Details

Roll Number: 7376241CS218
Training: AI Fluency Training
Day: 1
Focus: LLMs, Workflows and AI Agents


---

# 🚀 Day 1 AI Fluency Lab

## From Language Models to Tool-Based Agents

**Student Roll Number:** 7376241CS227

---

## 📝 Introduction

This project was developed as part of the Day 1 AI Fluency Training session.

The objective of the lab is to understand how an LLM-powered application can be designed in different ways, starting with direct question answering and progressing toward an agent capable of using application-defined functions.

The project contains:

1. A conversational LLM application
2. A Python-based workflow
3. A tool-enabled AI agent

---

## 🏗️ Architecture

The three approaches can be viewed as follows:

```text
                 User Input
                     │
          ┌──────────┼──────────┐
          ↓          ↓          ↓
       Chatbot    Workflow     Agent
          │          │          │
          ↓          ↓          ↓
        LLM        Rules       LLM
                                │
                           Tool Selection
                                │
                       ┌────────┴────────┐
                       ↓                 ↓
                  Fee Lookup        Calculator
                       │                 │
                       └────────┬────────┘
                                ↓
                           Final Answer
1️⃣ Direct Chatbot

The first program communicates directly with the configured language model.

The user provides a question and the model generates an answer.

This demonstrates basic LLM interaction without giving the model direct access to the application's course database.

2️⃣ Structured Workflow

The second program uses conventional Python logic.

Course codes are extracted from the user's question and matched with the course-fee information stored in the application.

For suitable questions, the workflow can also calculate totals and apply scholarship percentages.

This makes the processing deterministic for the rules that have been implemented.

3️⃣ Tool-Based Agent

The third implementation introduces tool calling.

The agent has access to two functions:

get_course_fee

Used when the agent needs the fee associated with a course.

calculator

Used when arithmetic operations are required.

The general process is:

User Request
     ↓
Language Model
     ↓
Determine Required Action
     ↓
Call Function
     ↓
Receive Result
     ↓
Generate Response
📊 Data Used by the Application

The application works with the following course-fee records:

Code	Course Fee
CS101	Rs. 12,000
AI202	Rs. 18,000
DS303	Rs. 15,000
🔬 Sample Tasks

The project evaluates different types of questions, including:

What is the fee for AI202?
What is the total fee for CS101 and AI202 after a 10% scholarship?
Is DS303 more expensive than CS101?
Write a two-line welcome message for new AI students
