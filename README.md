
# BaraBuddy


# Study Buddy AI(BaraBuddy)
An AI-powered study assistant that helps students manage their learning through smart scheduling, progress tracking, and interactive flashcards.



# 📚 BaraBuddy AI

**BaraBuddy AI** is a smart, student-focused assistant designed to help learners manage their education more effectively. It offers features like AI-generated study plans, progress dashboards, flashcards, and quizzes — all tailored to boost study consistency and learning outcomes.



## 🎯 Project Overview

- **Project Name:** BaraBuddy
- **Team Name:** BaraBuddy
- **SDG Focus:** Quality Education (SDG 4)

BaraBuddy is built to support students in managing their study habits through personalized recommendations, automated check-ins, and interactive learning features.



## 🌟 Features

- 🧠 **AI-Powered Study Assistant**: Get instant help on your subjects
- 📅 **Smart Study Scheduler & Planner**: Automatically plan your study time
- 📊 **Progress Dashboard**: Track your learning and consistency
- 📝 **Interactive Flashcards & Auto-Quizzes**: Boost memory with quick, smart quizzes
- 🔔 **Motivational Check-ins**: Stay motivated with nudges and feedback


## 🛠 Tech Stack

- **Languages & Libraries**: Python, OpenCV, scikit-learn, Keras, NumPy, Pandas
- **Development Tools**: Jupyter Notebook, Anaconda
- **Frontend (optional)**: Streamlit / Flask (for UI)



## 💡 Problem Statement

Students often struggle with staying consistent, organizing their study routines, and reviewing effectively. BaraBuddy AI helps solve this by providing an intelligent, personalized tool that adapts to each student's progress, learning needs, and habits.


### 📁 Installation & Setup
## 🦫 Barabuddy AI – Local Model Setup Guide

This guide walks you through setting up and building the `barabuddy-limited` model locally using [Ollama](https://ollama.com/), starting from scratch—even if you’re new to the process.


## Guide: Setting Up Open WebUI with a Custom Ollama Model (Windows)

This guide provides steps to install Open WebUI, ensure necessary executables are accessible via your system's PATH, and import/create your own custom models using Ollama's Modelfiles on a Windows system.

**Note:** This guide assumes you are using PowerShell for commands.

## Prerequisites

* **Python 3.8 or higher:** Required for installing Open WebUI via pip.
* **pip:** The package installer for Python (usually comes with Python).
* **Ollama:** The local large language model runner. Download and install the Windows version from [ollama.com](https://ollama.com/download).

## Step 1: Install Ollama

1.  Go to [ollama.com/download](https://ollama.com/download).
2.  Download the Windows installer.
3.  Run the installer and follow the on-screen instructions.


## Step 2: Download the model located at the top named:

# studybara-1746546173743.json


After downloading proceed to Step 3

## 📁 Step 3: Create a `Modelfile` from File Explorer

1. Navigate to the folder where you want to store your model, for example:
C:\Users\YourName\Documents\Barabuddy

3. Right-click inside the folder and select:
New > Text Document

4. Name the file exactly:
Modelfile

> ⚠️ Important:  
> - If you see `Modelfile.txt`, remove the `.txt` extension.  
> - If file extensions are hidden, go to:

>   - **View > Show > File name extensions** in File Explorer, then rename properly.

---

## ✍️ Step 4: Edit the Modelfile Contents

1. Right-click `Modelfile` and choose **Open with > Notepad**
2. Paste the following:
```bash

FROM llama3

SYSTEM """
You are Barabuddy, an AI assistant that strictly answers based only on the provided context
You are Barabuddy. When answering, ONLY provide direct, concise answers. 
Do NOT include "User Query", context tags, or helper phrases. 
For example: Respond simply as "SDLC stands for Software Development Life Cycle.".

Follow these rules carefully:

1. **Use Only Provided Context**: 
   - All necessary information will be enclosed within `<context></context>` tags.
   - Do NOT use any external knowledge beyond this context.

2. **Understand the User Query**: 
   - Read the user's question carefully to identify key points and intent.

3. **Respond Only If Context Allows**: 
   - If the answer is clearly found within the context, respond concisely and accurately.
   - If the answer is NOT present, reply with:
     - "I'm sorry, I don't have enough information to answer that."

4. **Ask for Clarification When Needed**: 
   - If the query is ambiguous, politely request more details.

5. **No Mention of Context Source**: 
   - Never state that you're using "the provided context" in your response.

6. **Language Consistency**: 
   - Always respond in the same language as the user's query.

When answering, be clear, concise, and to the point. Avoid unnecessary elaboration or speculation. Do not repeat the question in your answer.
"""


```

## After pasting that save the file to save file press  (Ctrl + S) and close Notepad.

Step 5: Open a Terminal Window (CMD or PowerShell)
Press Windows + R, type:
powershell
>Then hit Enter.


Step 6: Navigate to your project folder:
eg..("C:\Users\YourName")


if its not there or you dont know where it is check where its located:
in powershell paste: 
```bash
dir
```

Step 7: Build the Model with Ollama
Run this command in powershell:

```bash
ollama create barabuddy-limited -f Modelfile
```

If successful, you'll see something like:


writing manifest


success


Step 8: Run the Model

```bash
ollama run barabuddy-limited
```



## Step 9: Install Open WebUI

Open PowerShell and run the following command:

```bash
pip install open-webui
```
```bash
## To run open-webui
open-webui serve
```

## To open open-webui key in in your google search:
http://localhost:8080

## After installing Open-webui
1. Sign in or create account for open-webui
2. After signing in go to Workspace
3. In Workspace import model studybara-1746546173743
4. After importing press new chat and start chatting:)








