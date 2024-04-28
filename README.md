# BiteBuddy - Restaurant Chatbot

Welcome to BiteBuddy, your friendly neighborhood restaurant chatbot developed for Pandey Ji Fresh and Delicious! BiteBuddy is designed to make your ordering experience seamless and efficient. This README provides essential information about BiteBuddy, its features, development, and usage.

## Overview

BiteBuddy is a chatbot developed using Dialogueflow, aimed at simplifying the ordering process for customers of Pandey Ji Fresh and Delicious restaurant. It facilitates order placement, order tracking, and status updates, ensuring a smooth dining experience.

## Features

- **Order Tracking**: Users can track the status of their orders through BiteBuddy. Three status updates are provided: "In Progress," "In Transit," and "Delivered."
- **Order ID Generation**: BiteBuddy generates a unique order ID for each order placed, which can be used for tracking purposes.
- **Order Placement**: BiteBuddy allows users to place orders for food items from the restaurant's menu.

## Technologies Used

- **Dialogueflow**: BiteBuddy is developed on the Dialogueflow platform for natural language processing and conversation management.
- **FastAPI**: The backend of BiteBuddy is built using FastAPI, a modern, fast (high-performance), web framework for building APIs with Python 3.11.0.
- **MySQL Connector**: MySQL Connector is used to establish a connection with the database for storing order information.

## Development

BiteBuddy is an end-to-end project that involves several steps:

1. **Order ID Generation**: BiteBuddy generates a unique order ID for each order placed, facilitating order tracking.
2. **Order Tracking Setup**: Database connections are established using MySQL Connector. The `db_helper` file contains all the necessary database connection configurations.
3. **Dialogueflow Integration**: The chatbot is trained on Dialogueflow using intents and entities to understand user queries and commands.
4. **NGROK Integration**: Due to the protocol mismatch between FastAPI (HTTP) and Dialogueflow (HTTPS), NGROK is utilized to enable webhook communication between the chatbot and the FastAPI server.

## Usage

To use BiteBuddy:

1. Start a conversation with BiteBuddy on your preferred messaging platform.
2. Follow the prompts to place your order and provide necessary information.
3. Receive an order ID for tracking purposes.
4. Use the provided order ID to track the status of your order as it progresses through the stages of "In Progress," "In Transit," and "Delivered."

## Directory structure

backend: Contains Python FastAPI backend code
db: contains the dump of the database. you need to import this into your MySQL db by using MySQL workbench tool
dialogflow_assets: this has training phrases etc. for our intents
frontend: website code

## Install these modules

- pip install mysql-connector
- pip install "fastapi[all]"

- OR just run pip install -r backend/requirements.txt to install both in one shot

## To start fastapi backend server

1. Go to backend directory in your command prompt
2. Run this command: uvicorn main:app --reload

## ngrok for https tunneling

1. To install ngrok, go to https://ngrok.com/download and install ngrok version that is suitable for your OS
2. Extract the zip file and place ngrok.exe in a folder.
3. Open windows command prompt, go to that folder and run this command: ngrok http 80000

NOTE: ngrok can timeout. you need to restart the session if you see session expired message.


## Contributors

- **Arnav A Verma**

We hope BiteBuddy enhances your dining experience at Pandey Ji Fresh and Delicious! If you have any feedback or encounter any issues, feel free to reach out to [your contact information]. Enjoy your meal! 🍔🥗🍕
