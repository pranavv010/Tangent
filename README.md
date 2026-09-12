# Tangent AI

Tangent AI is a comprehensive procedural material suite designed specifically for Blender. It leverages large language models to bridge the gap between natural language descriptions and complex procedural material generation in 3D environments.

## Overview

Procedural material creation in Blender often requires an extensive understanding of shader nodes, math operations, and material logic. Tangent AI abstracts this complexity by allowing users to generate complete material node trees and python scripts using simple natural language prompts. Additionally, it offers troubleshooting capabilities for developers and artists working with Blender's Python API.

## Core Features

- **Procedural Material Generation**: Translates natural language descriptions into executable Blender Python scripts that construct procedural shader node networks.
- **Free Chat and Troubleshooting**: An integrated assistant designed to analyze broken scripts, debug Blender API errors, and answer technical questions regarding material creation.
- **Automated Vercel Deployment**: The architecture is designed to run seamlessly on Vercel, with a Flask-based serverless backend and a lightweight vanilla JavaScript frontend.

## Architecture

The system is divided into two primary components:

### Frontend
- **Technology Stack**: Vanilla HTML, CSS, and JavaScript.
- **Functionality**: Provides a responsive user interface with distinct modes for material generation and general chat. It interfaces with the backend REST API to process user prompts.

### Backend
- **Technology Stack**: Python, Flask, and the NVIDIA API.
- **Functionality**: Acts as a serverless function hosted on Vercel. It receives user queries, constructs system prompts specific to Blender's API constraints, and securely communicates with inference endpoints to generate code or debugging steps.

## Installation and Local Development

To run the application locally, follow these steps:

1. Clone the repository.
2. Navigate to the `backend` directory and install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Create a `.env` file in the `backend` directory and configure your environment variables:
   ```env
   NVIDIA_API_KEY="your_api_key_here"
   FLASK_DEBUG=1
   ```
4. Start the backend server:
   ```bash
   python app.py
   ```
5. Open `frontend/index.html` in your web browser. Ensure that `env.js` is configured to point to `http://localhost:5000` for local development.

## Deployment

The application is configured for immediate deployment via Vercel. The `vercel.json` file is set up to route API requests to the Flask backend while serving the static frontend assets. 

1. Connect the repository to your Vercel account.
2. Add the required environment variables (e.g., `NVIDIA_API_KEY`) in the Vercel project settings.
3. Deploy the project. The configuration will automatically build the Python environment and serve the application.

## License

This project is intended for educational and developmental purposes.
