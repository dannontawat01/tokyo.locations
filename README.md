# Tokyo Trip Log 🇯🇵

A modern, responsive web application designed to help you curate, explore, and track locations for your Tokyo trip. Featuring a sleek neon-aesthetic design, this app allows you to browse restaurants, shops, and sightseeing spots with ease.

## ✨ Features

- **Dynamic Data Loading**: Fetches location data directly from a Google Sheet (CSV), ensuring your list is always up to date.
- **Smart Caching**: Implements a "stale-while-revalidate" strategy. The app loads instantly from local storage and updates with fresh data from the cloud in the background.
- **Responsive Design**:
  - **Desktop**: A comprehensive table view for detailed planning.
  - **Mobile**: A beautiful, touch-friendly card view with glassmorphism effects.
- **Powerful Search & Filter**:
  - Real-time search by name, type, or area.
  - Multi-select dropdowns for **Areas** and **Types**.
  - **Favorites** filter to quickly see your top picks.
- **Local Customization**:
  - **Edit & Delete**: Modify details or remove locations (changes are persisted locally).
  - **Favorites**: Mark spots as favorites to highlight them.
- **Navigation**: One-click integration with **Google Maps** for easy navigation.

## 🛠️ Technologies Used

- **HTML5**: Semantic structure.
- **Tailwind CSS**: Utility-first styling for a custom, responsive design (loaded via CDN).
- **JavaScript (ES6+)**: Core logic for data fetching, filtering, and DOM manipulation.
- **PapaParse**: Robust CSV parsing library.
- **Google Fonts**: Uses 'Inter' for UI text and 'Kanit' for a modern touch.

## 🚀 Getting Started

### Prerequisites
You just need a modern web browser (Chrome, Edge, Firefox, Safari).

### Installation
1. **Clone the repository** or download the files.
   ```bash
   git clone <repository-url>
   ```
2. **Open the App**:
   - **Recommended**: Open `index.html` using a local development server (like "Live Server" in VS Code) to avoid CORS issues.
   - **Direct File**: You can double-click `index.html`, but data fetching might be restricted by browser security policies.

## ⚙️ Configuration (Google Sheet)

This app is designed to read data from a public Google Sheet.

1. **Prepare your Google Sheet**:
   Create a sheet with the following header columns:
   - `id`: A unique number for the location.
   - `name`: Name of the location.
   - `type`: Category (e.g., Food, Shopping, Sightseeing, Cafe).
   - `area`: District (e.g., Shibuya, Shinjuku, Asakusa).
   - `time`: Opening hours (e.g., "10:00 - 22:00").
   - `favorite`: Set to `1` for favorite, `0` otherwise.

2. **Publish as CSV**:
   - In Google Sheets, go to **File** > **Share** > **Publish to web**.
   - Select the specific sheet tab.
   - Choose **Comma-separated values (.csv)** as the format.
   - Click **Publish** and copy the link.

3. **Connect to App**:
   - Open the app.
   - Click the **Settings** (gear icon or similar, if implemented) or look for the "Open Google Sheet" / "Settings" modal trigger.
   - Paste your CSV URL into the **Google Sheet CSV URL** field.
   - Click **Save & Refresh Data**.

## 🎨 Design System

The UI is built with a "Tokyo Night" theme:
- **Background**: Deep Navy (`#0B1120`)
- **Surface**: Glassy Blue-Grey (`#151F32`)
- **Accent**: Teal/Cyan (`#2DD4BF`) for primary actions and highlights.
- **Status Colors**:
  - 🟠 Food: Orange
  - 🌸 Cafe: Pink
  - 🔵 Shopping: Blue
  - 🟢 Sightseeing: Emerald

---

*Happy Travels!* ✈️
