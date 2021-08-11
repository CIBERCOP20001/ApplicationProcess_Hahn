# ApplicationProcess_Hahn

## Prerequisites

1.- Visual studio 2019, 2022 or VS Code
2.- Powershell 7
3.- Docker Desktop
4.- Postman (optional)

## Folder structure

Solution
--SourceCode (Solution and projects)
  -- Hahn.ApplicationProcess.July2021.Web (Aurelia SPA)
  -- Hahn.ApplicationProcess.July2021.Data (Repositories and unit of work EF5)
  -- Hahn.ApplicationProcess.July2021.Domain (Models, entities, etc)
  -- Hahn.ApplicationProcess.July2021.WebApi (Web API)
--TestCode (unit test)
  -- UnitTest

## How to unzip and restore the solution

1.- Clone or download zip file
2.- Look for Hahn.ApplicatonProcess.Application.sln file and open it using VS 2019, VS 2022 or VS Code
3.- Open a command window
4._ go to source/Hahn.ApplicationProcess.July2021.Web and run "dotnet build" command
5._ go to source/Hahn.ApplicatonProcess.July2021.WebApi and run "dotnet build" command

## Create dev certificate for https

1.- Run the command "dotnet dev-certs https --clean" in Poweshell window
2.- Run the comand "dotnet dev-certs https --trust -ep $env:USERPROFILE\.aspnet\https\aspnetapp.pfx -p SECRETPASSWORD" in Poweshell window

## Run the app

1.- Goto solution folder Hahn.ApplicatonProcess.Application
2.- Run "docker-compose build" command
3.- Run "docker-compose up" command

## Test the app using browser

1.- Open a browser tab and go to the [spa app] (https://localhost:9091/)
2.- Open a browser tab ang go to [swagger page] (https://localhost:5050/swagger/index.html)

## Import the postman collection

1.- Open Postman and Import the WebApi.postman_collection.json file