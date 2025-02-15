---
title: "How to Make OpenAI API Calls in Your JavaScript Application"
seoTitle: "OpenAI API Calls in JavaScript: A Guide"
seoDescription: "Learn how to make OpenAI API calls in your JavaScript application using the `openai-api-helper` npm package in this step-by-step guide"
datePublished: Mon Jul 22 2024 22:31:34 GMT+0000 (Coordinated Universal Time)
cuid: clyxka54j000309l69ftybqu0
slug: how-to-make-openai-api-calls-in-your-javascript-application
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1721687145157/9dad33d8-0e7f-4d2e-acd7-9272a7c1c96d.jpeg
tags: ai, openai, chatgpt

---

OpenAI provides a robust API that allows developers to leverage its state-of-the-art language models for various applications. However, interacting with APIs can sometimes be cumbersome, especially when handling authentication, constructing HTTP requests, and parsing responses.

This tutorial will guide you through making OpenAI API calls in a JavaScript application using a simple npm package called `openai-api-helper`.

You’ll learn how to install the `openai-api-helper` package, set it up in your JavaScript application, and make your first API call to OpenAI.

You can find more details on the `openai-api-helper` package here:

* [Github](https://github.com/Buddhsen-tripathi/openai-api-helper)
    

Before we begin, ensure you have the following:

* Nodejs should be installed.
    
* A valid OpenAI API key. You can obtain this by signing up for an API key on the [OpenAI website](https://beta.openai.com/signup/).
    

### Installing the `openai-api-helper` npm Package

To begin, you need to install the `openai-api-helper` package from npm. This package provides an easy-to-use interface for making requests.

Open your terminal and run the following command to install the `openai-api-helper` package:

```bash
npm install openai-api-helper
```

Ensure that your project is initialized with `package.json`. If you haven’t already done so, you can initialize it with:

```bash
npm init -y
```

### Usage

Now that you’ve installed the package, let’s write some code to make an API call to OpenAI. The following example demonstrates how to use the `openai-api-helper` package to interact with the OpenAI API.

1. **Create a JavaScript File**
    
    Create a new file named `app.js` (or any name you prefer) in your project directory.
    
2. **Write the Code**
    
    Add the following code to `app.js`:
    
    ```javascript
    const OpenAIHelper = require('openai-api-helper');
    
    async function main() {
        // Replace 'YOUR_OPENAI_API_KEY' with your actual OpenAI API key
        const apiKey = 'YOUR_OPENAI_API_KEY';
        const model = 'gpt-4';  // Specify the model you want to use
        const prompt = 'What is the capital of France?';
    
        // Initialize the OpenAIHelper with your API key
        const openai = new OpenAIHelper(apiKey);
    
        try {
            // Make the API call
            const response = await openai.call(model, prompt);
            // Log the response from OpenAI
            console.log('Response from OpenAI:', response);
        } catch (error) {
            console.error('Error:', error);
        }
    }
    
    main();
    ```
    
3. **Run Your Code**
    
    Execute the `app.js` file using Node.js:
    
    ```bash
    node app.js
    ```
    

You should see the response from OpenAI printed in your terminal.

**Example Output**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721686782663/f98a3b9c-7c99-4fac-874a-c602af96a0d4.png align="center")

Congrats! You've just made OpenAI API call from your Js Application.

Feel free to explore further and experiment with different prompts and models to fully harness the capabilities of OpenAI’s API.

If you have any questions or run into issues, don’t hesitate to reach out to me on socials or check out the documentation for more detailed information.