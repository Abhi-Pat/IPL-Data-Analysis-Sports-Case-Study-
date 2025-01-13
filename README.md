# IPL Data Analysis - Extended Description

This repository offers an in-depth analysis of the **IPL Matches 2008-2020** dataset and  covering match-level and ball-by-ball data from the 2008-2020 seasons. The analysis includes a variety of insights into overall match statistics, player performance, toss decisions, and team victories, with the help of Python libraries like **Pandas**, **NumPy**, **Matplotlib**, **Seaborn**, and **Plotly**.

### **1. Data Import and Setup**
To begin the analysis, we imported several Python libraries for data manipulation, visualization, and statistical analysis:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
import plotly.graph_objs as go
from plotly.offline import init_notebook_mode, plot, iplot
```

The data was extracted from two CSV files:
- **Deliveries Data**: Contains ball-by-ball data for IPL matches from 2008-2020.
- **Match Data**: Contains match-level details such as teams, toss winners, match winners, and venue information.

```python
deliveries_data = pd.read_csv(r'Z:\5.. IPL\Datasets/IPL Ball-by-Ball 2008-2020.csv')
match_data = pd.read_csv(r'Z:\5.. IPL\Datasets/IPL Matches 2008-2020.csv')
```

### **2. Basic Data Analysis**

The first phase of the analysis focuses on providing key insights across the entire dataset:
- **Total Matches Played**: The total number of IPL matches from 2008-2020.
- **Venues Played At**: Identifying all the venues where IPL matches were held.
- **Total Teams Participated**: Identifying all the teams that have participated in the IPL.
- **Maximum Toss Winner Teams**: The teams that have won the toss the most often.
- **Most Player of the Match Awards**: The players who received the highest number of "Player of the Match" awards.

### **3. Batsman Performance Analysis - Focus on Virat Kohli**

The next step was to perform a detailed analysis of a specific batsman, **Virat Kohli (VKohli)**, including:
- **Extracting All Unique Batsmen**: A list of all unique batsmen across the IPL dataset.
- **Filtering Data for VKohli**: We focused on analyzing only the records for Virat Kohli.
- **Runs Scored**: We calculated the total runs scored by Virat Kohli, breaking them down by categories of runs: 1s, 2s, 3s, 4s, and 6s.

To visualize the contribution of each category of runs, we created a **donut chart** that shows the percentage of runs scored in each category.

### **4. Toss Decision Analysis Across Seasons**

We analyzed how teams made toss decisions over the years:
- We plotted a **bar plot** of "Season" vs "count" for the toss decisions (whether teams decided to bat or field), using a **hue** to represent each year. This provided insights into how teams' toss decisions have evolved throughout the seasons.

### **5. Analyzing the Relationship Between Toss Winner and Match Winner**

We explored whether winning the toss has a direct impact on winning the match:
- **Toss vs Match Winner**: We extracted data for cases where the **toss winner** was the same as the **match winner**.
- This analysis was visualized using a **pie chart**, which represented the percentage of times the toss winner won the match versus when the toss winner did not win the match.

### **6. Number of Times Each Team Has Won the Tournament**

To determine which teams have been most successful in the IPL:
- **Extracting Seasons**: We created a new column, **Seasons**, derived from the match date, to analyze the data on a per-season basis.
- We created a **dictionary** to store the winner for each season and then used the `Counter` function to identify which team won the most tournaments across the seasons.

### **7. Total Number of Wins for Each Team Throughout the Seasons**

We also analyzed the total number of wins for each team in the league:
- We calculated the total number of matches played by each team, considering both columns `"team1"` and `"team2"`. Then, we counted how many times each team appeared.
- **Inner Join**: We performed an inner join between the `match_data` and the aggregated team data, resulting in a comprehensive DataFrame showing the total matches played and total wins for each team.
- A **bar plot** was created to compare the total number of matches played versus the total number of wins for each team.

### **Visualizations**

Throughout the analysis, a variety of visualizations were created to make the findings more accessible:
- **Bar Plots**: Used to show the distribution of match statistics, such as the number of toss wins and match wins by season or team.
- **Donut Chart**: Displayed the percentage breakdown of runs scored by categories (1s, 2s, 3s, 4s, and 6s) for Virat Kohli.
- **Pie Chart**: Visualized the relationship between toss winners and match winners.
- **Line and Bar Charts**: Used for trends across different seasons, such as toss decisions and total wins.

These visualizations were created using both **Matplotlib**, **Seaborn**, and **Plotly**, enabling interactive and detailed views of the data.

---

### Conclusion

This repository provides a comprehensive analysis of IPL match data, offering insights into:
- Match statistics, such as total matches played, venues, and team participation.
- Individual player performance, with a focus on Virat Kohli's batting contributions.
- Team performance trends, including tournament victories, toss decisions, and win-loss records.
- Detailed data visualizations help present key findings and make it easier to interpret the results.

The analysis is aimed at sports analysts, IPL enthusiasts, and data scientists interested in sports data analytics. It provides useful insights into team strategies, player performances, and trends across IPL seasons.

---

### Prerequisites:
- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly

### Installation:

To run this analysis, clone the repository and ensure you have the necessary packages installed:
pip install pandas numpy matplotlib seaborn plotly
