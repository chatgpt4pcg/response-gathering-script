# Reponse Gathering Script

This repository contains a script for gathering responses from ChatGPT API and produce a file with the responses.

## Installation

To use this script, you must have <a href="https://nodejs.org/en/" target="_new">Node.js</a> and <a href="https://www.npmjs.com/" target="_new">npm</a> installed on your system.

1. Clone this repository to your local machine.
2. Navigate to the repository directory in your terminal.
3. Run `npm install` to install the necessary dependencies.
4. Copy `.env.example` to `.env` and fill in the `OPENAI_API_KEY` which can be obtained by following [this page](https://platform.openai.com/docs/api-reference/making-requests).
5. Run `npx prisma generate` to generate Prisma client.
6. Run `npx prisma migrate dev --name init` to initialize database and sync with Prisma.

## Usage

1. Run the script using the command `npm start -s="<SOURCE_FOLDER>"`. For example, `npm start -s="./competition"`.
2. The script will output response files in `../<SOURCE_FOLDER>/competition/<TEAM_NAME>/raw/<CHARACTER>` folder. The file `response_log_<DATE_TIME>.txt` will be created in the `../<SOURCE_FOLDER>/competition/logs` folder.

**You might need to run the script at least *twice* to ensure that all responses are generated correctly.**

Please ensure that the source folder contains only text files.

Please note that interacting with ChatGPT via API costs money. Please refer to [this page](https://openai.com/pricing) for more information.

## Contributing

If you would like to contribute to this project, please fork this repository and submit a pull request. Please ensure that your code is well documented and that you have tested your code before submitting a pull request.

## Bug Reporting

If you find any bugs, please submit an issue on this repository.