Here is the complete content for your `README.md` file. You can copy and paste this directly into your file on GitHub or in your code editor.

````markdown
# City Explorer

A responsive web application built with **Node.js**, **Vite**, and **Vue 3**. It displays live weather forecasts, quality of life scores, and city information using a robust hybrid API strategy (Open-Meteo + Teleport + Wikipedia).

## 📋 Prerequisites

Before you begin, ensure you have the following installed on your computer:

1.  **Node.js** (Version 18 or higher recommended)
      * [Download Node.js here](https://nodejs.org/)
      * To check if installed, type `node -v` in your terminal.
2.  **Git**
      * [Download Git here](https://git-scm.com/)
      * To check if installed, type `git --version` in your terminal.

## 🚀 Installation & Local Development

Follow these steps to run the app on your local machine:

### 1. Clone the Repository

Open your terminal or command prompt and run:

```bash
git clone [https://github.com/gestaacinc/madel_cityExplorer.git](https://github.com/gestaacinc/madel_cityExplorer.git)
cd madel_cityExplorer
````

### 2\. Install Dependencies

This command installs all the necessary libraries (Vue, Tailwind, Vite, etc.) listed in `package.json`.

```bash
npm install
```

### 3\. Run the Development Server

Start the app in development mode with hot-reloading (changes update instantly):

```bash
npm run dev
```

> **Output:** You will see a local URL (usually `http://localhost:5173`). Open this link in your browser to view the app.

-----

## 📦 Building & Deployment

This project is configured for **GitHub Pages**.

### Live Demo

**[https://gestaacinc.github.io/madel\_cityExplorer/](https://www.google.com/search?q=https://gestaacinc.github.io/madel_cityExplorer/)**

### How to Deploy Updates

If you make changes to the code and want to update the live site, follow this **manual deployment** process:

1.  **Build the Project**
    This creates a `dist` folder containing the optimized production files.

    ```bash
    npm run build
    ```

2.  **Push to GitHub Pages**
    This command pushes *only* the `dist` folder to the `gh-pages` branch, which GitHub uses to host the site.

    ```bash
    git add dist -f
    git commit -m "Deploying updates"
    git subtree push --prefix dist origin gh-pages
    ```

-----

## 🛠️ Project Structure

  * **`src/App.vue`**: The main application logic, template, and styles.
  * **`src/main.js`**: The entry point that initializes Vue.
  * **`vite.config.js`**: Configuration for the build tool and base URL path.
  * **`tailwind.config.js`**: Configuration for the Tailwind CSS framework.

## 🌐 API Reference

This application uses a **Hybrid Data Strategy** to ensure reliability. It requires **NO API Keys**.

1.  **Open-Meteo API**:
      * *Purpose*: Provides Geocoding (Search) and Live Weather data.
      * *Status*: Primary, highly reliable.
2.  **Teleport API**:
      * *Purpose*: Provides "Quality of Life" scores and curated urban images.
      * *Status*: Secondary. If down, the app switches to "Basic Mode".
3.  **Wikipedia API**:
      * *Purpose*: Provides city images and "Popular Places" lists.
      * *Status*: Backup. Used automatically if Teleport is unavailable.
4.  **CorsProxy / AllOrigins**:
      * *Purpose*: Middleware used to bypass browser CORS security restrictions for external APIs.

-----

*Developed by: Madel Sison*

```
```