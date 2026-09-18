# Tangent AI

Tangent AI is a comprehensive procedural material suite designed specifically for Blender. It leverages large language models to bridge the gap between natural language descriptions and complex procedural material generation in 3D environments.

## UI
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b3fa9229-a8a1-4ef4-bbff-db4adb460320" />

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

## License

This project is intended for educational and developmental purposes.
