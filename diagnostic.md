# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.

What is the purpose of a backend?

```md
The purpose of a backend is to respond to user requests from the client. These
responses usually are the result of accessing a database to save or modify
stored data.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```md
The model is used by the controller to fetch data.
```

Which layer in the MVC pattern communicates with the model?

```md
The controller communicates with the model.
```

Why don't we use views in our interpretation of the MVC pattern?

```md
Serializers replace views but not sure what serializers are or why they replace views.
```

What does C.R.U.D stand for?

```md
Create, Read, Update, Delete
```

In which part of the MVC pattern can we find C.R.U.D actions?

```md
The controller responds to the user requests with specific CRUD actions.
```

List at least 5 standard rails actions that C.R.U.D requests correspond to?

```md
1. #signup
2. #signin
3. #changepw
4. #signout
5. #index
```

A user action fires a `GET` request for `/people/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list)

```md
1. The client sends a GET request to the base_URI + '/people/1'
2. The Rails router sends the request to the appropriate controller (people:#show)
3. The controller performs the #show action by asking the person model for the record of the person with id = 1.
4. The model returns the data to the controller.
5. The controller converts the data to a JSON object and returns it to the view.
6. The view formats the data object for presentation to the client.
```

What is the command to generate a new rails-api app?

```bash
bin/rails generate scaffold <table_name col_name:type,...>
```

What is the command to start an instance of a rails server?

```bash
bin/rails server
```

What are the commands to drop, create, migrate and seed a database from the command
line? (5 bullet points)

```bash
bin/rake db:drop
bin/rake db:create
bin/rake db:migrate
bin/rake db:seed
bin/rake db:examples
```

What is the command to scaffold a pet with a name and age attributes (hint:
Also think of the data types for each attribute)?

```bash
bin/rails generate scaffold pet name:string age:number
```
