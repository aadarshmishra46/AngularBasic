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

---

### Day 2: Angular Project Structure

#### Objective:
Learn the structure of an Angular project and understand the purpose of key files and folders.

#### Tasks:

1. **Explore the Angular Project Structure**
   - When you create a new Angular application using the Angular CLI, a specific project structure is generated. Understanding this structure is crucial for efficient development.

2. **Understand Key Files and Folders**

Let's explore the project structure of `my-first-app` created on Day 1:

```plaintext
my-first-app/
├── e2e/                # End-to-end tests
├── node_modules/       # Project dependencies
├── src/                # Application source code
│   ├── app/            # Main application module and components
│   ├── assets/         # Static assets like images
│   ├── environments/   # Environment configuration files
│   ├── index.html      # Main HTML file
│   ├── main.ts         # Main entry point for the application
│   ├── polyfills.ts    # Polyfills needed by Angular
│   ├── styles.css      # Global styles
│   └── test.ts         # Entry point for unit tests
├── .editorconfig       # Editor configuration
├── .gitignore          # Git ignore file
├── angular.json        # Angular CLI configuration
├── package.json        # Node.js package configuration
├── README.md           # Project README file
├── tsconfig.json       # TypeScript configuration
└── tslint.json         # TSLint configuration
```

3. **Detailed Explanation of Key Files and Folders**

- **`e2e/`**: This folder contains end-to-end tests for your application. These tests simulate user interactions and verify that the application behaves as expected.

- **`node_modules/`**: This folder contains all the npm packages installed for your project. These packages include Angular itself and other dependencies.

- **`src/`**: This is the main folder where you'll be spending most of your time. It contains the source code of your application.

  - **`app/`**: Contains the main application module and components.
    - **`app.module.ts`**: The root module of the application. It declares all the components, directives, and services used in the app.
    - **`app.component.ts`**: The root component of the application. It contains the logic and data for the main view.
    - **`app.component.html`**: The template (HTML) for the root component.
    - **`app.component.css`**: The styles for the root component.

  - **`assets/`**: This folder is for storing static assets like images, fonts, and other files. These assets can be accessed by your application.

  - **`environments/`**: This folder contains environment-specific configuration files. You can define different settings for different environments (e.g., development, production).

  - **`index.html`**: This is the main HTML file that gets served when someone visits your application. It contains the root element (`<app-root></app-root>`) where Angular will render your application.

  - **`main.ts`**: This is the main entry point for your application. It bootstraps the root module (`AppModule`) and starts the application.

  - **`polyfills.ts`**: This file includes polyfills needed by Angular to support older browsers.

  - **`styles.css`**: This file contains global styles for your application.

  - **`test.ts`**: This file is the entry point for unit tests. It sets up the Angular testing environment.

- **Configuration Files:**
  - **`.editorconfig`**: This file helps maintain consistent coding styles between different editors and IDEs.
  - **`.gitignore`**: This file specifies which files and folders should be ignored by Git.
  - **`angular.json`**: This file contains configuration options for Angular CLI. It defines how the application is built and served.
  - **`package.json`**: This file lists the project's dependencies and scripts. It also contains metadata about your project.
  - **`README.md`**: This file contains a brief description of the project and instructions on how to set it up.
  - **`tsconfig.json`**: This file contains TypeScript configuration options.
  - **`tslint.json`**: This file contains TSLint configuration options for linting your TypeScript code.

### Example: Modify and Understand `app.component`

1. **Open `src/app/app.component.ts`**:
   - This is the TypeScript file for the root component.

```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'my-first-app';
}
```

- **Explanation:**
  - `@Component`: This decorator defines the component. It specifies the selector, template, and styles.
  - `selector: 'app-root'`: This defines the custom HTML tag for the component.
  - `templateUrl: './app.component.html'`: This points to the HTML template for the component.
  - `styleUrls: ['./app.component.css']`: This points to the styles for the component.
  - `title = 'my-first-app'`: This defines a property `title` that is used in the template.

2. **Open `src/app/app.component.html`**:
   - This is the HTML template for the root component.

```html
<div style="text-align:center">
  <h1>
    Welcome to {{ title }}!
  </h1>
</div>
```

- **Explanation:**
  - `{{ title }}`: This is Angular's interpolation syntax. It binds the `title` property from the component class to the HTML.

