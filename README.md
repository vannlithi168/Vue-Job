Here is a sample `README.md` file for your project. Feel free to customize it as needed:

```markdown
# Vue Job Board

A job listing platform built with Vue 3, Vite, TailwindCSS, and JSON Server to simulate a backend. This project allows users to view job listings, add new jobs, and more.

## Features

- **Job Listings**: View available job opportunities with details such as type, description, salary, and company information.
- **Add Jobs**: Add new job listings to the platform.
- **Mock API**: Using `json-server` to simulate a REST API with job data stored in a JSON file.
- **Toast Notifications**: Show notifications when a job is added successfully using `vue-toastification`.
- **Loading State**: Display a loading spinner when fetching job data.

## Technologies Used

- **Vue 3**: The front-end JavaScript framework used to build the user interface.
- **Vite**: A build tool for faster development and production bundling.
- **TailwindCSS**: A utility-first CSS framework for rapid UI development.
- **Vue Router**: For handling routing and navigation between pages.
- **Axios**: To make HTTP requests for fetching and posting job data.
- **JSON Server**: A fake REST API server for simulating a backend.
- **PrimeIcons**: A library for adding icons to the app.
- **Vue Spinner**: For displaying loading spinners.

## Setup

### Prerequisites

Make sure you have [Node.js](https://nodejs.org/) and [npm](https://www.npmjs.com/) installed.

### Clone the repository

```bash
git clone <repository-url>
cd vue-job-board
```

### Install dependencies

Run the following command to install all the required dependencies:

```bash
npm install
```

### Running the Development Server

To start the development server, run:

```bash
npm run dev
```

This will start the Vite dev server at `http://localhost:3000`, and you can view your project in the browser.

### Running the Mock API Server

To start the mock API server, run:

```bash
npm run server
```

This will start the `json-server` at `http://localhost:5000`, serving the data from `src/jobs2.json`.

### Building the Project

To build the project for production, run:

```bash
npm run build
```

### Previewing the Built Project

To preview the production build, run:

```bash
npm run preview
```

## Folder Structure

```
├── public/            # Static assets
├── src/
│   ├── assets/        # Static assets (images, fonts, etc.)
│   ├── components/    # Vue components
│   ├── router/        # Vue Router setup
│   ├── stores/        # Vue stores (if using Vuex or Pinia)
│   ├── views/         # Vue pages (views)
│   ├── jobs2.json     # Mock API data
│   ├── App.vue        # Main Vue component
│   └── main.js        # Vue app entry point
├── tailwind.config.js # Tailwind CSS configuration
├── vite.config.js     # Vite configuration
└── package.json       # Project metadata and dependencies
```

## Contributions

If you'd like to contribute to this project, feel free to fork the repository, make changes, and submit a pull request. Contributions are always welcome!

## License

This project is licensed under the MIT License.

```

### Explanation of the README Sections:

1. **Project Overview**: A description of what the project is about and its features.
2. **Technologies Used**: A list of key technologies used in the project.
3. **Setup**: Instructions on how to clone the repository, install dependencies, and run the development and mock API servers.
4. **Folder Structure**: An overview of the project's folder structure to help developers understand how the project is organized.
5. **Contributions**: A section to invite contributions from others.
6. **License**: The type of license the project is using, here it’s the MIT License. 

This README will help users understand how to set up and contribute to your Vue job board project.
