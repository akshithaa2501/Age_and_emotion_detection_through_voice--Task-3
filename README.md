# Age_and_emotion_detection_through_voice--Task-3
This app blocks female voices with an error message and processes male voices by age. It displays just the age for males under 60, but unlocks a senior tag and emotion graph for males over 60.

📋 Project Summary
1. The Problem (What the app does)
This app automatically sorts voice recordings using two strict rules:

Rule 1 (Gender Rule): The app only allows Male voices. If a Female voice is detected, it stops and shows a red error message: "Upload male voice."

Rule 2 (Age Rule): If it is a male voice, it calculates his age. If he is under 60, it only shows his age. If he is above 60, it labels him as a Senior Citizen, detects his emotion, and displays a colorful emotion bar graph.


2. Methodology (How it works behind the scenes)
Clean up: The app cuts out background silence from your uploaded clip.

Check Gender: If the voice pitch is higher than 150Hz, it labels it Female and blocks it.

Check Age: If it's under 150Hz, it labels it Male. If the sound brightness is low, it knows the speaker is a Senior Citizen (60+) and unlocks the emotion graph.


3. Results (What you see on the screen)
Female Upload: A red box pops up saying "Upload male voice."

Young Male Upload: Shows the exact age with a note saying emotion charts are skipped because he is under 60.

Senior Male Upload: Shows the age, tags him as a "Senior Citizen", and draws a clean bar chart showing his vocal emotion (like "Calm").



🛠️ How to Setup and Run in VS CodeStep

Step 1: Open Your Project in VS Code
Open VS Code.Go to the top menu and select File -> Open Folder.

Choose your project folder


Step 2: Open the Integrated TerminalYou don't need to open the Windows Command Prompt. VS Code has its own built-in terminal:
Go to the top menu of VS Code and click Terminal -> New Terminal (or press `Ctrl + ``).

A black terminal panel will pop up at the bottom of your VS Code screen, already pointed at your project folder.


Step 3: Install the Required Modules
Paste this command directly into the VS Code terminal at the bottom and hit Enter to install the necessary audio and dashboard packages:

pip install streamlit librosa numpy matplotlib seaborn soundfile


Step 4: Run the App
Make sure your file is saved as voice_task.py. In the exact same VS Code terminal panel, type this command and press Enter:

streamlit run voice_task.py


Step 5: Test Your Application
A web browser page will automatically open.

Drag and drop your audio files into the upload box on the screen to watch the app automatically verify the genders and calculate the ages!