3. **Modify the Component**:
   - Change the `title` property in `app.component.ts` to a different value:
     ```typescript
     title = 'My Angular App';
     ```
   - Update the HTML template to add more content:
     ```html
     <div style="text-align:center">
       <h1>
         Welcome to {{ title }}!
       </h1>
       <p>This is a basic Angular application.</p>
     </div>
     ```

4. **Serve the Application**:
   - Save your changes and run:
     ```sh
     ng serve
     ```
   - Open a web browser and go to `http://localhost:4200`. You should see the updated content.

### Summary
On Day 2, you've learned about the Angular project structure and the purpose of key files and folders. You've also modified the root component to understand how components work in Angular.

---
### Day 3: Components and Templates

#### Objective:
Learn about components and templates in Angular. Understand how to create and use components, and how to bind data to templates.

#### Tasks:

1. **Understand Components and Templates**

   - **Components**:
     - Components are the building blocks of an Angular application. Each component consists of:
       - A TypeScript class that contains data and logic.
       - An HTML template that defines the view.
       - Optional CSS styles that define the appearance of the view.

   - **Templates**:
     - Templates are used to define the view of a component. They contain HTML along with Angular-specific syntax for binding data and handling events.

2. **Create a New Component**

   - **Use Angular CLI to Generate a Component**:
     - Open your terminal and navigate to your Angular project directory (`my-first-app`).
     - Run the following command to generate a new component:
       ```sh
       ng generate component my-component
       ```
     - **Explanation**:
       - `ng generate component <component-name>`: This command generates a new component with the specified name. It creates four files:
         - `my-component.component.ts`: The TypeScript file for the component.
         - `my-component.component.html`: The HTML template for the component.
         - `my-component.component.css`: The CSS file for the component's styles.
         - `my-component.component.spec.ts`: The unit test file for the component.

3. **Understand the Component Decorator**

   - Open the generated `my-component.component.ts` file. It should look like this:

     ```typescript
     import { Component, OnInit } from '@angular/core';

     @Component({
       selector: 'app-my-component',
       templateUrl: './my-component.component.html',
       styleUrls: ['./my-component.component.css']
     })
     export class MyComponent implements OnInit {

       constructor() { }

       ngOnInit(): void {
       }

     }
     ```

   - **Explanation**:
     - `@Component`: This decorator marks the class as an Angular component and provides metadata about the component.
     - `selector`: Defines the custom HTML tag for the component.
     - `templateUrl`: Points to the HTML template for the component.
     - `styleUrls`: Points to the CSS file(s) for the component.

4. **Create a Simple Template and Use Data Binding**

   - **Open `my-component.component.ts`** and add a property:

     ```typescript
     export class MyComponent implements OnInit {
       message: string;

       constructor() {
         this.message = 'Hello from MyComponent!';
       }

       ngOnInit(): void {
       }
     }
     ```

   - **Explanation**:
     - `message: string`: This property holds the data that will be displayed in the template.
     - `this.message = 'Hello from MyComponent!'`: This initializes the `message` property.

   - **Open `my-component.component.html`** and use data binding to display the `message`:

     ```html
     <div>
       <p>{{ message }}</p>
     </div>
     ```

   - **Explanation**:
     - `{{ message }}`: This is Angular's interpolation syntax. It binds the `message` property from the component class to the HTML, displaying the value of `message`.

5. **Use the New Component in the Application**

   - **Open `app.component.html`** and include the new component using its selector:

     ```html
     <div style="text-align:center">
       <h1>
         Welcome to {{ title }}!
       </h1>
       <p>This is a basic Angular application.</p>
       <app-my-component></app-my-component> <!-- New component -->
     </div>
     ```

   - **Explanation**:
     - `<app-my-component></app-my-component>`: This is the custom HTML tag for the new component. Angular will render the template of `MyComponent` inside this tag.

6. **Serve the Application**

   - **Run the application**:
     ```sh
     ng serve
     ```
   - Open a web browser and go to `http://localhost:4200`. You should see the message from the new component displayed.

### Summary
On Day 3, you've learned about Angular components and templates. You've created a new component, understood the component decorator, used data binding in the template, and included the new component in the application.

---
### Day 3: Components and Templates

