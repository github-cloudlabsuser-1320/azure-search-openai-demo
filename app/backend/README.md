# Backend for RAG Chat App

This directory contains the backend code for the Retrieval Augmented Generation (RAG) chat application, which leverages Azure OpenAI Service and Azure AI Search to provide a ChatGPT-like experience over your own documents.

## Overview

- **Framework:** Quart (async Python web framework)
- **API Protocol:** AI Chat HTTP Protocol
- **Location:** All backend code is in this `app/backend` directory.

## Key Features

- Handles chat and Q&A requests using RAG approaches.
- Integrates with Azure OpenAI for language models.
- Integrates with Azure AI Search for document retrieval.
- Supports custom approaches for chat and ask tabs.
- Provides endpoints for frontend communication.

## Directory Structure

- `app.py` — Main entry point for the backend server.
- `approaches/` — Contains RAG approach classes for chat and ask tabs.
- `services/` — Integrations for Azure OpenAI, Azure AI Search, and other services.
- `utils/` — Utility functions and helpers.
- `config.py` — Configuration and environment variable management.

## Running Locally

1. Ensure you have run `azd up` to provision Azure resources.
2. Authenticate with Azure:
   ```powershell
   azd auth login
   ```
3. Start the backend server:
   - **Windows:**  
     ```powershell
     ./app/start.ps1
     ```
   - **Linux/Mac:**  
     ```sh
     ./app/start.sh
     ```
   - **VS Code:** Use the "VS Code Task: Start App" task.

## Customization

- To customize RAG logic, edit or add classes in `approaches/`.
- For settings and environment variables, see `config.py`.
- For logging, see the logging configuration in `app.py`.

## Logging

- Logs from the backend are configured to show `INFO` level and above for app code, and `WARNING` and above for dependencies.
- You can change the log level via the `APP_LOG_LEVEL` environment variable.

## References

- Customizing the backend
- Productionizing the app
- Local development guide

## License

This project is licensed under the MIT License.
