# Yelp Data Visualization for Restaurant Insights

An interactive data visualization dashboard designed to assist aspiring restaurant owners in making informed business decisions. By analyzing the Yelp Open Dataset, this tool uncovers patterns in location density, opening hours, and customer rating trends.

![Dashboard Overview](images\image_1_overview.png)
> *Snapshot of the main dashboard interface showing linked views and geospatial analysis.*

## 📖 Project Overview
This project bridges the gap between raw data and actionable business intelligence. Focusing on **Philadelphia, Tucson, and Tampa**, the visualization allows users to:
* Identify high-competition zones and "restaurant deserts."
* Optimize opening hours based on competitor analysis.
* Track temporal trends in customer ratings for specific cuisines.

The tool was built using **Python** and **Bokeh**, adhering to formal data visualization principles such as Shneiderman's mantra ("Overview first, zoom and filter, then details-on-demand").

## 👨‍💻 My Contributions
**Role:** Dashboard Architecture & Interaction Design

While this was a group effort, my primary focus was the design and implementation of the **interactive dashboard** and the **User Experience (UX)** logic.

* [cite_start]**Dashboard Layout:** Designed the layout to minimize cognitive load, placing controls alongside real-time updates to support intents like "Show me something conditionally"[cite: 61, 63].
* [cite_start]**Interaction Logic:** Implemented the filtering systems (City, Category, Rating) and the Model-View-Controller (MVC) patterns that handle the refresh/update functionality[cite: 68].
* [cite_start]**Direct Manipulation:** Engineered the interface to allow users to manipulate data representations directly (e.g., toggling contours, selecting ratings), ensuring high "Directness of Interaction"[cite: 65].

## 🚀 Key Features

### 1. Geospatial Analysis (Hexbin Map)
A hexbin plot overlaid on a city map to visualize restaurant density.
* [cite_start]**Purpose:** Mitigates overplotting to show high/low density areas at a glance[cite: 73].
* [cite_start]**Interaction:** Users can use "Lasso Select" to highlight specific neighborhoods, which links directly to the other plots[cite: 79].

### 2. Operational Strategy (Scatter-Contour Plot)
Maps opening hours (x-axis) against opening duration (y-axis).
* [cite_start]**Purpose:** Helps owners identify low-competition time slots[cite: 95].
* [cite_start]**Features:** Includes toggleable contour lines to combat overplotting and visualize the most common operating windows[cite: 86].

### 3. Market Trends (Line Chart)
A temporal analysis showing a 365-day rolling average of star ratings.
* [cite_start]**Purpose:** Allows users to compare the performance of different restaurant categories over time to spot market threats or opportunities[cite: 99, 103].

## 🛠️ Technologies Used
* **Language:** Python
* [cite_start]**Library:** Bokeh (for interactive visualizations) [cite: 135]
* **Data Processing:** Pandas (JSON parsing and cleaning)
* [cite_start]**Dataset:** [Yelp Open Dataset](https://www.yelp.com/dataset) (Academic Use) [cite: 15]

## ⚙️ Installation & Usage

1. Create a new virtual environment
2. Install other requirements using `pip install -r requirements.txt`
3. Add data files to `/data/...` (<https://drive.google.com/drive/folders/1Bxcp7AepA0WYMYJPcHPyx1_qM6JBlRrj>)

## Run

To see the dashboard, run this command from your command prompt:

`bokeh serve --show main.py`

Note: Your directory should be in the Dashboard folder.
