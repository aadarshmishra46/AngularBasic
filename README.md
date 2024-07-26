# AngularBasic


### Day 1: Introduction to Angular
- **Objective:** Understand what Angular is and set up the development environment.
- **Tasks:**
  - Read about Angular and its features.
  - Install Node.js and npm (if not already installed).
  - Install Angular CLI: `npm install -g @angular/cli`
  - Create your first Angular app: `ng new my-first-app`
  - Serve the application: `ng serve`

### Day 2: Angular Project Structure
- **Objective:** Learn the structure of an Angular project.
- **Tasks:**
  - Explore the files and folders created by the Angular CLI.
  - Understand the purpose of key files: `src/app/app.module.ts`, `src/app/app.component.ts`, etc.
  - Read about Angular modules and components.

### Day 3: Components and Templates
- **Objective:** Learn about components and templates in Angular.
- **Tasks:**
  - Create a new component using Angular CLI: `ng generate component my-component`
  - Understand the component decorator and its metadata.
  - Create a simple template and use data binding (`{{ }}`) to display data.

### Day 4: Directives
- **Objective:** Understand and use Angular directives.
- **Tasks:**
  - Read about built-in directives: `ngIf`, `ngFor`, `ngClass`, `ngStyle`.
  - Use these directives in your component templates.
  - Create a list using `ngFor` and conditionally display elements using `ngIf`.

### Day 5: Services and Dependency Injection
- **Objective:** Learn about services and dependency injection.
- **Tasks:**
  - Create a new service using Angular CLI: `ng generate service my-service`
  - Understand how to provide and inject services in Angular.
  - Use a service to share data between components.

### Day 6: Routing
- **Objective:** Learn about Angular routing.
- **Tasks:**
  - Understand the Angular Router and its configuration.
  - Create multiple components and set up routes for them.
  - Use `routerLink` to navigate between routes.

### Day 7: Forms
- **Objective:** Learn about template-driven and reactive forms.
- **Tasks:**
  - Understand template-driven forms: Create a simple form and handle form submission.
  - Learn about reactive forms: Create a form using `FormGroup` and `FormControl`.

### Day 8: HTTP Client
- **Objective:** Learn how to make HTTP requests in Angular.
- **Tasks:**
  - Understand Angular's `HttpClient` module.
  - Make GET and POST requests to a mock API.
  - Handle responses and errors.

### Day 9: Angular Material
- **Objective:** Learn about Angular Material and use it to style your application.
- **Tasks:**
  - Install Angular Material: `ng add @angular/material`
  - Import a few Angular Material components (e.g., buttons, inputs, cards) into your project.
  - Use these components in your templates.

### Day 10: Project Work
- **Objective:** Apply what you've learned to build a small project.
- **Tasks:**
  - Define a simple project (e.g., a to-do list, a weather app).
  - Create components, services, and use routing to build your project.
  - Style your project using Angular Material or custom CSS.

### Resources
- **Official Angular Documentation:** https://angular.io/docs
- **Angular CLI Documentation:** https://angular.io/cli
- **Angular Material:** https://material.angular.io/

---

### Day 1: Introduction to Angular (Detailed)

#### Objective:
Understand what Angular is and set up the development environment.

#### Tasks:

1. **Read About Angular and Its Features**
   - **What is Angular?**
     - Angular is a platform and framework for building single-page client applications using HTML and TypeScript. It is developed and maintained by Google.
     - Angular provides features like two-way data binding, dependency injection, modular development, and a robust CLI (Command Line Interface).

2. **Install Node.js and npm**
   - **Node.js** is a JavaScript runtime built on Chrome's V8 JavaScript engine.
   - **npm** (Node Package Manager) is a package manager for JavaScript and the default package manager for Node.js.
   - **To install Node.js and npm:**
     - Visit the [Node.js website](https://nodejs.org/).
     - Download the LTS (Long Term Support) version for your operating system.
     - Follow the installation instructions specific to your OS.
   - **Verify Installation:**
     - Open your terminal (Command Prompt, PowerShell, Terminal, etc.) and run:
       ```sh
       node -v
       ```
       - This command displays the installed version of Node.js.
       ```sh
       npm -v
       ```
       - This command displays the installed version of npm.

3. **Install Angular CLI**
   - **What is Angular CLI?**
     - The Angular CLI (Command Line Interface) is a powerful tool that helps you create, build, and run Angular applications.
   - **Install Angular CLI:**
     - Open your terminal and run:
       ```sh
       npm install -g @angular/cli
       ```
     - **Explanation:**
       - `npm install`: This command installs a package.
       - `-g`: This flag stands for "global". It installs the package globally, making the Angular CLI available across your entire system rather than just in a single project directory.
       - `@angular/cli`: This specifies the package to install, which is the Angular CLI.
   - **Verify Installation:**
     - Run:
       ```sh
       ng version
       ```
     - You should see output that includes Angular CLI, Node.js, and other related package versions.

4. **Create Your First Angular App**
   - **Create a New Angular Application:**
     - In your terminal, run:
       ```sh
       ng new my-first-app
       ```
     - **Explanation:**
       - `ng new <app-name>`: This command generates a new Angular application with the specified name.
     - **Prompts:**
       - You will be prompted with a few questions:
         - Would you like to add Angular routing? (Type 'y' for yes or 'n' for no)
         - Which stylesheet format would you like to use? (Choose from CSS, SCSS, SASS, LESS, Stylus)
     - **Directory Structure:**
       - The Angular CLI creates a project with the following structure:
         ```
         my-first-app/
         ├── e2e/                # End-to-end tests
         ├── node_modules/       # Project dependencies
         ├── src/                # Application source code
         │   ├── app/            # Main application module and components
         │   ├── assets/         # Static assets like images
         │   ├── environments/   # Environment configuration files
         │   ├── index.html      # Main HTML file
         │   ├── main.ts         # Main entry point for the application
         │   └── styles.css      # Global styles
         ├── .gitignore          # Git ignore file
         ├── angular.json        # Angular CLI configuration
         ├── package.json        # Node.js package configuration
         └── README.md           # Project README file
         ```

5. **Serve the Application**
   - **Navigate to the Application Directory:**
     - Change directory to your new Angular application:
       ```sh
       cd my-first-app
       ```
   - **Serve the Application:**
     - Use the Angular CLI to build and serve your application:
       ```sh
       ng serve
       ```
     - **Explanation:**
       - `ng serve`: This command builds your application and starts a web server. It watches for file changes and rebuilds the application automatically.
     - **Access the Application:**
       - Open a web browser and go to `http://localhost:4200`. You should see the default Angular welcome page.

#### Additional Explanation:

- **Angular CLI Commands:**
  - `ng new <app-name>`: Creates a new Angular application with the specified name.
  - `ng serve`: Builds and serves the application, watching for file changes.

- **Project Structure:**
  - **`src/app/`**: This folder contains the main application module and components.
    - **`app.module.ts`**: The root module of the application.
    - **`app.component.ts`**: The root component of the application.
    - **`app.component.html`**: The template (HTML) for the root component.
    - **`app.component.css`**: The styles for the root component.
  - **`angular.json`**: Configuration file for Angular CLI.
  - **`package.json`**: Lists the project's dependencies and scripts.

### Summary
On Day 1, you've learned about Angular, set up your development environment, created your first Angular app, and served it locally. You now have a basic understanding of Angular and the tools needed to start building applications.
