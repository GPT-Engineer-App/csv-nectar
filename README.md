# csv-nectar

App Description

This application is a CSV file uploader and viewer with data enrichment capabilities. It consists of two main pages: a Home page (Index) with the CSV uploader and a Scanned Data page.

Home Page (CSV Uploader):

	•	Users can upload a CSV file using a file input.
	•	The app displays file statistics including total rows, total columns, file size, and total pages.
	•	The uploaded CSV data is displayed in a paginated table.
	•	Each row in the table has an “Enrich” button.
	•	Users can navigate through pages of the CSV data.
	•	The app remembers the last uploaded file name using local storage.
	•	Users can clear the stored data and upload a new file.

Scanned Data Page:

	•	This page displays a simple table with sample data.
	•	It also includes an “Enrich” button for the sample data row.

Common Features:

	•	Both pages have an “Enrich” button for each row of data.
	•	When clicked, the “Enrich” button changes to “Enriched” and becomes disabled.
	•	On the Home page, a toast notification appears when a row is enriched.

Navigation:

	•	The app uses a navbar layout, allowing users to switch between the Home and Scanned Data pages.

Key Functionalities:

CSV File Handling:

	•	Reads and parses CSV files.
	•	Displays CSV data in a paginated table.
	•	Stores file reference for continued processing across page changes.

Data Enrichment:

	•	Provides a mechanism to “enrich” individual rows of data.
	•	Currently, the enrichment is a placeholder function that only updates the UI state.

User Interface:

	•	Responsive design using Tailwind CSS.
	•	Uses shadcn/ui components for a consistent look and feel.
	•	Provides feedback through toast notifications.

State Management:

	•	Uses React’s useState and useEffect hooks for local state management.
	•	Implements pagination for large datasets.

Error Handling:

	•	Basic error handling for file reading and processing.

It’s important to note that while the structure for data enrichment is in place, the actual enrichment logic is not implemented. This is currently a placeholder for future functionality where you might want to add specific data processing or API calls to enrich the data.

The app provides a foundation for a data processing tool, particularly useful for scenarios where CSV data needs to be uploaded, viewed, and potentially enhanced or processed in some way.

New Feature Request: Data Enrichment via Anthropic Claude API

We need to add a new feature to our internal tool that allows us to enrich CSV data by querying the Anthropic Claude API. Here are the detailed requirements for this feature:

	1.	API Key Usage:
	•	The app will use a local API key to authenticate requests to the Anthropic Claude API. This key will be stored securely within the application.
	2.	Data Enrichment:
	•	For each row in the uploaded CSV, the app will send a request to the Anthropic Claude API. The request will include data from the row, specifically location information.
	•	The query will ask the Anthropic Claude API to provide a brief and informative description of the location based on the provided data.
	3.	Response Handling:
	•	The app will capture the response from the Anthropic Claude API and update the corresponding row in the CSV table with the description received from the API.
	•	Each row will have an “Enrich” button. When clicked, this button will initiate the API request, update the row with the response, and then change to “Enriched” and become disabled.
	4.	Progress Tracking:
	•	The app will include a progress bar to show the user the progress of the enrichment process across all rows in the CSV.
	•	The progress bar will update in real-time as each row is enriched.
	5.	Caching and Persistence:
	•	To ensure data is not lost between sessions and to avoid redundant API calls, the app will cache the enriched data locally.
	•	This will involve saving the state of the enriched rows to local storage after each successful API response.
	6.	Error Handling:
	•	The app will handle errors gracefully, providing feedback to the user if an API request fails.
	•	It will allow the user to retry the enrichment process for rows that encounter errors.

## Collaborate with GPT Engineer

This is a [gptengineer.app](https://gptengineer.app)-synced repository 🌟🤖

Changes made via gptengineer.app will be committed to this repo.

If you clone this repo and push changes, you will have them reflected in the GPT Engineer UI.

## Tech stack

This project is built with .

- Vite
- React
- shadcn-ui
- Tailwind CSS

## Setup

```sh
git clone https://github.com/GPT-Engineer-App/csv-nectar.git
cd csv-nectar
npm i
```

```sh
npm run dev
```

This will run a dev server with auto reloading and an instant preview.

## Requirements

- Node.js & npm - [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating)
