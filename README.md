# Flask Cafe Review App

This project is a simple Flask application where users can:
- Submit details about cafes, including location, opening/closing times, and ratings for coffee, WiFi, and power availability.
- View a list of all submitted cafes.

---

## Features
- **Form Submission**: Add details about cafes using a web form.
- **CSV Storage**: Save submitted data to a CSV file for persistence.
- **Bootstrap Integration**: Styled with Bootstrap for responsive and modern UI.
- **Data Viewing**: Display all submitted cafes in a user-friendly table.

---

## Installation

### Prerequisites
- Python 3.7+
- Pip (Python package manager)

### Clone the Repository
```bash
git clone <repository-url>
cd <repository-folder>
```

### Set Up a Virtual Environment (Optional but Recommended)
```bash
python -m venv venv
source venv/bin/activate  # On macOS/Linux
venv\Scripts\activate   # On Windows
```

### Install Dependencies
Install required packages by running:
```bash
pip install -r requirements.txt
```

If you're using macOS, you may need to use:
```bash
pip3 install -r requirements.txt
```

---

## Application Structure
```
.
├── app.py              # Main application file
├── templates/          # HTML templates
│   ├── index.html
│   ├── add.html
│   ├── cafes.html
├── static/             # Static files (CSS, JS, images)
├── cafe-data.csv       # CSV file storing cafe data
├── requirements.txt    # Required Python packages
└── README.md           # Project documentation
```

---

## Running the Application
To start the Flask server, run:
```bash
python app.py
```

The application will be available at: [http://127.0.0.1:5002](http://127.0.0.1:5002)

---

## Usage

### Add a Cafe
1. Navigate to `/add`.
2. Fill out the form with details about the cafe:
   - **Cafe name**: The name of the cafe.
   - **Location**: A Google Maps URL of the cafe's location.
   - **Opening/Closing Times**: When the cafe opens and closes.
   - **Coffee Rating**: Rate the quality of coffee (1-5 cups).
   - **WiFi Strength Rating**: Rate the strength of the WiFi (1-5 bars).
   - **Power Availability**: Rate the availability of power outlets (1-5 plugs).
3. Click "Submit" to save the data.

### View Cafes
1. Navigate to `/cafes`.
2. View a list of all cafes in a table format, with their details.

---

## Code Overview

### `CafeForm`
Defines the form for adding cafes, including:
- **Fields**:
  - `cafe`: Cafe name.
  - `location`: Google Maps URL.
  - `open`/`close`: Opening and closing times.
  - `coffee_rating`, `wifi_rating`, `power_rating`: Ratings for coffee, WiFi, and power.
  - `submit`: Submit button.

### Routes
- **`/`**:
  - Renders the home page (`index.html`).

- **`/add`**:
  - Renders the form for adding cafes (`add.html`).
  - Saves valid submissions to `cafe-data.csv`.

- **`/cafes`**:
  - Reads and displays cafe data from `cafe-data.csv` in a table (`cafes.html`).

---

## Required Packages
The application uses the following Python packages:
- `Flask`
- `Flask-WTF`
- `WTForms`
- `Flask-Bootstrap`
- `csv`
- `validators` (e.g., `DataRequired`, `URL`)

These can be installed by running:
```bash
pip install -r requirements.txt
```
