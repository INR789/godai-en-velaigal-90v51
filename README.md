# En Velaigal — என் வேலைகள்

A responsive Tamil task manager built with HTML, CSS and vanilla JavaScript. Includes email signup/login, account-private saved tasks, completion toggles, editing, confirmed deletion, optional due dates, priority, search, status filters and progress summaries.

## Hosting

Place `index.html`, `style.css`, and `app.js` at your GitHub Pages site root (or together in a subdirectory). Supply the platform-provided `godai-db.js` helper in the same directory. This helper is intentionally not included or reimplemented. It must export `GodDB` with the documented authentication and collection methods and be configured for the deployment origin. Enable GitHub Pages and open the deployed URL. For local testing, use an HTTP static server rather than a file:// URL.

## Accounts and storage

The app uses the supplied GodDB authentication service and the `en_velaigal_tasks` collection. Records contain `title`, `dueDate` (optional YYYY-MM-DD), `priority` (`normal` or `high`), and `completed`. Record IDs and creation timestamps are supplied by the service. User isolation must be enforced by the provided GodDB service; no custom backend is used. No credentials or tasks are stored in localStorage.

Signup may require email confirmation. Confirm the received email before signing in if required. An unavailable helper or service produces a visible Tamil error instead of presenting a fake login. Task-list loading failures offer a retry action; writes are reflected after successful persistence.

## Usage

Sign up or sign in, enter a task, optionally choose a due date and priority, and select சேர்க்க. Check a task to complete it. Use திருத்து to edit, நீக்கு to delete, and the filter buttons or search to find tasks. Sign out with வெளியேறு. Dates use the device's local date; overdue tasks are highlighted. Pending and high-priority tasks appear first.

No build tools, external fonts, API keys, or CDN dependencies are required. An internet connection and a functioning provided GodDB service are required for account and task operations.

GOD AI சோதனை வரி — தானியங்கி சோதனை வெற்றி
