# Jabeng Beer Stop Data Automation

## Table of Contents

- [Purpose](#purpose)
- [Features](#features)
  * ##### [Collect Sales Data](#collect-sales-data)
  * ##### [Validate Input](#validate-input)
  * ##### [Update Worksheets](#update-worksheets)
  * ##### [Calculate Surplus](#calculate-surplus)
  * ##### [Calculate Stock Levels](#calculate-stock-levels)
  * ##### [Retrieve and Display Stock Values](#retrieve-and-display-stock-values)

- [Technologies Used](#technologies-used)
- [Requirements](#requirements)
- [Setup](#setup)
  * ##### [Clone the Repository](#clone-the-repository)
  * ##### [Install Dependencies](#install-dependencies)
  * ##### [Setup Google Cloud Credentials](#setup-google-cloud-credentials)
  * ##### [Create and configure Google Sheets](#create-and-configure-google-sheets)

- [Usage](#usage)
  * [Programm Flow](#program-flow)
- [Functions](#functions)
- [Flowchart](#flowchart)
- [Testing](#testing)
- [Deployment](#deployment)
- [Acknowledgements](#acknowledgements)

## Purpose

The Jabeng Beer Stop Data Automation project is designed to streamline the process of collecting and managing sales data of six types of beers for a beer store. The program automates data entry, calculates surplus, updates stock levels, and provides stock recommendations for six beer types.


The purpose of this programm 

## Features

* #### Collect Sales Data: 
    Prompt the user to enter sales data for six different beer types.

* #### Validate Input: 
    Ensure that the input data is valid and correctly formatted.

* #### Update Worksheets: 
  Append sales and surplus data to the relevant Google Sheets worksheets.

* #### Calculate Surplus:
   Determine the surplus for each beer type based on sales and stock data.


* #### Calculate Stock Levels: 
  Compute new stock levels based on average sales from the last five markets.


* #### Retrieve and Display Stock Values: 
  Fetch beer type headings and current stock values, displaying them in a user-friendly format.


## Technologies Used

* Python - used to provide functionality to the app.

* [Google Sheets](https://workspace.google.com/products/sheets/) - used to host application data

* [Gitpod](https://www.gitpod.io/) - used to create code and content for the repository.

* [Github](https://github.com/) - used to host the repository

* [draw.io](https://app.diagrams.net/) - used to create the flowchart in the planning stages. 

## Requirements

* Python 3.x

* `gspread` library

* `google-auth` library

* Google Cloud project with Google Sheets API enabled

* `creds.json`  file containing your Google Cloud credentials


## Setup

1. #### Clone the repository.

2. #### Install dependencies:
   `pip install gspread google-auth`

3. #### Setup Google Cloud credentials:
   
    *   Ensure you have a `creds.json` file with your Google Cloud credentials.
    *   Place this file in the project root directory.

4. #### Create and configure Google Sheets:

   * Create a Google Sheet named `jabeng_beer_stop`.
   * Create worksheets named ``sales``, ``surplus``, and ``stock``.
   * Ensure the first row of the ``stock`` worksheet contains beer type headings.

## Usage

Run the script by executing the following command:

``python run.py``

### Program Flow

1. #### Start

2. #### Collect Sales Data:
   * Prompt the user for sales data of six beer types.
   * Validate the input.

3. #### Append Sales Data to Worksheet:
   * Convert sales data to integers.
   * Append the data to the ``sales`` worksheet.

4. #### Calculate Surplus:
   * Calculate the surplus for each beer type based on the stock.
   * Append the surplus data to the ``surplus`` worksheet.

5. #### Calculate Average Sales:
   * Retrieve the last 5 entries of sales data.
   * Calculate the average sales for each beer type.

6. #### Calculate Stock Recommendations:
   * Use the average sales to calculate new stock levels.
   * Append the new stock data to the ``stock`` worksheet.

7. #### Retrieve and Display Stock Values:
   * Retrieve beer type headings.
   * Build a dictionary of stock values.
   * Print the stock values dictionary.

8. #### End   

## Functions

* ``get_sales_data()``: Collects sales data from the user.

* ``validate_data(values)``: Validates the sales data input.

* ``update_worksheet(data, worksheet)``: Updates the specified worksheet with the provided data.

* ``calculate_surplus_data(sales_row)``: Calculates the surplus for each item type.

* ``get_last_5_entries_sales()``: Retrieves the last 5 entries for each beer type from the sales worksheet.

*  ``calculate_stock_data(data)``: Calculates the average stock for each item type, adding 10%.

* ``get_stock_values(stock_values)``: Retrieves beer type headings and builds a dictionary with stock values.

* ``main()``: Runs all program functions in sequence.`

## Flowchart

![Flowchart](images/flow.webp) 


## Testing

I checked my code by installing pep8 `pip3 install autopep8` and got no errors after testing. 

I also checked my code again on [Python code checker](https://www.pythonchecker.com/) with no errors to report. 


## Deployment
* The project was deployed to [heroku](https://www.heroku.com/). First we create a new app on the Heroku Dashboard.

* After the App is created, head over to the settings tab and create a Config Var and add a KEY called CREDS and its contents as it's VALUE. The template code used will use this information to create a file called creds.json and write  this data into it as the application is built. 

![Settings](images/settings.PNG)
![config_var](images/config_var.PNG)

* The next step is to add a couple of  buildpacks to the application.
Scroll down and click the “Add buildpack” here. Select Python as the first  buildpack and then select node.js as the next buildpack to handle the mock terminal.

![Buildpacks](images/Buildpacks.PNG)

* Next we select the deploy tab to choose the method with which we want to deploy.

* Select Github and confirm that we want to connect.

![Github_deploy](images/deploy.PNG)


* Search for the repository name and connect



## Acknowledgments

* [gspread](https://github.com/burnash/gspread)

* [Google Auth Library](https://github.com/googleapis/google-auth-library-python)

* [Love Sandwiches Walkthrough project by Code Institute](https://bit.ly/3zyJce8) 

* [Code Institue](https://bit.ly/3zyJce8) Tutor Assisstant




















