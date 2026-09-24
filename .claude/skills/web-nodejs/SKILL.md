---
name: web-nodejs
description: Develope web applications using Node.js and EJS templates and store data in sqlite database
---

### Workflow
1. Analyze the requirements for the web application from user's requirement both spec and html user interface mockups.
2. Implement web application following project structure and technology stack to cover all required features and functionalities.
3. Check user requirements and validate that all features are implemented correctly.
4. Check web layout and user interface to ensure it matches the HTML mockups and @DESIGN.md specifications and provides a good user experience.


## Technology Stack

- Node.js and Express framework
- EJS templates
  * https://www.npmjs.com/package/ejs
- SQLite file database (build-in sqlite in NodeJS)
  * https://nodejs.org/api/sqlite.html
- Call Anthropic API to upload file with [Anthropic SDK](https://www.npmjs.com/package/@anthropic-ai/sdk)
  * https://platform.claude.com/docs/en/build-with-claude/working-with-messages

## Project Structure with layer separation
```
src
  ├─ controllers
  ├─ models
  ├─ routes
  ├─ views
  ├─ database
     ├─ data_slip.db
     ├─ database.js
     └─ schema.sql
  ├─ services
     └─ anthropicService.js # call Anthropic API
  └─ app.js
```

## Best Practices
- Don't store sensitive information such as API keys directly in the code. Use environment variables instead.
- Keep the project structure organized by separating controllers, models, routes, views, and database-related files.
- Use environment variables to store sensitive information such as API keys.
- Validate user input to prevent SQL injection and other security vulnerabilities.
- Use async/await for handling asynchronous operations to keep the code clean and readable.
- Regularly back up the SQLite database to prevent data loss.
- Handle errors gracefully and provide meaningful error messages to users.
- Keep dependencies up to date to benefit from security patches and new features.
- Write unit tests for critical parts of the application to ensure reliability and facilitate future changes.
- Document the code and project structure to make it easier for new developers to understand and contribute.  