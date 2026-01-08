## 🚗 Car Rental Web Application
📓 <a href="https://github.com/cdsouza2701/car-rental-web-app.git" target="_blank" rel="noopener noreferrer">View Project Code</a>
 | 🌐 <a href="https://cdsouza2701.github.io/car-rental-web-app/" target="_blank" rel="noopener noreferrer">Live Demo </a>

**Project description:** This project focuses on designing and implementing a front-end car rental website using HTML, CSS, and JavaScript. The goal was to build a multi-page web application that allows users to browse available cars, select rental details, and view dynamically calculated pricing using client-side logic.

The project serves as an introduction to front-end web development concepts, including page navigation, DOM manipulation, and handling user input via URL parameters.

### 1. The objective of this project was to:

- Build a structured, multi-page website

- Enable users to select rental duration and car details

- Dynamically calculate rental prices on the client side

- Display user-specific information consistently across pages

### 2. Application Structure & Data Flow

**Application Type:** Front-end web application

**Pages Included:**

- Home

- Cars listing

- About

- Return

- Contact

**Data Handling:**

- User inputs (name, rental days, car ID, price per day) are passed between pages using URL query parameters

- JavaScript extracts these parameters and dynamically updates the page content

### 3. Methodology

**Page Structure:**
Built multiple HTML pages with shared navigation and consistent layout styling.

**Client-Side Logic:**
Used JavaScript to:

- Read URL parameters using URLSearchParams

- Perform price calculations based on rental duration

- Inject dynamic values into the DOM

**Styling:**
Applied custom CSS to maintain a unified visual design across all pages.

**Navigation Flow:**
Ensured users can move seamlessly between pages while preserving relevant rental information.

### 4. Tools & Technologies

- HTML5

- CSS3

- JavaScript (ES6)

- DOM Manipulation

- URL Parameters (URLSearchParams)

### 5. Key Learnings

- How client-side JavaScript can manage dynamic content without a backend

- How to pass and retrieve data between pages using URL parameters

- How to manipulate the DOM to display calculated values

- How to structure a multi-page web application

- Importance of separating structure (HTML), styling (CSS), and logic (JavaScript)

### 6. Limitations

- No backend or database integration

- Data is not persisted beyond the browser session

- No form validation or error handling for invalid user input

- Pricing logic is client-side only and not secure for production use

### 7. Future Improvements

- Introduce backend logic and database storage

- Add form validation and error handling

- Improve accessibility and responsive design

- Refactor into a modern framework such as React

- Implement secure state management instead of URL parameters

### 7. Academic Context
This project was developed as part of a university coursework to practice foundational web development concepts. It represents an early-stage project focused on understanding how front-end applications function before introducing backend technologies or frameworks.

