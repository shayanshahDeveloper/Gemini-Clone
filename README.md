<h1 align="center">Hi 👋, I'm Shayan Shah</h1>
<h3 align="center">A Passionate Frontend Developer from Pakistan</h3>

# Gemini Chatbot Clone

A chatbot clone inspired by ChatGPT, built using React.js, CSS, JavaScript, and an API integration. The chatbot provides users with information in a conversational format, responding to various queries in real-time.

## ScreenShot

![Gemini main](https://github.com/user-attachments/assets/e025a7e3-1ec4-45c8-bd15-bd5988f6141c)
![Gemini main3](https://github.com/user-attachments/assets/037c5891-1398-4d59-9da9-22277afef2d2)
![Gemini main2](https://github.com/user-attachments/assets/0b7b9596-aee3-4a11-b2e2-9473179a3362)
![gif gemin](https://github.com/user-attachments/assets/394d58fd-5c0e-4551-84f8-571dc5838453)


## Demo

- [A live demo of the chatbot can be accessed here](https://geminibotclone.netlify.app/)

## Features

- Conversational Interface: Users can ask questions and receive real-time responses from the chatbot.
- Responsive design: The interface is optimized for both desktop and mobile devices.
- Natural Language Processing (NLP): Provides answers in a natural conversational flow.
- Customizable: Easily adaptable to provide specific information or services based on user queries.

## Technologies

- React.js: Framework used to build the frontend interface of the chatbot.
- CSS: For designing and styling a clean, modern UI.
- JavaScript: Handles chatbot logic, API calls, and interactivity.
- API Integration: Provides real-time responses based on the user’s input.

# Installation

Follow these steps to run the chatbot locally:

- Clone the repository:

```
https://github.com/shayanshahDeveloper/Gemini-Clone.git
```

## Install dependencies:

```
$ cd Gemini Clone   
$ npm install
$ npm install @google/generative-ai
```

## How to Get & Add the Gemini API Key

- Step 1: Go to Google and Search for: `Gemini Api`
 
  ![Gemini Clone Api](https://github.com/user-attachments/assets/05fdb0b7-1f4f-441f-aa70-d8f6ad8e14a1)
  
- Step 2: Click on get Api key
  
![Gemini Clone APi 2](https://github.com/user-attachments/assets/fdd0ced4-86ea-42fd-885d-56f92359fff7)


- Step 3: Click on Create Api key
  
  ![Gemini Clone APi 3](https://github.com/user-attachments/assets/fa0a7a66-fd2b-497f-b278-5b35b2e5b1cd)

- Step 4: Copy the Key
  
  ![Gemini Clone APi 4](https://github.com/user-attachments/assets/75c23870-fbeb-4975-8352-e851a413737b)

- Step 5: Paste the APi key in `gemini.js` as Shown in Screen-Shot
  
  ![Gemini Clone APi 5png](https://github.com/user-attachments/assets/03601965-5545-4e7e-a198-41c506f42c78)


## Run the project:

```
npm run dev
```

The project will be hosted on: `localhost:5173`

# API

The chatbot integrates with a backend API to process user queries and provide real-time responses. You can configure the API to respond with specific data or integrate with external sources of information.

- Example of an API call for retrieving chatbot responses:

```
import {
  GoogleGenerativeAI,
  HarmCategory,
  HarmBlockThreshold,
} from "@google/generative-ai";

const apiKey = "Enter Your API Key Here";
const genAI = new GoogleGenerativeAI(apiKey);

const model = genAI.getGenerativeModel({
  model: "gemini-1.5-flash",
});

const generationConfig = {
  temperature: 1,
  topP: 0.95,
  topK: 64,
  maxOutputTokens: 8192,
  responseMimeType: "text/plain",
};

async function run(prompt) {
  const chatSession = model.startChat({
    generationConfig,
    history: [],
  });

  const result = await chatSession.sendMessage(prompt);
  const response = result.response;
  return response.text();
}

export default run;
```

## Contributing

If you'd like to contribute to this project, follow the steps below:

- Fork the repository.
- Create a new branch: git checkout -b feature-name
- Commit your changes: git commit -m 'Add new feature'
- Push your branch: git push origin feature-name
- Submit a pull request.

#

<h3 align="left">Connect with me:</h3>
<p align="left">
<a href="https://linkedin.com/in/shayan-shah-b31439296" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="shayan-shah-b31439296" height="20" width="50" /></a>
</p>
