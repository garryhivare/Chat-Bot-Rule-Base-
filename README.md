# Chat-Bot-Rule-Base-
🤖 Rule-Based AI Python ChatBot

A simple rule-based chatbot built using Python.
This chatbot interacts with the user, greets them based on the current time, and responds to predefined questions using a dictionary-based logic.

📌 Features

👋 Greets the user by name

⏰ Time-based greeting (Morning / Afternoon / Evening / Night)

💬 Responds to basic user questions

🧠 Rule-based logic using Python dictionary

🔁 Continuous conversation until user types bye

🌐 Supports English + Hinglish inputs

🛠️ Technologies Used

Python 3

Built-in modules:

datetime

time

📂 Project Structure
Rule-Based-AI-ChatBot/
│
├── chatbot.py        # Main Python chatbot program
├── README.md         # Project documentation

⚙️ How the ChatBot Works
1️⃣ User Greeting

Asks for the user’s name.

Detects the current hour using datetime.

Displays greeting based on time:

Morning (5–11)

Afternoon (11–17)

Evening (17–20)

Night (else)

2️⃣ Predefined Responses (Rule-Based AI)

The chatbot uses a dictionary (responses) to store questions and answers.

Example:

responses = {
    "hello": "Hi, welcome. How can I help you?",
    "how are you": "I am very fine. Thank you",
    "who are you": "I am smart AI chatbot",
    "motivate me": "Keep going. Every bug of your project makes you a better developer"
}


User input is converted to lowercase

Bot checks if any key matches the input

If matched → returns response

If not matched → returns default message

3️⃣ Response Logic Function
def getResponseOfBot(userQuestion):
    userQuestion = userQuestion.lower()
    for eachKey in responses:
        if eachKey in userQuestion:
            return responses[eachKey]
    return "I am not able to tell that yet. Mai jald hi ye sikh lunga"

4️⃣ Chat Loop

The chatbot keeps running inside a while True loop

Conversation continues until user types bye

if "bye" in userInput.lower():
    break

▶️ How to Run the Project

Install Python 3

Save the file as chatbot.py

Open terminal or command prompt

Run the program:

python chatbot.py

💬 Sample Output
Swagat h, enter your name : Gaurav
Good evening, Gaurav
Namaste! Welcome to Your ChatBot
You can ask me basic question, Type 'bye' to exit from the bot

Please ask your question: hello
Bot Response: Hi, welcome. How can I help you?

Please ask your question: motivate me
Bot Response: Keep going. Every bug of your project makes you a better developer

Please ask your question: bye
Bot Response: I am not able to tell that yet. Mai jald hi ye sikh lunga

🚀 Future Improvements

Add more responses

Use JSON file for chatbot memory

Add NLP using NLTK / spaCy

Convert into GUI or Web-based chatbot

Add voice input/output

👨‍💻 Author

Gaurav Hivare
Beginner Python Developer | AI & Software Enthusiast
