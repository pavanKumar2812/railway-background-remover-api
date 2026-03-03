# Railway Background Remover API

AI-powered background removal API built with FastAPI and rembg.

## What is Background Remover API?

A Background Remover API is an AI-powered service that removes the background from images and returns a transparent PNG. This template uses FastAPI and the rembg library powered by the U²-Net deep learning model to automatically separate the foreground subject from the background.

## About Hosting Background Remover API

This template deploys a ready-to-use Background Remover API using FastAPI. Once deployed, users can upload an image via an API endpoint and receive a processed image with the background removed. The API uses the rembg library which loads the U²-Net model to perform image segmentation.

Railway handles the infrastructure, container build, and deployment automatically. After deployment, the API provides interactive documentation via the `/docs` endpoint so developers can test and integrate the service easily into their applications.

## Common Use Cases

- E-commerce product image background removal  
- Profile picture background editing  
- Image preprocessing for AI or computer vision pipelines  

## Dependencies for Background Remover API Hosting

- Python 3.11  
- FastAPI  
- rembg  
- Uvicorn  
- ONNX Runtime  

### Deployment Dependencies

rembg repository  
https://github.com/danielgatis/rembg

FastAPI documentation  
https://fastapi.tiangolo.com

## Demo

![Background remover demo](docs/demo.png)

## API

POST /remove-bg

Upload an image and get a transparent PNG back.

### Example (curl)

curl -X POST \
  -F "file=@image.jpg" \
  http://localhost:8000/remove-bg \
  --output output.png

## Run locally

pip install -r requirements.txt
uvicorn main:app --reload

## Deploy on Railway

[![Deploy on Railway](https://railway.com/button.svg)](https://railway.com/deploy/yOtmyd?referralCode=NetYKS&utm_medium=integration&utm_source=template&utm_campaign=generic)