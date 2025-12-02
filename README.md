FitCRM – Simple Client Manager for a Fitness Program
This is a Frontend-only client relationship management (CRM) application designed specifically for fitness instructors, personal trainers, and small gym owners. It provides a lightweight, browser-based tool to manage client information and track fitness goals using HTML, CSS, and JavaScript.

Features
FitCRM implements a three-page structure with data persistence using the browser's localStorage and integration with an external API for workout suggestions.

Page 1: New Client Form (client-form.html)
Add Client: Allows input of client details (Name, Email, Phone, Goal, Start Date, History).

Data Persistence: Saves all client information directly to the browser's localStorage.

Form Validation: Basic HTML5 validation ensures required fields (e.g., Name, Email) are completed and the email format is correct.

Edit Client: The same form is repurposed to repopulate existing client data when accessed via the "Edit" button from the Client List.

Page 2: Client List View (client-list.html)
Display: Renders a dynamic table listing all clients retrieved from localStorage.

Search: Implements a search function to filter the client list by Client Name.

Delete: Removes a client permanently from the list and localStorage, requiring a confirmation prompt before execution.

Edit: Redirects to the client-form.html with the client's unique ID to enable data update.

View: Clicking anywhere on a client's row (excluding action buttons) redirects to the dedicated Client View page.

Page 3: Client View (client-view.html)
Details Display: Shows all stored client information, including Name, Email, Phone, Fitness Goal, Membership Start Date, and Training History.

API Integration: Fetches suggested exercises for the next session by integrating with the Wger REST API. It grabs 5 exercises relevant to the client's primary fitness goal.

Technology Stack
HTML5: Structure

CSS3: Styling and Responsive Design

JavaScript (ES6+): Core application logic, DOM manipulation, data management.

Local Storage API: Data Persistence.

Wger API: External REST API used for workout suggestions.

File Structure
The project follows a clean, modular structure:

fitcrm/
├── index.html                  (Homepage)
├── client-form.html            (Add/Edit Client Form)
├── client-list.html            (Client Directory/List)
├── client-view.html            (Single Client Details)
├── css/
│   └── styles.css              (All application styling, including responsive design)
└── js/
    └── main.js                 (All JavaScript logic: Data CRUD, API calls, DOM rendering)
