# AI-powered-Summarize-Assistant Chrome Extension 🚀

A Chrome extension that provides AI-powered summarization using the **Gemini API** for text processing and **Spring Boot** as the backend.

## 📌 Features
- Summarizes webpage content using **AI (Gemini API)**.
- Chrome extension UI for user interaction.
- Backend built with **Spring Boot**.
- Supports summarization of selected text or full pages.
- Fast and efficient API communication.

## 🏗️ Tech Stack
- **Frontend:** Chrome Extension (JavaScript, HTML, CSS)
- **Backend:** Spring Boot
- **AI Model:** Gemini API
- **Database:** (Optional, if storing summaries)

## Setup and Installation

### 1. Spring Boot Backend

1.  **Clone the Repository:**
    ```bash
    git clone <your-repository-url>
    cd spring-boot-backend
    ```
2.  **Configure Gemini API:**
    * Create a `application.properties` file in `src/main/resources/`.
    * Add your Google Cloud API key:
        ```properties
        gemini.api.key=<your-gemini-api-key>
        ```
    * Add the Gemini model name you want to use.
        ```properties
        gemini.model=gemini-pro
        ```
3.  **Build and Run the Application:**
    ```bash
    mvn clean install
    mvn spring-boot:run
    ```
    The Spring Boot application should now be running on `http://localhost:8080`.

### 2. Chrome Extension

1.  **Load the Extension:**
    * Open Chrome and go to `chrome://extensions/`.
    * Enable "Developer mode" in the top right corner.
    * Click "Load unpacked" and select the `chrome-extension` directory.
2.  **Configure the Backend URL:**
    * Open `popup.js` in the `chrome-extension` directory.
    * Modify the `backendUrl` variable to match the URL of your Spring Boot backend (e.g., `http://localhost:8080/summarize`).
3.  **Using the extension:**
    * Navigate to any webpage.
    * click on the extension icon.
    * click the summarize button.
    * The extension will send the page content to your spring boot backend, which will then send it to the gemini api, and then display the results.


