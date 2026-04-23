# Public Transport Delay Analysis

## Project Overview

This project studies why buses and trains get delayed. Think of it as detective work where we find patterns behind late arrivals.


## Objectives

We wanted to answer four questions:

- Does weather affect delays
- Which routes and stations have the most problems
- Do public events cause more delays
- Are peak hours worse than normal hours



## Dataset

We used information about bus and train trips. Each trip record included:

- Date and time of the trip
- Weather condition at that time
- Traffic level on the road
- Any special event happening nearby
- How late the bus or train arrived



## Technologies Used

- Python for all the coding
- Pandas to organize and clean data
- Matplotlib and Seaborn to make charts
- Scikit-learn for prediction models
- SciPy for statistical testing



## Project Workflow

### Step 1: Data Cleaning

Before starting any analysis, we cleaned the data. This means:

- We checked for empty or missing information
- We removed duplicate records
- We converted dates and times into a format the computer understands
- We created new useful columns like:
    - Hour of the day
    - Day of the week
    - Whether it was a weekend or weekday
    - Whether there was an event or not



### Step 2: Finding Relationships

We made a correlation heatmap. This shows which things are connected.

Example of how correlation works:

- When one number goes up, another also goes up. That is positive correlation.
- When one goes up and the other goes down. That is negative correlation.
- If there is no pattern, there is no correlation.

Our finding: Traffic congestion and delays have a strong positive relationship.



### Step 3: Weather Analysis

We grouped delays by weather type and calculated average delay for each.

Results:

- Clear weather had the lowest average delay
- Cloudy weather was slightly worse
- Rain caused moderate to high delays
- Snow caused the highest delays

This makes practical sense. Bad weather means slower driving, slippery roads, and more caution.



### Step 4: Route and Station Analysis

We found average delays for each route and station.

Some routes consistently showed higher delays. These problem routes were often near:

- Busy market areas
- Stadiums
- Narrow roads
- Construction zones

Some stations were major delay points. Passengers at these stations faced regular late arrivals.


### Step 5: Event Impact

We compared days with events against normal days.

Normal days had lower average delays. Event days showed higher delays. Different types of events had different impact levels:

- Small local events caused minor delays
- Large concerts or sports matches caused significant delays
- Festivals and parades caused the most disruption



### Step 6: Statistical Testing

We performed a T-test. This is a method to check if two groups are truly different or if the difference happened by chance.

We compared:

- Group A: Peak hour delays (morning 8-10 AM, evening 5-7 PM)
- Group B: Non-peak hour delays

The T-test gave us a p-value less than 0.05. In simple terms, this means peak hours really do have higher delays. It is not random chance.



### Step 7: Prediction Model

We built a Simple Linear Regression model. This is a basic formula that tries to predict one number using another number.

Our model:

- Input: Traffic congestion index (a score from 1 to 10)
- Output: Predicted arrival delay in minutes

The model showed that traffic does affect delay. But the relationship is not very strong on its own. This means predicting delays accurately needs more than just traffic data. You need weather, event information, and time of day too.


## Final Conclusions

Delays are not random. They follow patterns. The main causes we identified are:

- Weather conditions, especially rain and snow
- Traffic congestion on busy roads
- Peak hours when everyone travels together
- Public events that bring large crowds

Transport planners should focus on these factors when scheduling buses and trains.



## Future Improvements

This project can be expanded in several ways:

- Use Multiple Linear Regression to include many factors at once
- Apply better models like Random Forest or XGBoost
- Build a real-time delay prediction system
- Create an interactive dashboard for transport managers



## Author

Priyal Aggarwal


## How to Use This Project

- Download or clone the repository
- Open the Jupyter Notebook file
- Run each cell from top to bottom
- Read the comments and outputs to understand each step
