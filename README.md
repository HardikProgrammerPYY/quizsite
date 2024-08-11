<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz Login and Quiz</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #e0f7fa;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            width: 90%;
            max-width: 800px;
            background: #ffffff;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
            padding: 20px;
            box-sizing: border-box;
        }
        h1 {
            text-align: center;
            color: #00796b;
        }
        .form-group {
            margin-bottom: 20px;
        }
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #00796b;
        }
        .form-group input, .form-group select {
            width: 100%;
            padding: 10px;
            border-radius: 5px;
            border: 1px solid #00796b;
            box-sizing: border-box;
        }
        .form-group button {
            width: 100%;
            padding: 10px;
            background: #00796b;
            color: #ffffff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }
        .form-group button:hover {
            background: #004d40;
        }
        .quiz-question {
            background: #f1f8e9;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 15px;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
        }
        .quiz-question label {
            margin-bottom: 5px;
            font-weight: normal;
            color: #004d40;
            display: block;
        }
        .quiz-question input[type="radio"] {
            margin-right: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Login</h1>
        <form id="login-form">
            <div class="form-group">
                <label for="username">Username</label>
                <input type="text" id="username" name="username" required>
            </div>
            <div class="form-group">
                <label for="password">Password</label>
                <input type="password" id="password" name="password" required>
            </div>
            <div class="form-group">
                <button type="submit">Login</button>
            </div>
        </form>

        <div id="quiz-section" style="display: none;">
            <h1>Quiz</h1>
            <form id="quiz-form">
                <div class="quiz-question">
                    <label>1. What is the capital of France?</label>
                    <label><input type="radio" name="question1" value="Paris" required> Paris</label>
                    <label><input type="radio" name="question1" value="London"> London</label>
                    <label><input type="radio" name="question1" value="Berlin"> Berlin</label>
                    <label><input type="radio" name="question1" value="Madrid"> Madrid</label>
                </div>
                <div class="quiz-question">
                    <label>2. What is 5 + 7?</label>
                    <label><input type="radio" name="question2" value="10" required> 10</label>
                    <label><input type="radio" name="question2" value="12"> 12</label>
                    <label><input type="radio" name="question2" value="14"> 14</label>
                    <label><input type="radio" name="question2" value="16"> 16</label>
                </div>
                <div class="quiz-question">
                    <label>3. What is the largest planet in our solar system?</label>
                    <label><input type="radio" name="question3" value="Earth" required> Earth</label>
                    <label><input type="radio" name="question3" value="Mars"> Mars</label>
                    <label><input type="radio" name="question3" value="Jupiter"> Jupiter</label>
                    <label><input type="radio" name="question3" value="Saturn"> Saturn</label>
                </div>
                <div class="quiz-question">
                    <label>4. Who wrote "To Kill a Mockingbird"?</label>
                    <label><input type="radio" name="question4" value="Harper Lee" required> Harper Lee</label>
                    <label><input type="radio" name="question4" value="Mark Twain"> Mark Twain</label>
                    <label><input type="radio" name="question4" value="Ernest Hemingway"> Ernest Hemingway</label>
                    <label><input type="radio" name="question4" value="J.K. Rowling"> J.K. Rowling</label>
                </div>
                <div class="quiz-question">
                    <label>5. What is the chemical symbol for gold?</label>
                    <label><input type="radio" name="question5" value="Au" required> Au</label>
                    <label><input type="radio" name="question5" value="Ag"> Ag</label>
                    <label><input type="radio" name="question5" value="Fe"> Fe</label>
                    <label><input type="radio" name="question5" value="Hg"> Hg</label>
                </div>
                <div class="form-group">
                    <button type="submit">Submit Quiz</button>
                </div>
            </form>
        </div>
    </div>

    <script>
        document.getElementById('login-form').addEventListener('submit', function(e) {
            e.preventDefault();
            // Simulate login validation (not implemented in this example)
            document.getElementById('quiz-section').style.display = 'block';
            document.getElementById('login-form').style.display = 'none';
        });

        document.getElementById('quiz-form').addEventListener('submit', function(e) {
            e.preventDefault();
            // Handle quiz submission here
            alert('Quiz submitted!');
        });
    </script>
</body>
</html>
