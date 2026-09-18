# quiz-cli

An interactive command-line quiz game for learning JavaScript. The application allows users to choose a quiz category and question count, answer multiple-choice questions, receive immediate feedback with explanations, and review their final results.

## Technology Stack

- JavaScript
- Node.js 18 or later
- ES modules
- Node.js `readline` API for interactive terminal input
- Node.js filesystem promises API for loading question data
- Node.js built-in test runner
- ANSI escape codes for terminal styling
- JSON question data

The project has no external npm dependencies.

## Project Structure

```text
.
├── colors.js
├── index.js
├── input.js
├── package.json
├── questions.json
├── quiz.js
├── .DS_Store
├── ._.DS_Store
├── ._colors.js
├── ._data
├── ._index.js
├── ._input.js
├── ._package.json
├── ._questions.json
├── ._quiz.js
└── ._src
```

### Important Files

| File | Purpose |
|---|---|
| `index.js` | CLI entry point. Creates the readline interface, loads quiz data, handles category and question-count selection, runs the quiz, displays results, and manages replay and cleanup. |
| `input.js` | Provides readline helpers for prompts, selections, confirmations, and pause behavior. |
| `quiz.js` | Contains the `Quiz` class, including question shuffling, progress tracking, answer handling, scoring, history, and result display. |
| `colors.js` | Provides ANSI terminal styling utilities and semantic color styles. |
| `questions.json` | Contains quiz categories and questions. |
| `package.json` | Defines project metadata, Node.js requirements, and npm scripts. |

The files beginning with `._` and the `.DS_Store` files appear to be macOS metadata artifacts and are not application source files.

## Prerequisites

- Node.js `>=18.0.0`
- An interactive terminal

No database, web server, Docker installation, external service, or environment variables are required.

## Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/bhavyasri20/test-app.git
   ```

2. Enter the project directory:

   ```bash
   cd test-app
   ```

3. Install dependencies if needed:

   ```bash
   npm install
   ```

   The project currently declares no dependencies, so there are no external packages to install.

4. Review the path layout described in [Known Path Mismatch](#known-path-mismatch) before starting the application.

## Configuration

The project does not define environment variables or a separate configuration file.

Quiz content is stored in:

```text
questions.json
```

The available categories identified in the repository are:

- JavaScript Basics
- Node.js Fundamentals
- General Programming

Each category contains five questions. Question objects include:

- The question text
- Multiple-choice options
- A zero-based answer index
- An explanation

## How to Run

The intended npm command is:

```bash
npm start
```

The equivalent direct command is:

```bash
node index.js
```

However, the current repository layout contains a path mismatch that may prevent either command from starting successfully. See [Known Path Mismatch](#known-path-mismatch).

## Usage Flow

When running successfully, the application follows this flow:

1. Launch the CLI.
2. Choose a quiz category.
3. Choose the number of questions:
   - All available questions
   - Three questions
   - Five questions
4. Press Enter to begin.
5. Answer questions by selecting numbered options.
6. Receive immediate feedback and an explanation after each answer.
7. View progress during the quiz.
8. View the final score and review incorrect answers.
9. Choose whether to replay or exit.

Input helpers validate numeric selections and yes/no responses.

## Key Features

- Interactive command-line quiz experience
- Category selection
- Configurable question count
- JavaScript, Node.js, and general programming questions
- Fisher-Yates question shuffling
- Progress bar display
- Immediate answer feedback
- Explanations for answers
- Score calculation
- Incorrect-answer review
- Performance messages based on score
- Replay loop
- ANSI terminal styling
- Error handling and readline cleanup
- ES module implementation using asynchronous JavaScript APIs

## Concepts Demonstrated

The project demonstrates:

- ES module imports and exports
- Promises and `async`/`await`
- Filesystem access with Node.js promises
- Interactive input with `readline`
- JavaScript classes
- Array methods
- Fisher-Yates shuffling
- Template literals
- ANSI terminal styling
- Error handling

## Known Path Mismatch

The application entry point currently references files in paths that do not exist in the observed repository layout.

`index.js` imports:

```text
./src/input.js
./src/quiz.js
./src/colors.js
```

It also loads:

```text
data/questions.json
```

The actual files are located at the repository root:

```text
input.js
quiz.js
colors.js
questions.json
```

As a result, `npm start` and `node index.js` are likely to fail with module or file-not-found errors until the import and data paths are aligned with the existing layout, or the files are moved into the paths expected by `index.js`.

## Testing

The project defines the following test script:

```bash
npm test
```

This runs Node.js's built-in test runner:

```bash
node --test
```

No test files were present in the observed repository, so automated test coverage is not currently available.

## Build

No build step is defined. The project is intended to run directly with Node.js.

## License

This project is licensed under the MIT License, as specified in `package.json`.
