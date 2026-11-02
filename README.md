cd D:\DisasterMind-AI

@'
# DisasterMind AI
### AI-Powered Natural Disaster Risk Analysis, Prediction and Scenario Generation

## 1. About the Project

DisasterMind AI is a full-stack, AI-powered disaster analysis platform that uses Machine Learning, Deep Learning, historical earthquake data, statistical modelling, and interactive visualization.

The project focuses on analysing historical earthquake activity and generating analytical insights through a web application.

It provides:
- Earthquake occurrence classification.
- Historical earthquake data analysis.
- Geographical risk visualization.
- Synthetic earthquake-count scenario generation.
- Deep Learning-based anomaly exploration.
- Interactive dashboards and reports.
- User registration and authentication.

**Important:** This is a research-oriented analytical prototype. It does not predict the exact time, location, or magnitude of earthquakes. It is not an operational earthquake early-warning system.

---

## 2. Problem Statement

Natural disasters can cause significant damage to human life, infrastructure, and the economy.

Some major challenges include:

1. Large volumes of historical earthquake data are difficult to analyse manually.
2. Earthquake activity varies across geographical locations and time.
3. Raw geological datasets are difficult for ordinary users to understand.
4. Historical patterns cannot guarantee future earthquake events.
5. Researchers need tools to explore different possible disaster scenarios.
6. Data processing, Machine Learning, and visualization are often performed using separate tools.

## 3. Our Proposed Solution

DisasterMind AI provides a unified platform for historical earthquake analysis and scenario exploration.

### How We Solved the Problem

1. Data Collection: Retrieved historical earthquake records using the USGS Earthquake API.
2. Data Cleaning: Removed invalid and incomplete records and prepared structured datasets.
3. Feature Engineering: Converted earthquake records into geographical grid-cell and monthly observations.
4. Machine Learning: Trained models to classify next-calendar-month M4+ earthquake occurrence in geographical grid cells.
5. Deep Learning: Explored Autoencoders and Variational Autoencoders for anomaly analysis.
6. Scenario Generation: Developed a statistical generator to produce synthetic earthquake-count scenarios.
7. Visualization: Created interactive maps, charts, dashboards, and reports.
8. Integration: Connected the React frontend, Node.js backend, Python AI engine, and MongoDB database.

---

## 4. System Architecture

```text
                    USER
                      |
                      v
              REACT + VITE
               PORT 5173
                      |
                      v
              NODE.JS + EXPRESS
               PORT 5000
                      |
             +--------+--------+
             |                 |
             v                 v
        MONGODB ATLAS       PYTHON FASTAPI
        USER DATABASE       AI ENGINE
                            PORT 8000
                                |
                    +-----------+-----------+
                    |           |           |
                    v           v           v
                  MACHINE    DEEP        SCENARIO
                  LEARNING   LEARNING    GENERATOR
                    |
                    v
              TRAINED MODELS
              AND DATASETS
