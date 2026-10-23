# Smart Hostel Room Allocation System

A responsive, browser-based hostel management demo that helps manage students, hostel rooms, room allocation, waiting lists, and activity history. The project is built using **HTML, CSS, and JavaScript in a single `index.html` file**.

> **Note:** This is an academic demonstration project. It uses browser `localStorage` and is not intended for real hostel operations or storage of sensitive student information.

## Features

- **Dashboard:** View summary statistics for students, rooms, occupied beds, available beds, and students waiting for allocation.
- **Student management:** Add students, search records, remove records, and check students out.
- **Room management:** Add rooms, define room capacity and room type, and remove rooms when appropriate.
- **Automatic room allocation:** Assign eligible students to available rooms using a priority queue.
- **Priority scoring:** Prioritize allocation using the student's recorded priority information.
- **Waiting list:** Keep students waiting when no suitable bed is available and process the list when capacity becomes available.
- **Room transfer:** Move a student to another suitable room when space is available.
- **Roommate compatibility:** Use recorded preferences such as room type, sleep schedule, and roommate preference as a simple compatibility aid.
- **Activity history:** Display important actions performed in the demo.
- **Undo:** Restore a previous application state for supported changes.
- **Reports and exports:** Export application data as JSON or CSV.
- **Persistent browser storage:** Save the demo's state in `localStorage`.
- **Sample data:** Start with example students and rooms to explore the interface.
- **Responsive interface:** Usable on desktop and smaller screens.

## Technologies Used

- **HTML5** — page structure
- **CSS3** — layout, styling, and responsive design
- **JavaScript** — application logic and interactions
- **Data structures and algorithms:**
  - Array-based records for students and rooms
  - **Max-heap / priority queue** for priority-based allocation
  - **Stack-like history snapshots** to support undo
  - Searching and filtering for finding student records
- **Browser APIs:** `localStorage`, Blob/object URLs, and file downloads for data persistence and export

## How to Run

No installation or server is required.

1. Download or clone this repository.
2. Open `index.html` in a modern browser such as Chrome, Edge, or Opera.
3. Explore the sample data, add students or rooms, and try the allocation and export features.

## GitHub Pages Deployment

1. Create a GitHub repository named `Smart-Hostel-Room-Allocation-System`.
2. Upload `index.html` and `README.md` to the repository's root.
3. Open **Settings → Pages**.
4. Under the build/deployment section, select **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.
6. Wait for GitHub Pages to publish the site. The repository's Pages section will show the published URL.

## Suggested Repository Structure

```text
Smart-Hostel-Room-Allocation-System/
├── index.html
└── README.md
```

All styling and JavaScript are embedded in `index.html`, so separate `style.css` or `script.js` files are not needed.

## Data Structures Used

### 1. Max-Heap / Priority Queue
Students can be considered in priority order during automatic allocation. A heap supports retrieving the highest-priority entry efficiently compared with sorting the entire list for every retrieval.

### 2. Arrays
Student and room records are stored in JavaScript arrays, making it straightforward to add, remove, search, and update records.

### 3. Stack-like Undo History
Snapshots of earlier application states are stored so supported changes can be undone in reverse order.

## Limitations

- This is a front-end demonstration and does not use a backend database or user authentication.
- Data is stored in the current browser's `localStorage`; it is not automatically shared between devices or users.
- Compatibility and priority scores are simplified demo rules and should not be treated as authoritative decisions.
- Do not enter real sensitive personal information.
- A production version would need a secure backend, authentication, access controls, validation, backups, and privacy safeguards.

## Author

**Shine CK**

## License

This project is provided for educational and demonstration purposes. Add a license file if you want to distribute it under a specific open-source license.
