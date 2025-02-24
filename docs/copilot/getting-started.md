---
Order: 4
Area: copilot
TOCTitle: Quickstart
ContentId: 37fd3bd2-4209-49f6-bec5-c544d6b1b289
PageTitle: GitHub Copilot quickstart
DateApproved: 10/29/2024
MetaDescription: Get started with GitHub Copilot in Visual Studio Code and create your first AI-powered suggestions in the editor.
MetaSocialImage: images/shared/github-copilot-social.png
---
# Getting started with GitHub Copilot in VS Code

This tutorial walks you through the key features of GitHub Copilot in Visual Studio Code. Learn how to get started with the [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot) extension to get AI-powered code suggestions in the editor, use chat conversations to refactor your code, and fix code errors with smart actions.

> **Note:** While we're using TypeScript for this tutorial, please note that Copilot is also trained on numerous other languages and a wide variety of frameworks.

For an overview of what you can do with GitHub Copilot in VS Code, see the [GitHub Copilot Overview](/docs/copilot/overview.md).

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/2q0BoioYSxQ" title="GitHub Copilot Best Practices (what not to do)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Prerequisites

* To use GitHub Copilot in VS Code, you must have the [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot) extension. When you install this extension, the [GitHub Copilot Chat](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-chat) extension is also installed.

* To use GitHub Copilot, you must have an active subscription for GitHub Copilot in your personal account, or you need to be assigned a seat by your organization.

Follow these steps to [set up GitHub Copilot in VS Code](/docs/copilot/setup.md) by signing up for a subscription and installing the Copilot extension in VS Code.

## Get your first code suggestion

Now that you've signed up for Copilot and activated the extension, let's see its assistance in action!

To get started with GitHub Copilot in VS Code, you don't have to do anything special. As you're typing code in the editor, Copilot automatically presents you code suggestions in the editor to help you code more efficiently.

1. Open Visual Studio Code and create a new TypeScript file `Calculator.ts`.

1. In the TypeScript file, start typing the following class definition.

    ```typescript
    class Calculator
    ```

    Copilot automatically suggests a method for our `Calculator` class in gray dimmed text (ghost text). In our example, the `add` method is suggested. The exact suggestions can vary.

    ![Screenshot of VS Code editor, showing Copilot suggesting the `add` method inside the `Calculator` class.](./images/getting-started/copilot-code-completion.png)

1. To accept the suggestion, press the `kbstyle(Tab)` key.

    Congratulations! You've just accepted your first AI-powered inline suggestion. As you continue typing, Copilot updates the inline suggestion accordingly.

1. For any given input, there might be multiple suggestions. Type the following inside the class to add a `fibonacci` method:

    ```typescript
    fibonacci(n: number): number {
    ```

1. Hover over the suggestion in the editor and notice that there are multiple suggestions.

    ![Screenshot of VS Code editor, showing Copilot giving multiple suggestions for `fibonacci` when hovering over it.](./images/getting-started/copilot-code-completion-multiple.png)

    You can use the arrow controls or use the keybindings to show the next (`kb(editor.action.inlineSuggest.showNext)`) or previous (`kb(editor.action.inlineSuggest.showPrevious)`) suggestion.

AI-powered code completions can help you with generating boilerplate or repetitive code, letting you stay in the developer flow and focus on more complex coding tasks.

## Generate a simple web server with Copilot Chat

With the [Copilot Chat](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-chat) extension, you can start a chat conversations with Copilot in VS Code to ask specific tasks about your code by using natural language.

Let's use Copilot Chat to help us generate a simple Express web server.

1. First, add a new TypeScript file `server.ts` to your workspace.

    Let's use the Copilot Inline Chat in the editor to generate a simple Express web server.

1. Now, press `kb(inlinechat.start)` on your keyboard to bring up Copilot Inline Chat.

    With Copilot Inline Chat you get a chat interface that lets you ask questions about your code by using natural language.

    ![Screenshot of VS Code editor, showing the Copilot Inline Chat control.](./images/getting-started/copilot-inline-chat.png)

1. Type *"add a simple express web server"* in the chat input field, and press `kbstyle(Enter)` to send the chat request or prompt to Copilot.

    Notice that Copilot returns a streaming response into the editor. The response is an implementation for a simple Node.js Express web server.

    ![Screenshot of VS Code editor, showing the Copilot Inline Chat response for adding an Express web server.](./images/getting-started/copilot-inline-chat-express-server.png)

