MCP Calculator Demo
Overview

This project is a simple implementation of a Model Context Protocol (MCP) server built using .NET (C#).
It demonstrates how an AI / Large Language Model (LLM) can rely on server-side tools to perform calculations instead of handling the logic internally.

The project uses a basic calculator tool to show how arithmetic operations are passed to the MCP server and how the computed result is returned back to the AI.

How It Works
User Input
25 + 17 = ?

AI Tool Call
Add(25, 17)

Server Response
42


Rather than calculating the answer on its own, the AI calls the Add function exposed by the MCP server and uses the server’s response.

Project Structure
Calculator/
│
├── Program.cs      # MCP server entry point
├── Tools.cs        # Calculator tool implementation
└── mcp.json        # MCP configuration for AI interaction

Key Components
Program.cs

Starts the MCP server

Registers the available tools

Manages communication between the AI client and the server

Tools.cs

Contains the calculator logic

Exposes the Add(int a, int b) function for use through MCP

mcp.json

Defines the tool schema used by MCP

Describes available functions and their parameters

Helps the AI understand how to call the server-side tools

Running the Project
Requirements

.NET SDK 7 or later

Terminal or Command Prompt

Steps
cd Calculator
dotnet run


Once started, the MCP server will run and wait for tool calls from the AI client.

Why This Project

Understand how Model Context Protocol (MCP) works

See how AI systems interact with external tools

Explore a clean example of AI and C# integration

Useful as a reference project or learning example

Possible Improvements

Add more calculator operations (Subtract, Multiply, Divide)

Include logging for tool calls

Connect with OpenAI or Azure OpenAI clients

Add validation and error handling

Author

Srivathsan P S
