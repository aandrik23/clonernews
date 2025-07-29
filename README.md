# Hacker News UI

## A modern, responsive web interface to browse Hacker News posts with real-time updates and enhanced usability.

## Authors
	•	Aandriko
	•	Cemvalot
	•	Ychaniot


## Features
	•	Post Types: Stories, Jobs, Polls (with visual labels)
	•	Categories: Top, New, Best, Ask HN, Show HN, Jobs, Polls
	•	Pagination: Load more posts on demand (20 posts per page)
	•	Post Modal: View full post details and comments
	•	Nested Comments: Expand/collapse threaded replies
	•	Live Updates: Sidebar updates with new posts every 5 seconds
	•	Responsive: Optimized for desktop and mobile
	•	Keyboard Support: ESC closes modal
	•	Rate Limiting: 200ms between API requests, 5-second live update throttle


## Project Structure
```bash
clonernews/
├── index.html       # Main HTML file
├── styles.css       # Styling
├── app.js           # JavaScript logic
└── README.md        # This documentation
```
### Getting Started

### Prerequisites
	•	Modern browser (Chrome, Firefox, Edge, Safari)
	•	Optional: local server for better API compatibility

### Installation
	1.	Clone the repository or download the source
	2.	Run a local server in the project directory, e.g.:
  ```bash
  python -m http.server 8000
  ```
  3.	Open http://localhost:8000 in your browser

### Usage
	•	Click tabs to switch categories
	•	Click a post to open details and comments in modal
	•	Use “Load More” to fetch more posts
	•	Monitor live updates in sidebar, click to open posts
	•	Expand comments and their nested replies interactively


## API Endpoints Used
	•	/topstories.json
	•	/newstories.json
	•	/beststories.json
	•	/askstories.json
	•	/showstories.json
	•	/jobstories.json
	•	/item/{id}.json


## Configuration
	•	POSTS_PER_PAGE (default 20) configurable in app.js
	•	Live update frequency: every 5 seconds (change in startLiveUpdates())


## Troubleshooting
	•	No posts? Check console/network for errors
	•	Live updates not showing? Wait 5 seconds and confirm internet/API access
	•	Polls may be rare; the app fetches from top stories to find polls
	•	Modal doesn’t open? Verify JavaScript enabled and no conflicts
