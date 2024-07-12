# ESLint-Prettier-Husky Configuration Template for Node.js Projects

This project is a configuration template for integrating ESLint, Prettier, and Husky into Node.js projects. It provides pre-configured settings for these tools, which can be easily copied into any Node.js project.

ESLint is used for identifying and reporting on patterns found in ECMAScript/JavaScript code. Prettier is an opinionated code formatter, ensuring that all outputted code conforms to a consistent style. Husky is used to ensure that all commits meet the project's standards by running linters before each commit.

The project also includes instructions on how to make git pre-commit hooks executable and how to commit using the provided npm script.

## Requirements

- Node.js >= 20
- npm >= 10

## Installation

1. Clone the repository: `git clone git@github.com:neverovski/nodejs-eslint-prettier-husky.git`
2. Install dependencies: `npm install`

## Usage

Simply copy the files from this project template to your Node.js project.

```bash
$ cp -R /path-to-template/* /path-to-your-project/

```

## Configurations

**ESLint:** Configuration is in the .eslintrc.js file. Customize as needed.
**Prettier:** Configuration in the .prettierrc file. Modify as necessary.
**Husky:** Pre-configured to run linters before commit. Configuration in .husky directory

## Notes

### 1. Enable Git hooks

```sh
  npx husky install
  npx husky add .husky/commit-msg 'npm run commit-msg'
  npx husky add .husky/pre-commit 'npm run pre-commit'
```

### 2. Why is my git pre-commit hook not executable by default?

- Please execute the below command on terminal to hook get executable by default.
- Because files are not executable by default; they must be set to be executable.

```bash
$ chmod ug+x .husky/*
$ chmod ug+x .git/hooks/*
```

### 3. Git commit

```bash
$ npm run commit
```

### 4. Project release

```sh
  npm run release:patch // Patch release 0.1.0 -> 0.1.1
  npm run release:minor // Minor release 0.1.1 -> 0.2.0
  npm run release:major // Major release 0.2.0 -> 1.0.0
```

## Contribution

Happy to get your feedback, but also you are feel free to raise a pull request.

## License

This project is licensed under the MIT. See the LICENSE.md file for details.
