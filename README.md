# Quiz CLI

An interactive command-line quiz game for learning JavaScript, Node.js, and general programming concepts. Quiz CLI runs with Node.js and uses colorful terminal output, randomized questions, explanations, and score summaries to make learning engaging.

## Features

- Choose from JavaScript Basics, Node.js Fundamentals, and General Programming categories.
- Select all available questions or a shorter three- or five-question quiz when available.
- Answer questions through an interactive terminal menu.
- Randomize the order of questions for each quiz.
- View progress, immediate correctness feedback, explanations, and final scores.
- Review incorrect answers after completing a quiz.
- Replay without restarting the application.
- Uses only Node.js built-in modules; no runtime dependencies are required.

## Requirements

- Node.js 18 or newer
- A terminal that supports ANSI color escape codes

## Installation

Clone the repository and install the project metadata:

```bash
git clone https://github.com/bhavyasri20/test-app.git
cd test-app
npm install
```

The project has no external dependencies, so `npm install` is optional but useful for validating the package setup.

## Usage

Start the quiz with:

```bash
npm start
```

Follow the prompts to choose a category, select the number of questions, enter answers by number, and decide whether to play again.

## Testing

Run the configured Node.js test command with:

```bash
npm test
```

## Project Structure

```text
.
├── index.js          # Application entry point and main quiz loop
├── src/
│   ├── colors.js     # ANSI terminal color helpers
│   ├── input.js      # Readline prompts and menu selection
│   └── quiz.js       # Quiz state, scoring, and result display
├── data/
│   └── questions.json # Quiz categories and questions
└── package.json      # Project metadata and npm scripts
```

## Learning Topics

The codebase demonstrates ES modules, async/await, Promises, filesystem access, JSON parsing, readline input, classes, destructuring, array methods, error handling, and the Fisher–Yates shuffle algorithm.

## License

This project is licensed under the MIT License.
