# Indian Property Insurance Underwriting Tool

This Streamlit app helps property insurance underwriters assess risk at specific geographic locations across India.

## Latest Fix

* **Safe Coordinate Update**: Removed `st.experimental_rerun()` and implemented a guard-based session-state update for coordinates.
* Prevents infinite reruns and runtime errors.
* Provides clear user feedback when location is updated or unchanged.

## Features

* Interactive map centered on India with clickable property location selection
* Real-time elevation data via Open-Elevation API
* Flood risk classification based on elevation
* Urban flood risk zones for major Indian metros (Mumbai, Chennai, Kolkata, Delhi, Bengaluru)
* Fire brigade response time estimate based on sample fire stations in India
* Nearby properties exposure risk simulation
* Downloadable PDF report summarizing underwriting risk analysis

## Setup & Run

1. **Clone repository**:

   ```bash
   git clone https://github.com/yourusername/indian-property-insurance-tool.git
   cd indian-property-insurance-tool
   ```

2. **Install dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the app locally**:

   ```bash
   streamlit run app.py
   ```

## Deployment on Streamlit Cloud

1. Push changes to your GitHub repository.
2. Log in to [Streamlit Community Cloud](https://streamlit.io/cloud).
3. Create or select your app, set main file path to `app.py`, and deploy.
4. The app auto-rebuilds on new commits to the main branch.

## Notes

* The latest fix addresses coordinate updates without using `st.experimental_rerun()`.
* Ensure you’re using Streamlit version 1.12 or above.
* Replace sample flood zones and fire stations with official GIS data for production.

*Developed by \[Rajat Deshmukh]*
