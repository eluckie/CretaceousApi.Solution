# Cretaceous API 

#### By E. Luckie ☀️

#### This is a follow-along project created using lessons on LearnHowToProgram.com on building an API. This API will share data about a wildlife park consisting of creatures from the cretaceous period that other developers can query.

## Technologies Used

* C#
* .NET 7.0
* API
* Postman
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

5. Within the production directory "CretaceousApi", run `dotnet run` in the command line to start the project in development mode.

### Endpoints

GET http://localhost:5000/api/animals/

GET http://localhost:5000/api/animals/{id}

POST http://localhost:5000/api/animals/

PUT http://localhost:5000/api/animals/{id}

DELETE http://localhost:5000/api/animals/{id}

### Optional Parameters

| Parameter | Type | Required | Description |
| --------- | ----- | ------- | ----------- |
| species | string | not required | returns animals with a matching species value |
| name | string | not required | returns animals with a matching name value | 
| minimumAge | number | not required | returns animals than have an age value that is greater than or equal to the specified minimumAge value | 

#### Example Queries
* The following query will return all animals with a species value of "Dinosaur":
```GET http://localhost:5000/api/animals?species=dinosaur```

* The following query will return all animals with the name "Matilda":
```GET http://localhost:5000/api/animals?name=matilda```

* The following query will return all animals with an age of 10 or older:
```GET http://localhost:5000/api/animals?minimumAge=10```

* It's possible to include multiple query strings by separating them with an `&`:
```GET http://localhost:5000/api/animals?species=dinosaur&minimumAge=10```

### Additional Requirements

#### for POST request

When making a POST request to `http://localhost:5000/api/animals/`, you need to include a **body**. Here's an example body in JSON:

```json
{
  "species": "Tyrannosaurus Rex",
  "name": "Elizabeth",
  "age": 8
}
```

#### for PUT request
When making a PUT request to `http://localhost:5000/api/animals/{id}`, you need to include a body that includes the animal's `animalId` property. Here's an example body in JSON:

```json
{
  "animalId": 1,
  "species": "Tyrannosaurus Rex",
  "name": "Lizzy",
  "age": 9
}
```

And here's the PUT request we would send the body to:

`http://localhost:5000/api/animals/1`

Notice that the value of `animalId` needs to match the id number in the URL. In this example, they are both 1.