1. Select **Accept** or press `kb(inlineChat.acceptChanges)` to apply the proposed code changes.

    Congratulations! You've used Copilot Chat for generating code using chat and natural language.

Now, let's use Copilot Chat to help us refactor our code and return a static HTML file when users navigate to the home page.

## Refactor your code through AI chat

As you work on an existing codebase, you often need to refactor or improve existing code. You'll use Copilot Chat to refactor and iterate over your code.

Let's update the `/` route to return a static HTML page.

1. In the editor, select the `app.get('/', req, res)` method, and then press `kb(inlinechat.start)` to start Inline Chat.

    By selecting a range of text in the editor, you provide more context to Copilot about your request.

1. Type *"return a static index.html file"* in the chat input field, and press `kbstyle(Enter)` to send the chat request or prompt.

    Notice how Copilot updates the existing method implementation to return an `index.html` file.

    ![Screenshot of VS Code editor, showing the Copilot Inline Chat suggested changes, highlighting the `Show changes` button.](./images/getting-started/copilot-inline-chat-refactor.png)

1. Select **Accept** or press `kb(inlineChat.acceptChanges)` to apply the proposed code changes.

    Experiment further with Copilot Chat, for example to use an environment variable for the port number, to add more routes to your web server, or ask Copilot Chat to add error handling, and more.

    ![Screenshot of VS Code editor, showing the Copilot Inline Chat to use an environment variable for the port number.](./images/getting-started/copilot-inline-chat-refactor-port.png)

With Copilot Chat you can use a chat conversation and natural language to direct Copilot to perform specific tasks on your codebase. With Inline Chat, you can stay in the flow of coding, and ask for AI assistance in the moment, when you need it, without switching context.

## Use Copilot Chat for general programming questions

As you're working in a new codebase, or exploring a new programming language, you might have more general coding questions come up. Copilot Chat lets you open a chat conversation on the side, and which keeps track of the history of your questions.

1. Open the Chat view from the Command Center chat menu or press `kb(workbench.action.chat.open)`.

    ![Screenshot of VS Code editor, showing the Copilot Chat view, highlighting the chat menu in the Command Center.](./images/getting-started-chat/command-center-open-chat.png)

    > [!TIP]
    > You can access different Copilot features from the Command Center menu at any time.

1. Type "what is recursion?" in the chat input field and press `kb(workbench.action.chat.submit)` to send the request to Copilot.

    ![Screenshot of VS Code editor, showing the Copilot Chat view containing the answer to what recursion is. The result contains both text and a code block.](./images/getting-started/copilot-chat-view-recursion.png)

    Notice how the chat response contains rich results, consisting of text and a code block. The code block in the chat response supports IntelliSense, which enables you get information about methods and symbols by hovering over them, or to go to their definition.

## Fix coding errors with Copilot

Aside from inline completions and chat conversations, GitHub Copilot is available in different places and throughout your developer flow in VS Code. You might notice the presence of Copilot functionality through the *sparkle* icon in the VS Code user interface.

One such place is the Copilot coding actions in the editor, whenever there you have a red squiggle because of a compiler error. Let's see how Copilot can help with resolving coding errors.

1. Open the `server.ts` TypeScript file that you created earlier in the editor.

    Notice that the `import express from 'express';` statement contains a red squiggle. If you put the cursor on the red squiggle, you can see the Copilot sparkle appear.

    ![Screenshot of VS Code editor, showing the Copilot sparkle because of an error with the express import statement.](./images/getting-started/copilot-code-action-sparkle.png)

1. Select the sparkle to view the Copilot code actions, and then select **Fix using Copilot**.

    ![Screenshot of VS Code editor, showing the Copilot code actions, hihglighting `Fix using Copilot`.](./images/getting-started/copilot-code-action-fix.png)

1. Notice that the Copilot Inline Chat comes up, prepopulated with the error message, and a solution to fix the problem.

    ![Screenshot of VS Code editor, showing the Copilot Inline Chat proposing to install the express npm package to solve the problem.](./images/getting-started/copilot-code-action-fix-result.png)

    Directly from the chat response, you can optionally select the **Insert into Terminal** button to copy the proposed command in your terminal.

## Congratulations

Congratulations, you've now used artificial intelligence to enhance your coding! In this tutorial, you successfully set up Copilot in VS Code, and used Copilot code completions, Copilot Chat, and code actions to help you code more efficiently.

You've started experimenting with Copilot and there's a lot more you can do with it! To learn more about Copilot Chat, proceed to the [Copilot Chat Tutorial](/docs/copilot/getting-started-chat.md).
