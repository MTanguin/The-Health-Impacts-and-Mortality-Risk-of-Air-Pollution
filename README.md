
#### "Creating interactive visualization using JavaScript to visualize the health impacts and mortality risk of air pollution in different countries"

CREDITS:
Heidari, Ali | Shahzad, Sameen | Syed, Farman | Tanguin, Marivic 

#### Project-3_Group-13

### "The Health Impacts and Mortality Risk of Air Pollution"


![AirQualityDashboard](https://user-images.githubusercontent.com/114210481/221664041-0066fd05-0402-494c-ab89-2633a06173d4.png)

## Background

In this project, we aim to create a data-driven web application that showcases visualizations and insights derived from a dataset. The dataset contains more than 100 unique records and is stored in a database PostgreSQL. By leveraging the power of Python Flask API, HTML/CSS, JavaScript, and the chosen database, we create an interactive web application that allows users to explore and understand the data through various visualizations.

The study involved analyzing air quality data from different countries as well as mortality rate and disease burden data related to air pollution. We used modeling technique like interactive visualizations to present the spatial distribution of pollutants such as PM25, PM10, and NO2 their ambient concentrations across different countries, quantifying air pollution,burden of disease and mortality rates. These pollutants, in addition to other pollutants vary across the globe and may result in different concentrations of air pollution  country to country.


## Purpose

The purpose of this study is to investigate the health impacts and mortality risk of air pollution, including ambient household air pollution, ambient particulate matter pollution, ambient ozone pollution, and air pollution caused by solid fuels. By examining exposure to these types of pollution, we aim to gain a better understanding of the risks associated with air pollution and identify potential strategies to mitigate its harmful effects on human health.


## Research Question

1. Ambient Air Quality Data: Which countries had the highest concentrations of PM2.5, PM10, and NO2 in 2019? (Top 10 countries)
2. Outdoor Pollution Rates by Age: Which countries had the highest death rates across different age groups (under 5, 5-14 years, 15-49 years, 50-69 years, and 70+ years) in 2019? (Top 10 countries)
3. Death Rates From Air Pollution: Which countries had the highest death rates attributed to air pollution (including household air pollution, ambient particulate matter pollution, air pollution in general, and ambient ozone pollution) in 2019? (Top 10 countries)
4. AQ Pollution Mortality Data: Which countries had the highest yearly total pollution deaths and air pollution deaths in 2019? (Top 10 countries)
5. Disease Burden by Risk Factor: Is air pollution a leading cause of death compared to other risk factors such as smoking or poor diet? (Comparison of risk factors)
6. Number of Deaths by Risk Factors: Are deaths from air pollution attributed to various risk factors such as low physical activity, air pollution, and smoking? (Examine the relationship between air pollution and other risk factors)

Please note that the specific data requested is from the year 2019. Let me know if you would like any further assistance with these research questions.
   

## Scope & Limitations:

The study covered a period of 5 years (2015-2019) and includes data on air quality, mortality rates, and disease burden associated with air pollution from a variety of countries. The focus is on the health impacts and mortality risk associated with exposure to ambient household air pollution, ambient particulate matter pollution, ambient ozone pollution, and air pollution caused by solid fuels.

The study is limited by the availability and quality of data, which may vary by country and over time. In addition, the study focuses on selected types of air pollution and does not cover all possible sources of air pollution, such as industrial emissions or transportation-related pollution.

## Methods

##### Data Collection and Database Setup:

Collected a dataset from reliable sources or through web scraping and API request.
Set up a database system PostgreSQL to store and manage the dataset.

##### Backend Development:

Utilized Python Flask API to develop the backend of the web application.
Created routes and endpoints to handle data requests and retrieve information from the database.
Ensured that the page showcasing data visualizations runs without errors.

##### Frontend Development:

Designed and developed HTML/CSS templates to create an intuitive and visually appealing user interface.
Incorporated JavaScript to enhance interactivity and user-driven interactions on the web page.
Utilized a JavaScript library to enhance the visualizations and user experience.

##### Visualization Design:

The web application includes the following visualizations:

1. Leaflet Map: The Leaflet library is used to create an interactive map that displays the spatial distribution of air pollution based on different pollutants (PM2.5, PM10, and NO2) across different countries. The map visualization enhances the understanding of the global variations in air pollution levels.

2. Bar Plots: The Plotly.js library is utilized to create bar plots that showcase the top 10 countries based on pollutant levels. The bar plots provide a visual comparison of pollutant concentrations and allow users to explore data for different years.

3. Radar Chart: The D3.js library is employed to generate a radar chart that depicts the death rates by different types of pollution. This visualization allows for a comprehensive comparison of the impact of various pollution types on mortality rates.

4. Pie Chart: The D3.js library is also used to create a pie chart representing the outdoor pollution rates by age group. This visualization provides an overview of how different age groups are affected by air pollution.

5. Disease Burden and Mortality Bar Charts: The Plotly.js library is used to generate bar charts that compare disease burden and mortality rates attributed to different risk factors with the impact of air pollution. These visualizations aid in understanding the relative contribution of air pollution to overall disease burden and mortality.

The web application incorporates JavaScript libraries like Leaflet, Plotly.js, and D3.js to create interactive and visually appealing visualizations. These visualizations allow users to explore and analyze the dataset, enabling a better understanding of the relationships between air pollution, disease burden, and mortality rates.

## Deployment:

Flask application

1. Database Connection:
   - The application establishes a connection to a PostgreSQL database using the SQLAlchemy library. The connection details, such as the username, password, and database name, are provided in the `create_engine` function.

2. ORM Mapping:
   - The application uses SQLAlchemy's `automap_base` to reflect the existing database tables and map them to Python classes. This allows the application to interact with the database using these mapped classes.

3. Flask Setup:
   - The Flask application is created using `Flask(__name__)`. The `template_folder` parameter is set to specify the folder where HTML templates are located.

4. Routes:
   - The application defines several routes using the `@app.route` decorator. Each route corresponds to a specific type of data that the application retrieves from the database.

5. Querying the Database:
   - Within each route function, the application creates a session using `Session(engine)` to establish a connection to the database.
   - It then uses SQLAlchemy's query capabilities to retrieve the desired data from the corresponding tables.
   - The retrieved data is processed and transformed into dictionaries or dictionary-based structures.
  
       Data that can be retrieved :

       1. Country Data:
          - Latitude and longitude coordinates for different countries.

       2. Ambient Air Quality Data:
          - Yearly data on PM2.5, PM10, and NO2 levels for different countries.

       3. Outdoor Pollution Rates by Ages:
          - Yearly death rates due to outdoor air pollution categorized by different age groups (under 5, 5-14 years, 15-49 years, 50-69 years, and 70+ years) for                      different countries.

       4. Death Rates From Air Pollution:
          - Yearly death rates from different types of air pollution (household air pollution, ambient particulate matter pollution, air pollution in general, and ambient               ozone pollution) for different countries.

       5. AQ Pollution Mortality Data:
          - Yearly total pollution deaths and air pollution deaths, ranked by country.

       6. Disease Burden by Risk Factor:
          - Yearly Disability-Adjusted Life Years (DALY) attributed to various risk factors (e.g., low physical activity, air pollution, smoking) for different countries.

       7. Number of Deaths by Risk Factor:
          - Yearly number of deaths attributed to various risk factors (e.g., low physical activity, air pollution, smoking) for different countries.

The Flask application sets up routes for each of these data categories and queries the corresponding tables in the database to retrieve the data. The retrieved data is then converted into dictionaries and returned as JSON responses.
       
6. JSON Responses:
   - The processed data is returned as JSON responses using Flask's `jsonify` function.
   - Each route function specifies the structure and content of the JSON response based on the retrieved data.

7. Running the Application:
   - At the end of the code, the application is run using `app.run(debug=True)`.
   - The `debug=True` parameter enables the debug mode, which provides detailed error messages and automatically restarts the application on code changes.

8. Opening the Browser:
   - The `open_browser` function is used to open the browser and display the application.
   - A Timer is set to delay the opening of the browser by 1 second to ensure that the Flask server is running before the browser is opened.

By accessing the defined routes of the Flask application, such as `"/countrydata"` or `"/agepollution"`, users can retrieve the corresponding data from the database in JSON format.


## Results:

1. Ambient Air Quality Data: Which countries had the highest concentrations of PM2.5, PM10, and NO2 in 2019? (Top 10 countries)

![Most Polluted Countries 2019](https://github.com/MTanguin/Air_Quality_Project_3/assets/114210481/af5cef95-40b9-4c9e-bd3d-6369209cf7de)

2. Outdoor Pollution Rates by Age: Which countries had the highest death rates across different age groups (under 5, 5-14 years, 15-49 years, 50-69 years, and 70+ years) in 2019? (Top 10 countries)

![Top10AirPollutionDeathsAge](https://github.com/MTanguin/Air_Quality_Project_3/assets/114210481/35c02953-6ae1-468f-a8ce-6d7f543e9e03)

3. Death Rates From Air Pollution: Which countries had the highest death rates attributed to air pollution (including household air pollution, ambient particulate matter pollution, air pollution in general, and ambient ozone pollution) in 2019? (Top 10 countries)

 ![Top10CountriesAirPolllutionDeaths](https://github.com/MTanguin/Air_Quality_Project_3/assets/114210481/6904f8c6-90c3-4b82-8a51-9017db1e54e0)

4. AQ Pollution Mortality Data: Which countries had the highest yearly total pollution deaths and air pollution deaths in 2019? (Top 10 countries)

 ![Pollution Mortality Data](https://github.com/MTanguin/Air_Quality_Project_3/assets/114210481/f93cced8-ef70-4787-b236-3b0484da4ef8)

5. Disease Burden by Risk Factor: Is air pollution a leading cause of death compared to other risk factors such as smoking or poor diet? (Comparison of risk factors)

![DiseaseBurden](https://github.com/MTanguin/Air_Quality_Project_3/assets/114210481/0786148e-549a-488f-be39-a4d8f3b6b449)

6. Number of Deaths by Risk Factors: Are deaths from air pollution attributed to various risk factors such as low physical activity, air pollution, and smoking? (Examine the relationship between air pollution and other risk factors)

![DeathRisk](https://github.com/MTanguin/Air_Quality_Project_3/assets/114210481/6c6b114a-ce54-4bd2-9554-d6252aa3ca0d)


## Conclusions:

Pollutants such as PM2.5, PM10, and NO2 allow scientists to estimate the spatial distribution of their ambient concentrations across different countries, quantifying air pollution,burden of disease and mortality rates. These pollutants, in addition to other pollutants vary across the globe and may result in different concentrations of air pollution from city to city, and country to country.

Based on our analysis, it can be concluded that air pollution is among the top five factors contributing to mortality rates and burden of disease worldwide.

It can be deduced that similar age groups (i.e., under 5, 5-14, 15-49, 50-69, 70 plus) are affected similarly by air pollution in all countries across the globe.

Understanding the severity of air pollution and the burden of disease and mortality rates related to it is important for public health officials, policymakers, and healthcare providers, as it can help them to prioritize resources and develop interventions to reduce the impact of the disease on the population.



Sources:

World Health Organization (WHO)
Links: 
[WHO Air Quality Database](https://www.who.int/data/gho/data/themes/air-pollution/who-air-quality-database)
[WHO Air Quality & Health Impacts](https://www.who.int/teams/environment-climate-change-and-health/air-quality-and-health/health-impacts)
[WHO Health Impacts & Types of Pollutants](https://www.who.int/teams/environment-climate-change-and-health/air-quality-and-health/health-impacts/types-of-pollutants)
[WHO Health Impacts & Exposure- to Air Pllution](nhttps://www.who.int/teams/environment-climate-change-and-health/air-quality-and-health/health-impacts/exposure-air-pollution)
       

Global Alliance on Health and Pollution (GAHP)  
Link: 
[Pollution & Health Metrics](https://gahp.net/wp-content/uploads/2019/12/PollutionandHealthMetrics-final-12_18_2019.pdf)


kaggle.com (@article{owidairpollution)
Links: 
[Death Rates from Air Pollution](https://www.kaggle.com/datasets/programmerrdai/air-pollution?select=death-rates-from-air-pollution.csv)
[Outdoor Air Pollution](https://www.kaggle.com/datasets/programmerrdai/outdoor-air-pollution?select=PM25-air-pollution.csv)



