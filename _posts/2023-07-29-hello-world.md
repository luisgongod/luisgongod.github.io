---
layout: post
title: Haikus with Python
date: 2023-07-29 13:30 +0200
categories: [Programing, python]
tags: [tags, python, openai, chatgpt, haiku]
---

## Haiku

 🐍🌸

Have you ever wanted to generate beautiful Haikus effortlessly using Python? Look no further! Today, we'll explore how to create a Python script to get Haikus from ChatGPT, the powerful language model. Let's dive in! 🚀

Step 1: Set Up OpenAI API
To get started, you'll need an API key from OpenAI. Head over to OpenAI's website and sign up for an account. Once you have your API key, make sure you have the OpenAI Python package installed by running:

```bash
pip install openai
```

Step 2: Import Libraries
In your Python script, import the required libraries:

```python
import openai
```

Step 3: Authenticate with OpenAI
Use your API key to authenticate with OpenAI:

```python
openai.api_key = "YOUR_API_KEY"
```

Step 4: Generate Haikus
Now, let's write the function to generate Haikus using ChatGPT:

```python
def generate_haiku(prompt):
    response = openai.Completion.create(
        engine="text-davinci-002",
        prompt=prompt,
        temperature=0.7,
        max_tokens=50,
        top_p=1.0,
        frequency_penalty=0.0,
        presence_penalty=0.0,
    )
    haiku = response['choices'][0]['text'].strip()
    return haiku
```

Step 5: Get Haikus from ChatGPT
Time to put it all together! You can now prompt ChatGPT to generate Haikus:

```python
if __name__ == "__main__":
    prompt = "Write a Haiku about nature"
    haiku = generate_haiku(prompt)
    print(haiku)
```

Step 6: Experiment and Refine
Play around with the prompt and the parameters to get different styles and themes for your Haikus. Adjusting the temperature and token limits can lead to more creative or focused outputs.

Remember, Haikus are traditional Japanese poems with a 5-7-5 syllable pattern across three lines. Feel free to add constraints to ensure the generated output follows this structure.

Now you have the power of ChatGPT to create beautiful Haikus on the fly! 🌸 Unleash your creativity and explore the possibilities of language models with Python.

Enjoy creating and sharing your poetic masterpieces! Happy coding! 😊✨
