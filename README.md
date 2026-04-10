# 🚀 AI Cinematic Wallpaper Generator (Modular Langflow Flow)

This project is a modular AI orchestrator built in **Langflow** that converts simple user ideas into high-end, professional cinematic photography descriptions for 4K wallpaper generation.

Unlike standard monolithic prompts, this system uses a **three-node architecture** to ensure absolute control over the AI's output, optimizing lighting, camera composition, and rendering parameters.

## 🛠️ Modular Architecture

The system is divided into independent modules for easier debugging and scaling:

1.  **Input Layer:** Captures the basic user idea via the Langflow Playground.
2.  **Logic Core (Constructor & Executor):** A custom Python component that injects professional prompt engineering rules and handles the API call to Pollinations/Vertex AI.
3.  **Parsing Layer:** A data extraction module that cleans the JSON response and delivers only the final prompt to the chat interface.

## ⚙️ Mandatory Configuration

For security reasons, this flow is distributed **without an active API key**. To make the system work, you must configure your own credentials:

### 1. Insert API Key
* Locate the node named **"Constructor y Ejecutor API"**.
* Click the **Code** button (`{}`).
* Find the `headers` dictionary and replace the `Authorization` value with your own key:
    `"Authorization": "Bearer YOUR_API_KEY_HERE"`

### 2. AI Customization
If you want the AI to follow a specific style (e.g., more artistic, less technical), you can modify the instructions within the `payload["messages"]` block inside the same node. The entire behavior of the "Wallpaper Architect" is defined here.

## 🚀 Installation & Usage

1.  Ensure you have **Langflow 1.0+** installed.
2.  Import the provided `.json` file into your workspace.
3.  This flow is optimized for installed network environments and ephemeral pods, where JSON portability is key to maintaining settings across sessions.
4.  Open the **Playground**, type a simple concept (e.g., *"Cyberpunk city, neon lights"*), and receive a professional technical prompt instantly.

## 🌟 Why this project?

This generator was built to showcase the power of **Modular AI Engineering**. By decoupling the API request from the response parsing, users can access metadata such as request IDs or token counts without needing to repeat the API call.

---
*Developed for AI Automation and Prompt Engineering research.*

<img width="1287" height="724" alt="image" src="https://github.com/user-attachments/assets/4728863a-1577-428a-80c9-a283eb7273db" />

image generated with Nano Banana 2
