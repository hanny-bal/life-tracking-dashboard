# Life tracking dashboard
This repository contains code for a life tracking dashboard that brings together time entries from Toggl Track, user surveys with Google Forms and auxiliary data sources. The software is a template for similar efforts and should serve as a replacement for visualisation tools like [Looker Studio](https://lookerstudio.google.com) or [Power BI](https://www.microsoft.com/de-de/power-platform/products/power-bi), which are often used for this purpose.

## 📊 Data collection
The dashboard integrates multiple personal data streams and should provide a broad overview of personal well-being:

- **Time tracking (Toggl Track):** All 24 hours of the day are tracked using [Toggl Track](https://track.toggl.com/), using projects and clients for categorisation. Data is retrieved via the Toggl v9 API.

- **Daily surveys (Google Forms):** A short daily Google Form captures self-reported mood, qualitative reflections, and gratitude journaling entries. Responses are automatically synced through Google Sheets and imported into the dashboard.

- **Health data (CamAPS FX):** Blood sugar measurements recorded through CamAPS FX are exported from [MyLife Cloud](https://mylife-software.net/Pages/Login.aspx) as a CSV file and ingested as an auxiliary dataset. The values are aligned temporally with other data sources to enable health–behaviour correlations.
