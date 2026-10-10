<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Interactive FAQ</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f2f2f2;
            margin: 0;
            padding: 40px 20px;
        }

        .container {
            max-width: 700px;
            margin: auto;
        }

        h1 {
            text-align: center;
            color: #333;
            margin-bottom: 30px;
        }

        .faq {
            background-color: white;
            margin-bottom: 15px;
            border-radius: 8px;
            box-shadow: 0 2px 6px #ccc;
            overflow: hidden;
        }

        .question {
            width: 100%;
            padding: 18px;
            border: none;
            background-color: white;
            text-align: left;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
        }

        .question:hover {
            background-color: #f5f5f5;
        }

        .answer {
            display: none;
            padding: 0 18px 18px;
            color: #555;
            line-height: 1.6;
        }

        .answer.show {
            display: block;
        }

        .question::after {
            content: "+";
            float: right;
            font-size: 22px;
        }

        .question.active::after {
            content: "-";
        }
    </style>
</head>

<body>

    <div class="container">

        <h1>Frequently Asked Questions</h1>

        <!-- FAQ 1 -->
        <div class="faq">
            <button class="question">
                What is HTML?
            </button>

            <div class="answer">
                HTML stands for HyperText Markup Language.
                It is used to create the structure of web pages.
            </div>
        </div>

        <!-- FAQ 2 -->
        <div class="faq">
            <button class="question">
                What is CSS?
            </button>

            <div class="answer">
                CSS stands for Cascading Style Sheets.
                It is used to style and design web pages.
            </div>
        </div>

        <!-- FAQ 3 -->
        <div class="faq">
            <button class="question">
                What is JavaScript?
            </button>

            <div class="answer">
                JavaScript is a programming language used to
                make web pages interactive and dynamic.
            </div>
        </div>

        <!-- FAQ 4 -->
        <div class="faq">
            <button class="question">
                What is VS Code?
            </button>

            <div class="answer">
                Visual Studio Code is a code editor used for
                writing and developing websites and applications.
            </div>
        </div>

        <!-- FAQ 5 -->
        <div class="faq">
            <button class="question">
                What is DOM?
            </button>

            <div class="answer">
                DOM stands for Document Object Model.
                It allows JavaScript to access and modify HTML elements.
            </div>
        </div>

    </div>

    <script>

        // Select all question buttons
        const questions = document.querySelectorAll(".question");

        // Add event listener to each question
        questions.forEach(function(question) {

            question.addEventListener("click", function() {

                // Find the answer related to the clicked question
                const answer = this.nextElementSibling;

                // Show or hide the answer
                answer.classList.toggle("show");

                // Add or remove active class
                this.classList.toggle("active");

            });

        });

    </script>
</body>
</html>
