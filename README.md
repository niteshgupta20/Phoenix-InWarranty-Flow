# Postman API Automation Integration with Github Actions #

This repository is a demonstration for POC for integrating postman tests with github actions. The Tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. you can also execute the project manually using workflow_dispatch. The projects runs on a scheduled time with the help of the cron job.

The HTML report is archived and kept in the artifact section for the team to download. Along with that they can view the report directly from the github page : https://niteshgupta20.github.io/Phoenix-InWarranty-Flow/.
The latest report is mailed to the team members using GMAIL SMTP.

## About Me ##
Hi my name is Nitesh Gupta. I have 6 yrs of experience in automation testing. my skillset includes UI Automation with Selenium Webdriver and for API Testing I use Rest Assured and Postman.
You can connect with me over: (https://www.linkedin.com/in/niteshgupta20/)

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets

## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for Self hosted Github Runner

## Github Pages ##
You can direclty view the latest test report of the postman at the Github Page Link: https://niteshgupta20.github.io/Phoenix-InWarranty-Flow/

## HTML Report ##
The Report will be created in the newman folder.
![Postman Report](https://github.com/niteshgupta20/Phoenix-InWarranty-Flow/blob/static-content/newman-report.PNG)

## Project Structure ##
```
Phoenix InWarranty Flow
├─ Inwarranty-Flow Collection.postman_collection.json # Collection File
├─ QA.postman_environment.json # Enviroment File
├─ testdata.csv # TestData File
```

## How to run the Project? ##
You can run the project on your local system for that:
1. Clone the project on Local System: ```https://github.com/niteshgupta20/Phoenix-InWarranty-Flow.git```
2. Install Nodejs and npm from ```https://nodejs.org/en/download```
3. Install newman using ```npm install -g newman```
4. Install newman-reporter-htmlextra using ```npm install -g newman-reporter-htmlextra```
5. Run the newman command:
```
              newman run 'Inwarranty-Flow Collection.postman_collection.json' \
             -e QA.postman_environment.json \
             -d testdata.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html
```
