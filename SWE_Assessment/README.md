# Medical Bill Upload Service

This is a service that allows users to upload and retrieve medical bills. It's made with Node.js and Express. 

## Table of Contents
- [Installation](#installation)
- [Endpoints](#endpoints)
- [Testing](#testing)

## Installation

1. Clone this repository:

   `git clone https://github.com/Adnanahmed0014/TruffleHealth_SWEAssessment.git`

2. Install dependencies:

   `npm install`

   *NOTE: At this stage, if you are not in the correct directory, you will recieve an error, as the 'package.json' file will not be available. To address this issue, navigate to the correct directory, where the project is stored. Now you can run step 2 without any errors.  

   *Recommendation, if you're new to github and are using VScode, when cloning the repository, and you are asked where you would like to place the location of the repository, select Downloads. Then, in terminal, type: `cd SWE_Assessment`. Continue with the installation process by typing `npm install`. Move on to Step 3. 

3. Install Jest for testing:

   `npm install --save-dev jest`

## Endpoints

- **GET /items**: Returns a list of medical bills.

- **POST /items**: Creates a new medical bill.

## Testing

Run tests using Jest:

`npm run test`

# Testing through Terminal 
1. To GET the list of medical bills, run: 

    `curl http://localhost:3000/items`

2. To add a POST request, run: 

    `curl -X POST http://localhost:3000/items -H 'Content-Type: application/json' -d '{ "data": "value" }'`

*NOTE: Keep in mind that the data that you will be uploading through terminal should be in the same format as the orignal data. 

For Example: 

Instead of '{ "data": "value" }', the format (with sample data) should be: 

'{ "patientName": "Bill", "patientAddress": "21 second street", "hospitalName": "Gen hospital", "dateOfService": "2022-02-23", "billAmount": 500 }'

# Testing through Postman 
 
1. Create a new Collection 
2. Add a new request 
3. To GET the list of medical bills, add the following: 
    1. http://localhost:3000/items
    2. Click Send 
4. To add a POST request, add the following: 
    1. http://localhost:3000/items
    2. Navigate to the Body
    3. Select raw as the data type 
    4. Make sure JSON is selected on the right 
    5. Add the data that you would like to upload 
        *Remember: The data should be in the same format as the original data, to view an example, go back to # Testing through Terminal
    6. Click Send   

*NOTE: If you're having issues restarting the server to run a new test, a simple way would be to kill the server and rerun the test. To do this, type `lsof -i :3000` into terminal. Take the number under 'PID' and use it to kill the server. For example, if the number under 'PID' is '98765', type this into terminal: `kill 98765`. Now you can restart the server for testing by running `npm run test` again. 


