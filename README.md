# Child Penalty Explorer: Insights from Germany

This repository hosts a Dash web application for exploring the “child penalty” in Germany—how becoming a parent affects wages, working hours, and employment opportunities for men and women. The findings in this project draw on large-scale empirical data and event-study approaches, with interactive pages that let you delve into overall trends, subgroup analyses, methodology, and a “Build Your Profile” tool to estimate penalties for different demographic characteristics.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Deployment on Render](#deployment-on-render)

## Overview 

In many countries, women’s earnings and employment trajectories diverge sharply from men’s after becoming parents—a phenomenon often referred to as the “child penalty.” In Germany, this penalty remains especially pronounced, influenced by factors such as traditional gender norms, childcare availability, policy structure, and more.

**Key questions addressed:**
- How does having a child change women’s earnings and job participation?
- Which groups (by residential area, education, etc.) face a higher or lower penalty?
- Does the 2007 Parental Leave Reform (“Elterngeld”) reduce these penalties?

**Key takeaways:**
- Women’s earnings drop ~54% following the first child, compared to men’s relatively stable earnings.
- This penalty can persist 10+ years, indicating long-term career impacts.
- Subgroup analyses reveal heterogeneity along dimensions like urban vs. rural residence, education level, partnership status, and more.

## Features
- **Multi-Page Dash Application:** Organized into pages for Introduction, Overview, Methodology, Heterogeneous Analysis, Reform Analysis, and Profile Building.
- **Interactive Plots:** Users can select measures (income, hours, or employment status) and subgroups to see how outcomes evolve over time around the birth event.
- **Reform Analysis:** Visualizes how the 2007 parental leave reform might have impacted child penalties across different categories.
- **Profile Building:** Allows users to choose demographic attributes (e.g., gender, rural/urban, education level) and estimates their predicted long-run penalty.
- **Event-Study Design:** Compares individuals’ labor outcomes from pre-birth to post-birth relative to a baseline, controlling for year and age.

## Project Structure

```bash
.
├── app.py
├── requirements.txt
├── assets/
│   ├── style.css
│   └── worklife_balance.png
├── results/
│   ├── general_results_esa.csv
│   ├── general_results_ia.csv
│   ├── general_results_wha.csv
│   └── heterogeneous_analysis/
│       └── ... (subgroup .csv files)
└── README.md 
```

- `app.py`
  - The main entry point for the Dash application. Defines all pages, callbacks, 
    and layout.
- `assets/`
  - `style.css`: CSS styling for  the app.
  - `worklife_balance.png`: An image referenced in the project.
- `results/`
  - Contains CSV files for the general results (overall analysis) and a subfolder 
    `heterogeneous_analysis` for subgroup-specific results.
- `requirements.txt`
  - Lists the Python dependencies needed to run this Dash app.
    
## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/<merveogretmek>/<child-penalty-dash-app>.git
cd <child-penalty-dash-app>
```

### 2. Create and Activate a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate     # On macOS/Linux
venv\Scripts\activate        # On Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Application Locally

```bash
python app.py
```

By default, the Dash server should start on `http://127.0.0.1:8050/`. Visit that URL in your browser to explore the app.

## Usage

Once the app is running, you can navigate through the different pages via the top navigation bar:

1. **Introduction-** Landing page with a brief overview of the Child Penalty concept.
2. **Overview-** Presents the big-picture child penalty results for Germany.
3. **Methodology-** Discusses the event-study design, sample criteria, and research aims.
4. **Heterogeneous Analysis-** Lets you explore subgroups (e.g., rural vs. urban, different education levels) to see how child penalties vary.
5. **Reform Analysis-** Highlights how the 2007 Parental Leave Reform might have influenced long-run child penalties, visualized by bar charts.
6. **Build your Profile-** Allows you to select demographic characteristics, returning an estimated penalty for your chosen profile.


If you find this tool helpful or would like to suggest improvements, feel free to open an issue or submit a pull request!







