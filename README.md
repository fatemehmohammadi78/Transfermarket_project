# Football Data Analysis Project

## Overview

This project aims to perform comprehensive data analysis and leverage machine learning techniques on football transfer data from Transfermarkt, a widely-used website for football transfer information. By extracting valuable insights from the scraped data, we intend to gain a deeper understanding of player and team performance, as well as predict specific outcomes using machine learning models.

## Project Workflow

1. **Data Scraping:**
   We start by employing advanced web scraping techniques to gather essential football-related data from Transfermarkt. The data includes player details, transfer history, team information, and more.

2. **Data Storage:**
   To facilitate efficient querying and analysis, we design and implement a well-defined database schema. The scraped data is then stored in the database, ensuring seamless integration with the analysis implementations.

3. **Statistical Analyses:**
   Our next step involves performing in-depth statistical analyses on the collected data. This process helps us uncover valuable insights, identify trends, and derive meaningful player and team performance metrics.

4. **Machine Learning Model Training:**
   Building upon the insights gained from statistical analyses, we dive into the exciting realm of machine learning. We develop and train sophisticated models to predict specific outcomes, such as player performance, team success, or transfer values.

## Getting Started

To get started with this project, follow these steps:

1. Clone the repository:
```bash
git clone git@github.com:sinaaasghari/Transfermarket-project.git
```

2. Install the necessary dependencies:
``` bash
pip install -r requirements.txt
```
3. Scraping the Required Data:


   Steps:

    - Scraping the seasons and countries data.
    - Scraping the leagues data based on seasons and countries and unique information for each league.
    - Scraping the clubs data based on seasons and leagues and unique information for each club.
    - Scraping the players data based on seasons and clubs and unique information (performances) for each player.
    - Scraping the transfer data for each of the players.
    - Scraping the data of the clubs' appearance in the 2021 Champions League.

- Modify the scraping script (all .py files in `Scrapping data` folders ) to specify the desired data to be collected.
- Run the script to scrape the data from Transfermarkt.
- The scraped data will be stored in the database for further analysis.
## Design, Implementation, and Storage of Data in the Database

1. **Set up a database system (e.g., MySQL, PostgreSQL) and create a new database for the project.**

   - In the project directory, you will find a file named `model.py`. Open this file and modify the database configuration section according to your database system. Replace the placeholders with your actual database connection details, such as the username, password, host, and database name.

   - For example, if you are using PostgreSQL, you can configure the database connection as follows:

     ```python
     # model.py

     # Replace 'username', 'password', 'localhost', and 'db_name' with your actual database credentials and database name.
     DATABASE_URI = 'postgresql://username:password@localhost/db_name'
     ```


2. **Database Table Creation and Schema:**

   The database table creation and schema definition are handled in the following files:

   - `tables_cleaning_preparation.ipynb`: This Jupyter notebook contains the necessary code to create and prepare the tables for the project in the database. Execute the notebook to set up the required tables and data structures.

   - `model.py`: This Python script defines the SQLAlchemy models for the database tables. The models represent the data entities and their relationships. Modify this file to match the table schema and data relationships you created in `tables_cleaning_preparation.ipynb`.

3. **Inserting Data into the Database:**

   To populate the database with the scraped data, use the following file:

   - `insert_data.ipynb`: This Jupyter notebook contains the code to insert the scraped data into the respective database tables using the SQLAlchemy ORM. Execute this notebook to store the scraped data in the database.

4. **Data Cleaning and Deletion:**

   Data cleaning and deletion can be performed using the following file:

   - `delete.py`: This Python script provides functions to delete specific data entries from the database. Customize this file to handle data deletion based on your project requirements.

5. **Database Schema Visualization:**

   To get an overview of the database schema, refer to the provided PDF file:

   - `TransfermarktDiagram.pdf`: This PDF file contains the visualization of the database schema. It gives an intuitive representation of the data relationships and table structures.

By following these steps, you can set up, modify, and interact with your database using SQLAlchemy ORM. This will provide you with a convenient and Pythonic way to work with the database for data analysis and machine learning tasks.

## Statistical Analyses

The statistical analyses are divided into separate notebooks, each handling specific requests and hypotheses:

- Descriptive_statistic_Q1.ipynb
- Descriptive_statistic_Q2.ipynb
- Descriptive_statistic_Q3.ipynb
- Descriptive_statistic_Q4.ipynb
- Descriptive_statistic_Q5.ipynb
- Descriptive_statistic_Q6.ipynb
- Q7.ipynb
- Q8 & Q9.ipynb
- Q10 Hypothesis 1.ipynb
- Q11 Hypothesis 2.ipynb
- Q12 Hypothesis 3.ipynb

## Machine Learning Model Training

The machine learning section of the project involves using machine learning techniques to estimate and classify data from transfermarkt.com. The machine learning notebooks are as follows:

- ML_Q1.ipynb
- ML_Q2.ipynb
- ML_Q3.ipynb

## Technologies Used

- Python: The primary programming language for data scraping, analysis, and machine learning model development.
- Beautiful Soup and Selenium: Libraries used for web scraping the data from Transfermarkt.
- Pandas and NumPy: Essential for data manipulation and preprocessing tasks.
- SQLAlchemy: For creating and managing the database and data storage.
- Scikit-learn: To develop and train machine learning models.
- Matplotlib and Seaborn: For visualizing the data and analysis results.


## License

This project is under the MIT License. Feel free to use, modify, and distribute it as per the terms mentioned in the License.

## Contribution

Contributions are welcome! If you find any issues or have suggestions for improvements, please submit an issue or a pull request. Let's collaborate and make this project even better.

## Acknowledgments
Special thanks to:
- The Transfermarkt website for providing valuable data for analysis.
- Open-source libraries and frameworks used in this project.
-  [*Hossein JourEbrahimian*](https://github.com/H055EIN), [*Amirhossein Sharifinezhad*](https://github.com/Powerostad), [*Mohammadhossein Shamsipour*](https://github.com/Mound21k) for their contributions and efforts in developing this project.