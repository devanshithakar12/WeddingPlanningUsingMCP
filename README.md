# WeddingPlanningUsingMCP

## Prerequisites

- [Docker](https://www.docker.com/get-started) installed
- [VS Code Insiders](https://code.visualstudio.com/insiders/) installed
- A Google Maps API key (see [instructions](https://developers.google.com/maps/documentation/javascript/get-api-key#create-api-keys))
- GitHub Copilot with agent mode enabled

## Project Description

This repository helps you find wedding venues based on your guest list capacity and preferred location. It leverages the Google Maps MCP server to search for venues that match your criteria, making wedding planning easier and more efficient.

## Setup Instructions

1. **Clone the repository**  
    ```bash
    git clone <repository-url>
    cd WeddingPlanningUsingMCP
    ```

2. **Create a `.env` file**  
    Add your Google Maps API key to a `.env` file in the project root:
    ```
    GOOGLE_MAPS_API_KEY=your_api_key_here
    ```

3. **Open the project in VS Code Insiders**  
    Launch VS Code Insiders and open the project folder.

4. **Enable GitHub Copilot agent mode**  
    Make sure agent mode is turned on in GitHub Copilot for enhanced assistance.

You are now ready to use the application to search for wedding venues based on your requirements!

## Example Usage

### Step-by-Step Example to enter in Github Copilot Agent Mode

1. Search for wedding venues for 350+ guests with indoor and outdoor spaces in San Francisco
2. For each of these venues, calculate the distance from the nearest airport.
3. Can you add all of this information to my csv file with the known columns.

## Connecting to Your Email Server and Creating an Email Template

### Step 1: Connect to Your Email Server with MCP

Follow the MCP documentation to configure your preferred email server (e.g., Gmail, Outlook) for sending emails.

Example `.env` additions:
```
EMAIL_SERVER=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@gmail.com
EMAIL_PASSWORD=your_email_password
```

### Step 2: Create an Email Template

Prepare a template to reach out to venues using the contact information from your CSV file. Here’s a sample template:

```
Subject: Inquiry About Wedding Venue Availability

Dear [Venue Name] Team,

I am interested in hosting a wedding at your venue for approximately [Guest Count] guests. We are looking for both indoor and outdoor spaces and would appreciate information on availability, pricing, and amenities.

Could you please provide details and let us know if you have availability for our preferred dates?

Thank you,
[Your Name]
[Your Contact Information]
```

You can automate sending these emails using MCP by iterating through your CSV and replacing the placeholders with actual data for each venue.