#### Objective:
Learn about components and templates in Angular. Understand how to create and use components, and how to bind data to templates.

#### Tasks:

1. **Understand Components and Templates**

   - **Components**:
     - Components are the building blocks of an Angular application. Each component consists of:
       - A TypeScript class that contains data and logic.
       - An HTML template that defines the view.
       - Optional CSS styles that define the appearance of the view.

   - **Templates**:
     - Templates are used to define the view of a component. They contain HTML along with Angular-specific syntax for binding data and handling events.

2. **Create a New Component**

   - **Use Angular CLI to Generate a Component**:
     - Open your terminal and navigate to your Angular project directory (`my-first-app`).
     - Run the following command to generate a new component:
       ```sh
       ng generate component my-component
       ```
     - **Explanation**:
       - `ng generate component <component-name>`: This command generates a new component with the specified name. It creates four files:
         - `my-component.component.ts`: The TypeScript file for the component.
         - `my-component.component.html`: The HTML template for the component.
         - `my-component.component.css`: The CSS file for the component's styles.
         - `my-component.component.spec.ts`: The unit test file for the component.

3. **Understand the Component Decorator**

   - Open the generated `my-component.component.ts` file. It should look like this:

     ```typescript
     import { Component, OnInit } from '@angular/core';

     @Component({
       selector: 'app-my-component',
       templateUrl: './my-component.component.html',
       styleUrls: ['./my-component.component.css']
     })
     export class MyComponent implements OnInit {

       constructor() { }

       ngOnInit(): void {
       }

     }
     ```

   - **Explanation**:
     - `@Component`: This decorator marks the class as an Angular component and provides metadata about the component.
     - `selector`: Defines the custom HTML tag for the component.
     - `templateUrl`: Points to the HTML template for the component.
     - `styleUrls`: Points to the CSS file(s) for the component.

4. **Create a Simple Template and Use Data Binding**

   - **Open `my-component.component.ts`** and add a property:

     ```typescript
     export class MyComponent implements OnInit {
       message: string;

       constructor() {
         this.message = 'Hello from MyComponent!';
       }

       ngOnInit(): void {
       }
     }
     ```

   - **Explanation**:
     - `message: string`: This property holds the data that will be displayed in the template.
     - `this.message = 'Hello from MyComponent!'`: This initializes the `message` property.

   - **Open `my-component.component.html`** and use data binding to display the `message`:

     ```html
     <div>
       <p>{{ message }}</p>
     </div>
     ```

   - **Explanation**:
     - `{{ message }}`: This is Angular's interpolation syntax. It binds the `message` property from the component class to the HTML, displaying the value of `message`.

5. **Use the New Component in the Application**

   - **Open `app.component.html`** and include the new component using its selector:

     ```html
     <div style="text-align:center">
       <h1>
         Welcome to {{ title }}!
       </h1>
       <p>This is a basic Angular application.</p>
       <app-my-component></app-my-component> <!-- New component -->
     </div>
     ```

   - **Explanation**:
     - `<app-my-component></app-my-component>`: This is the custom HTML tag for the new component. Angular will render the template of `MyComponent` inside this tag.

6. **Serve the Application**

   - **Run the application**:
     ```sh
     ng serve
     ```
   - Open a web browser and go to `http://localhost:4200`. You should see the message from the new component displayed.

### Summary
On Day 3, you've learned about Angular components and templates. You've created a new component, understood the component decorator, used data binding in the template, and included the new component in the application.

---

### Day 4: Directives in Angular

#### Objective:
Understand and use Angular directives. Learn about built-in directives and how to create your own custom directives.

#### Tasks:

1. **Introduction to Directives**

   - **What are Directives?**
     - Directives are classes in Angular that add behavior to elements in your Angular applications. They can modify the DOM (Document Object Model) or add additional functionality.

   - **Types of Directives:**
     - **Structural Directives**: Change the DOM layout by adding or removing elements. Examples include `*ngIf` and `*ngFor`.
     - **Attribute Directives**: Change the appearance or behavior of an element, component, or another directive. Examples include `ngClass` and `ngStyle`.

