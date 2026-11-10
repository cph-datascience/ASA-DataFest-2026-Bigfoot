# Meeting Medical Accessibility Needs

## ASA DataFest 2026 | Team Bigfoot | Katy Adcox, Dean Callahan, Devon Walker, and Jonathan David Juarez

A data science project exploring differences in healthcare accessibility across Kansas. Using healthcare-related records, Census geography, and indicators of transportation, financial, and social needs, our team created an exploratory **Medical Access Score** and visualized geographic differences in access to healthcare resources.


## Project goals

- Examine the distribution of healthcare resources and patient needs across Kansas counties.
- Explore relationships among healthcare locations, patient counts, and reported barriers to care.
- Build interactive geographic visualizations to communicate potential areas of need.
- Identify counties that may benefit from further investigation and resource planning.

## Key findings

Our final presentation highlighted **Nemaha, Jackson, and Pottawatomie counties** as priority areas for additional attention, based on the team's exploratory scoring approach.

| County | Medical Access Score reported in presentation |
| --- | ---: |
| Nemaha | 0.077 |
| Jackson | 0.138 |
| Pottawatomie | 0.216 |

For additional context, refer to the presentation [`final presentation`](presentation/bigfoot_presentation.pptx).

## Notebooks

| Notebook | Purpose |
| --- | --- |
| [`clustering.ipynb`](notebooks/clustering.ipynb) | County-level summaries, exploratory access scoring, and interactive geographic visualizations. |
| [`notebook.ipynb`](notebooks/notebook.ipynb) | Exploratory mapping of patient-associated Census locations using Folium. |
| [`Financial and County Needs.ipynb`](notebooks/Financial%20and%20County%20Needs.ipynb) | Analyzes financial barriers and unmet financial needs across Kansas counties. |
| [`Social and County Needs.ipynb`](notebooks/Social%20and%20County%20Needs.ipynb) | Examines social needs and their geographic distribution across Kansas counties. |
| [`Transportation and County Needs.ipynb`](notebooks/Transportation%20and%20County%20Needs.ipynb) | Explores transportation-related barriers to healthcare access by county. |

## Repository Structure

```text
Bigfoot/
│
├── data/
│   ├── geospatial/
│   │   ├── kansas_counties.geojson
│   │   └── kansas_tracts.geojson
│   │
│   └── private/
│       ├── documentation/
│       │   ├── DataFest 2026 Challenge.docx
│       │   ├── Read Me_ About the Data.docx
│       │   ├── Social Determinant Questions and Domains.csv
│       │   └── Variable Definitions.csv
│       │
│       ├── processed/
│       │   ├── foot.csv
│       │   └── sd_clean.csv
│       │
│       └── raw/
│           ├── departments.csv
│           ├── diagnosis.csv
│           ├── encounters.csv
│           ├── patients.csv
│           ├── providers.csv
│           ├── social_determinants.csv
│           └── tigercensuscodes.csv
│
├── images/
│   ├── Patients per county.png
│   ├── Patients per postal code.png
│   ├── Unmet Financial.png
│   ├── Unmet Social.png
│   └── Unmet Transportation.png
│
├── notebooks/
│   ├── clustering.ipynb
│   ├── Financial and County Needs.ipynb
│   ├── notebook.ipynb
│   ├── Social and County Needs.ipynb
│   └── Transportation and County Needs.ipynb
│
├── outputs/
│   ├── 01_initial_map.html
│   ├── 02_location_counts.html
│   ├── 03_location_patient_ratio.html
│   ├── 04_county_access_score.html
│   ├── 05_transportation_access.html
│   ├── 06_financial_access.html
│   ├── 07_combined_access_score.html
│   └── patient_locations_sample.html
│
├── presentation/
│   ├── Bigfoot - Presentation.pptx
│   └── map.html
│
├── .gitignore
├── README.md
└── requirements.txt
```

**Note:** The `data/private/` and `outputs/` directories are excluded from Git by `.gitignore`.

## Tools and libraries

- **Python** — data analysis and processing
- **pandas / NumPy** — data manipulation
- **GeoPandas** — geographic data processing
- **Folium / Leaflet** — interactive maps
- **Matplotlib** — charts
- **Jupyter** — interactive analysis notebooks 
- **Excel** - additional processing and cleaning of data (`foot.csv`,`sd_clean.csv`)

**Data-use restriction:** ASA DataFest competition data is private and not redistributed. Datasets were deleted after competiton per the use agreement.

### Generated maps

-Intermediate map generating cells are saved as HTML files in `outputs/`.
- The final map can be accessed here: [`map`](presentation/map.html).


## Visualizations

### Patient Distribution by County

![Patients by County](images/Patients%20per%20county.png)

### Patient Distribution by Postal Code

![Patients by Postal Code](images/Patients%20per%20postal%20code.png)

### Unmet Financial Needs

![Unmet Financial Needs](images/Unmet%20Financial.png)

### Unmet Social Needs

![Unmet Social Needs](images/Unmet%20Social.png)

### Unmet Transportation Needs

![Unmet Transportation Needs](images/Unmet%20Transportation.png)
