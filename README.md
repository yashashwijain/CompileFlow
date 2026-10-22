# CompileFlow

**CompileFlow** is an interactive web platform for exploring compiler design concepts through visualizations and hands-on tools.

## Features

### Regex-to-Automata Playground
- Explore direct DFA construction using the followpos method.
- Compare it with Thompson's construction and subset construction.
- View state counts and construction-time comparisons.

### Grammar Analysis Tool
- Calculate FIRST and FOLLOW sets.
- Generate LL(1) parsing tables.
- Identify conflicts in grammar analysis.

### DFA Minimizer
- Visualize DFA minimization using partition refinement.
- Compare original and minimized automata.

### Compiler Pipeline
- Explore six compiler phases: lexical analysis, parsing, semantic analysis, intermediate code generation, optimization, and code generation.
- Use the Monaco editor, code presets, and inline error highlighting.
- Inspect compilation results through the pipeline dashboard.

## Technology Stack

- **Frontend:** React, Vite, Tailwind CSS, Monaco Editor
- **Backend:** Python, FastAPI
- **Testing:** Pytest

## Project Structure

```text
backend/    FastAPI backend, automata engines, grammar tools,
            and compiler pipeline
frontend/   React frontend and interactive tools
docs/       Architecture notes, roadmap, deployment guide,
            and screenshots
```

## Getting Started

### Prerequisites

- Python 3.12 recommended
- Node.js and npm

### Backend Setup

From the repository root:

```bash
cd backend
python -m venv .venv
```

Activate the environment.

**Windows PowerShell:**

```powershell
.\.venv\Scripts\Activate.ps1
```

**macOS/Linux:**

```bash
source .venv/bin/activate
```

Install dependencies and start the backend:

```bash
pip install -r requirements.txt
uvicorn app.main:app --reload
```

Backend API: `http://localhost:8000`

API documentation: `http://localhost:8000/docs`

### Frontend Setup

Open a second terminal from the repository root:

```bash
cd frontend
npm install
npm run dev
```

Open `http://localhost:5173` in your browser.

The frontend uses `VITE_API_BASE_URL` to configure the backend URL. If it is not set, the API client defaults to `http://localhost:8000`.

## Running Tests

```bash
cd backend
pytest -v
```

## Screenshots

Application screenshots are available in [`docs/screenshots/`](docs/screenshots/).

## Development

CompileFlow is maintained by **Yashashwi Jain and Nitin Giri**.

Development work should be done on separate branches and submitted through pull requests for review before merging into `main`.

## License

See [LICENSE](LICENSE) for the applicable license terms.