2. **Using Built-in Directives**

   - **`*ngIf` Directive:**
     - The `*ngIf` directive conditionally includes or excludes an element from the DOM based on a boolean expression.

     **Example:**
     - Open `app.component.html` and add the following code:

       ```html
       <div *ngIf="showMessage">
         <p>The message is visible!</p>
       </div>
       <button (click)="toggleMessage()">Toggle Message</button>
       ```

     - Open `app.component.ts` and add:

       ```typescript
       export class AppComponent {
         title = 'my-first-app';
         showMessage = true;

         toggleMessage() {
           this.showMessage = !this.showMessage;
         }
       }
       ```

     - **Explanation:**
       - `*ngIf="showMessage"`: The `div` is included in the DOM only if `showMessage` is `true`.
       - `(click)="toggleMessage()"`: The `toggleMessage()` method is called when the button is clicked, toggling the `showMessage` property.

   - **`*ngFor` Directive:**
     - The `*ngFor` directive is used to repeat an element for each item in a list.

     **Example:**
     - Open `app.component.html` and add the following code:

       ```html
       <ul>
         <li *ngFor="let item of items">{{ item }}</li>
       </ul>
       ```

     - Open `app.component.ts` and add:

       ```typescript
       export class AppComponent {
         title = 'my-first-app';
         items = ['Item 1', 'Item 2', 'Item 3'];
       }
       ```

     - **Explanation:**
       - `*ngFor="let item of items"`: Repeats the `li` element for each item in the `items` array.

   - **`ngClass` Directive:**
     - The `ngClass` directive adds or removes CSS classes based on conditions.

     **Example:**
     - Open `app.component.html` and add:

       ```html
       <div [ngClass]="{ 'highlight': isHighlighted }">
         This text will be highlighted based on the condition.
       </div>
       <button (click)="toggleHighlight()">Toggle Highlight</button>
       ```

     - Open `app.component.css` and add:

       ```css
       .highlight {
         background-color: yellow;
       }
       ```

     - Open `app.component.ts` and add:

       ```typescript
       export class AppComponent {
         title = 'my-first-app';
         isHighlighted = false;

         toggleHighlight() {
           this.isHighlighted = !this.isHighlighted;
         }
       }
       ```

     - **Explanation:**
       - `[ngClass]="{ 'highlight': isHighlighted }"`: Adds the `highlight` class if `isHighlighted` is `true`.

3. **Create a Custom Directive**

   - **Generate a New Directive:**
     - Use Angular CLI to generate a new directive:
       ```sh
       ng generate directive highlight
       ```

     - **Explanation**:
       - This creates a new directive called `HighlightDirective`.

   - **Implement the Directive:**
     - Open `highlight.directive.ts` and modify it as follows:

       ```typescript
       import { Directive, ElementRef, Renderer2, HostListener } from '@angular/core';

       @Directive({
         selector: '[appHighlight]'
       })
       export class HighlightDirective {
         constructor(private el: ElementRef, private renderer: Renderer2) { }

         @HostListener('mouseenter') onMouseEnter() {
           this.renderer.setStyle(this.el.nativeElement, 'backgroundColor', 'yellow');
         }

         @HostListener('mouseleave') onMouseLeave() {
           this.renderer.setStyle(this.el.nativeElement, 'backgroundColor', 'transparent');
         }
       }
       ```

     - **Explanation**:
       - `@Directive({ selector: '[appHighlight]' })`: Defines the directive with a selector `appHighlight`.
       - `ElementRef`: Allows access to the DOM element.
       - `Renderer2`: Provides a safe way to manipulate the DOM.
       - `@HostListener('mouseenter')`: Listens for the mouse enter event and changes the background color.
       - `@HostListener('mouseleave')`: Listens for the mouse leave event and resets the background color.

   - **Use the Custom Directive:**
     - Open `app.component.html` and use the directive:

       ```html
       <p appHighlight>Hover over this text to see the highlight effect.</p>
       ```

4. **Serve the Application**

   - **Run the application**:
     ```sh
     ng serve
     ```
   - Open a web browser and go to `http://localhost:4200`. You should see the results of the built-in directives and the custom directive in action.

### Summary
On Day 4, you've learned about Angular directives, including built-in directives like `*ngIf`, `*ngFor`, and `ngClass`, as well as how to create and use a custom directive. You’ve seen how directives can be used to manipulate the DOM and add dynamic behavior to your Angular application.

