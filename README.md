**Copenhagen Airport Flight Scraper**

A Python web scraper that retrieves all flight departures from Copenhagen Airport (CPH) for a specified date and time, solving the problem of manually checking individual airlines for destination availability.


Problem Statement

When planning travel without a specific destination in mind, checking each airline's routes individually is time-consuming. The Copenhagen Airport website loads only 10 flights at a time dynamically, requiring multiple manual interactions. This tool automates the process by scraping all available departures and enriching them with airport details. 

Disclaimer: I know sites like skyscanner or momondo exists. I wanted to build this nevertheless.

Features

    Dynamic content handling using Selenium to load all available flights
    User input for flexible date/time selection
    Automated pagination through "Load More" clicks
    Data enrichment via RapidAPI to fetch airport details by IATA code
    Structured output as a pandas DataFrame for easy analysis

Tech Stack

    Python 3.x
    Selenium - Dynamic web scraping
    BeautifulSoup4 - HTML parsing
    Pandas - Data manipulation and structuring
    Requests - API calls for airport information
    RapidAPI - Airport details lookup

How It Works

    Prompts user for departure date and time
    Launches automated browser session to CPH departures page
    Handles cookie consent popup
    Clicks "Load More" button repeatedly to load all flights
    Parses departure times, destinations, flight codes, and airlines
    Fetches additional airport details via IATA codes
    Outputs comprehensive flight data in a structured format

Usage

Follow the prompts to enter:

    Month (numeric)
    Day (numeric)
    Starting hour (24-hour format)

Output

Two DataFrames:

    Departures: Time, Destination, IATA code, Flight number, and Airline
    Airports: Detailed airport information for all destinations

Note

This was a quick practical solution to a real travel planning problem—demonstrating how automation can turn a tedious manual task into a simple script.
