 Quiz Application

A simple interactive quiz app built with vanilla JavaScript, HTML, and CSS that tests users through multiple-choice questions.

 Features

- 📝 Multiple-choice questions with 3 options
- 📊 Score tracking system
- 📈 Progress indicator
- 🏆 Final results display
- 🔄 Restart capability
- 📱 Responsive design

Project Structure
quiz-app/
│
├── index.html - Main HTML file with structure and inline styles
├── script.js - JavaScript functionality (inline in HTML in this implementation)
│
│── (Optional separate files):
│ ├── style.css - Stylesheet (currently inline in HTML)
│ └── data.js - Quiz questions data (currently in script.js)



 Data Structure

The quiz questions are stored in an array of objects with the following structure:


const quizData = [
    {
        question: "Question text here",
        options: ["Option 1", "Option 2", "Option 3"],
        correct: indexOfCorrectAnswer // (0-based index)
    },
    // ... more question objects
];
Core Functions
displayQuestion()
Renders the current question and options

Shows progress indicator

Uses array.map() to generate option buttons

selectAnswer(selectedIndex)
Handles answer selection

Compares selected answer with correct index

Updates score and progresses to next question

Uses array index navigation

showResults()
Displays final score after last question

Shows restart option

Uses template literals for result display

Array Method Usage
map() - Used to generate HTML for answer options


options.map((option, index) => `<button ...>${option}</button>`)
length - Used for progress tracking and score calculation

Question ${currentQuestionIndex + 1} of ${quizData.length}
