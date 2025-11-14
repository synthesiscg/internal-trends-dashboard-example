## Trends – Cyber Coverage Intelligence (Streamlit)

### Overview
Trends is a Streamlit-based dashboard for exploring recent cyber coverage patterns. It provides:
- Visual Dashboard: heatmaps, timelines, sector rankings, geography, and cost views
- Insights: curated incidents, attack types, seasonal timing, and emerging narratives
- Chat (simulated): quick Q&A backed by mock categories

Data in this repo is mock/prototype content to demonstrate layout and UX; there is no live data pipeline in this project.

### Quickstart
```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
streamlit run main_app.py
```
Then open the URL shown in your terminal (typically http://localhost:8501).

### Requirements
- Python 3.10+ recommended
- See `requirements.txt` for pinned dependencies:
  - streamlit, plotly, pandas, pyarrow, numpy

### Project Structure
- `main_app.py`: Streamlit app entrypoint (tabs: Visual Dashboard, Insights, Chat)
- `mock_data.py`: mock market intelligence and insights
- `cyber_mocup_data_new.py`: visual dashboard layout and design system
- `cyber_mockup_data.py` / `cyber_mockup_data_old.py`: legacy/alternate mock datasets
- `ui_components.py`: small Plotly helper utilities

### How to Run
- Development server:
  ```bash
  streamlit run main_app.py
  ```
- Stop with Ctrl+C.

### Configuration
No configuration is required for the prototype. The app uses mock data and does not read environment variables.

If you later wire this to real data sources, add a `config/` module (e.g., `config/config.py`) for environment-variable loading and import that across scripts for consistency. Keep configurable parameters out of code where possible.

### Notes on Data
- All figures, incidents, and metrics are illustrative for UX design and demo purposes.
- Currency ranges and coverage counts are mock values intended to reflect realistic shapes and scales.

### Troubleshooting
- If Streamlit fails to start, ensure your virtual environment is active and `pip install -r requirements.txt` completed without errors.
- For plotting issues, verify your browser allows WebGL and that Plotly is installed at the version pinned in `requirements.txt`.

### License
Internal prototype. Add an explicit license if sharing externally.


