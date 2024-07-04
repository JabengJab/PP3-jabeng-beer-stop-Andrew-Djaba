# Jabeng Beer Stop Data Automation

## Overview

The Jabeng Beer Stop Data Automation project is designed to streamline the process of collecting and managing sales data for a beer store. The program automates data entry, calculates surplus, updates stock levels, and provides stock recommendations for six beer types.

## Features

* Collect Sales Data: Prompt the user to enter sales data for six different beer types.

* Validate Input: Ensure that the input data is valid and correctly formatted.

* Update Worksheets: Append sales and surplus data to the relevant Google Sheets worksheets.

* Calculate Surplus: Determine the surplus for each beer type based on sales and stock data.


* Calculate Stock Levels: Compute new stock levels based on average sales from the last five markets.


* Retrieve and Display Stock Values: Fetch beer type headings and current stock values, displaying them in a user-friendly format.


## Requirements

* Python 3.x

* `gspread` library

* `google-auth` library

* Google Cloud project with Google Sheets API enabled

* `creds.json`  file containing your Google Cloud credentials


## Setup

1. Clone the repository:

2. Install dependencies:
   `pip install gspread google-auth`

3. Setup Google Cloud credentials:
   
    *   Ensure you have a `creds.json` file with your Google Cloud credentials.
    *   Place this file in the project root directory.

4. Create and configure Google Sheets:

   * Create a Google Sheet named `jabeng_beer_stop`.
   * Create worksheets named ``sales``, ``surplus``, and ``stock``.
   * Ensure the first row of the ``stock`` worksheet contains beer type headings.

## Usage

Run the script by executing the following command:

``python run.py``









