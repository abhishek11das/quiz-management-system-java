# Quiz Management System

## Project Overview
This is a simple **role-based quiz system** developed in Java. It supports two types of users:

- **Admin:** Can add multiple-choice questions (MCQs) to the question bank.
- **Student:** Can take a quiz composed of random MCQs from the question bank.

The system persists data using two JSON files:
- `users.json`: Stores user credentials and roles.
- `quiz.json`: Stores the MCQ question bank.

---

## Features

### Admin Features
- Login using username and password.
- Add MCQs with a question, four options, and an answer key.
- Can continuously add questions until quitting.
- The question bank is saved in `quiz.json`.

### Student Features
- Login using username and password.
- Take a quiz of 10 randomly selected questions.
- Each correct answer awards 1 mark; no negative marking.
- Displays score and feedback based on performance.
- Option to retake the quiz or quit.

## Technologies Used
- Java
- IntelliJ IDEA
- JSON Simple Library for JSON parsing and writing
- Command-line interface (CLI)

## JSON File Format

### users.json

```json
[
  {
    "username": "admin",
    "password": "1234",
    "role": "admin"
  },
  {
    "username": "salman",
    "password": "1234",
    "role": "student"
  }
]
```

### quiz.json

```json
[
  {
    "question": "Which is not part of system testing?",
    "option 1": "Regression Testing",
    "option 2": "Sanity Testing",
    "option 3": "Load Testing",
    "option 4": "Unit Testing",
    "answerkey": 4
  }
]
```


---

## 📊 Quiz Flow & Scoring

- The student receives 10 random questions from the question bank.
- Each correct answer awards 1 point.
- No negative marking for incorrect answers.

### 🧮 Score Feedback

| Score Range | Feedback Message                            |
|-------------|---------------------------------------------|
| 8 - 10      | Excellent! You have got [score] out of 10   |
| 5 - 7       | Good. You have got [score] out of 10        |
| 3 - 4       | Very poor! You have got [score] out of 10   |
| 0 - 2       | Very sorry, you are failed. Got [score]/10  |

---

## 📽️ Video Demonstration

### 🔐 Admin Functionality: Login & Add Questions:
https://github.com/user-attachments/assets/921d5383-04b4-47c6-ae1b-26aa7cb67ccc

### 🧑‍🎓 Student Functionality: Login & Take Quiz
https://github.com/user-attachments/assets/90b2503d-ccb4-42cb-9462-efd5334277dd
