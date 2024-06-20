# EduAiBuilder

## Summary of the Project

**EduAiBuilder**  is a platform that makes learning about artificial intelligence (AI) easier for beginners. It helps users create, train, and use their own AI models.

The project consists of five key components that work together seamlessly to provide a comprehensive learning experience:

### Components:

1. **Frontend App for Trainers Management**
    - **Goal**: Empower users to manage and configure AI trainers.
    - **Technologies**: Built with Next.js, React, and TypeScript.
    - **Features**:
        - User authentication
        - CRUD operations for trainers
        - Image collection and management
        - Real-time monitoring and exporting of trained models
    - **Link**: [trainers-front](https://github.com/EduAiBuilder/trainers-front) 

2. **Backend for Trainers Management**
    - **Goal**: Support the frontend with data management and integration with external services.
    - **Technologies**: Developed using Node.js, NestJS, and TypeORM.
    - **Features**:
        - Handles authentication
        - Manages trainer data
        - Interacts with Amazon SQS for image searches using the Bing API
        - Stores data in MySQL and S3
        - Provides endpoints to initiate model training
    - **Link**: [trainer-backend](https://github.com/EduAiBuilder/trainer-backend) 

3. **Training Application**
    - **Goal**: Train AI models using user-defined datasets.
    - **Technologies**: Implemented with Python and FastAPI.
    - **Features**:
        - Consumes messages from the queue
        - Retrieves data from the backend
        - Trains models using the Fast.ai framework
        - Sends progress updates
        - Exports trained models as PKL files to S3
    - **Link**: [training-service](https://github.com/EduAiBuilder/training-service) 

4. **Inference Frontend App**
    - **Goal**: Enable users to apply trained AI models to real-world data through a mobile-friendly interface.
    - **Technologies**: Developed using React.
    - **Features**:
        - Extracts model ID from URLs
        - Accesses the camera to capture images
        - Sends images and model ID to the backend
        - Displays prediction results in real-time
    - **Link**: [inference-front](https://github.com/EduAiBuilder/inference-front) 

5. **Inference Backend App**
    - **Goal**: Provide scalable and efficient inference capabilities for AI models.
    - **Technologies**: Built with FastAPI and Python, deployed on AWS Lambda for serverless execution.
    - **Features**:
        - Receives model ID and images
        - Identifies and loads the correct model
        - Performs inference
        - Returns predictions to the frontend
    - **Link**: [inference-backend](https://github.com/EduAiBuilder/inference-backend) 

**EduAiBuilder** aims to simplify AI for learners by integrating all these components into a cohesive system, allowing users to experience the full lifecycle of AI model development—from configuration and training to real-world application and inference.
