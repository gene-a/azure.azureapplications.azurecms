# Article CMS (FlaskWebProject)

This project is a Python web application built using Flask. The user can log in and out and create/edit articles. An article consists of a title, author, and body of text stored in an Azure SQL Server along with an image that is stored in Azure Blob Storage. Authentication is done through OAuth2 with Sign in with Microsoft using the `msal` library. App logging is done using Flask calls to the base Python logger. The purpose of this project is to learn how to integrate Azure Compute Services with Azure Storage Services alongside basic logging + metrics within the platform.

## App URL:
- https://azurecmsapp.azurewebsites.net

## Dependencies

Python 3.7 or later
Python dependencies in requirements.txt
