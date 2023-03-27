# Cretaceous API 

#### By E. Luckie ☀️

#### This is a follow-along project created using lessons on LearnHowToProgram.com on building an API. This API will share data about a wildlife park consisting of creatures from the cretaceous period that other developers can query.

## Technologies Used

* C#
* .NET 7.0
* API call
* RestSharp
* Newtonsoft
* Markdown
* Git

### Set Up and Run Project

1. Clone this repo.
2. Open the terminal and navigate to this project's production directory. called "CretaceousApi".
3. Within the production directory "CretaceousApi", create a new file called `appsettings.json`.
4. Within `appsettings.json`, put in the following code, replacing the `[YOUR-USERNAME-HERE]` and `[YOUR-PASSWORD-HERE]` with your own credentials for MySQL. 

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Port=3306;database=cretaceous_api;uid=[YOUR-USERNAME-HERE];pwd=[YOUR-PASSWORD-HERE];"
  }
}
```

5. Within the production directory "CretaceousApi", run `dotnet watch run` in the command line to start the project in development mode with a watcher.
6. Open the browser to _https://localhost:5001_. If you cannot access localhost:5001 it is likely because you have not configured a .NET developer security certificate for HTTPS. To learn about this, review this lesson: [Redirecting to HTTPS and Issuing a Security Certificate](https://www.learnhowtoprogram.com/lessons/redirecting-to-https-and-issuing-a-security-certificate).