---
layout: post
title: Flask restful API
---
A restful API is a starndard interface through which application services can be
accessed. After building an application that offer some services, it can be wrapped
in an api and deploy on some server where the wervices can be remotely accessed. In this,
I briefly go through the steps required to develop restful API using flask.
The steps can be summarized as follows:
1. Load the required libraries

        from flask import Flask, requests
        from flask_restful import Resource, Api

2. Instantiate flask app and wrap it in an API

        app = Flask(__name__)
        api = Api(app)

3. create the Resource

        class HelloWorld(Resource):
            def get(self):
              return "Hello World!"

            def post(self):
              json_data = request.get_json(force=True)

4. add resource to the wrapped app

        api.add_resource(HelloWorld,'/key')

5. set up the app to run as main

        if __name__ = "__main__":
          app.run(debug==true)

Having served up the website, it is time for the user to ping the api.

There are many ways to do this:

        curl -H "Content-Type : application/json" -H "Accept : application/json" -X POST
        --data "{"recipes" :{"101":"Abe"}}" http://localhost:5000/rec

- The first header above `-H` tells Flask that we are expecting a JSON input so we
can easily use flask.request() to extract our data which is specified with `--d`

- The second header tells flask that we are also expecting it to serve our query in
json.

- -X POST is a bit redundant as it tells flask that this is a POST request.

Alternatively, the first header can be removed as below in which case we get an error.
This is because flask does not know what the content type is.
However, to tell flask to parse the data as JSON nevertheless, we use [flask.request.get_json(force=True)](https://flask.palletsprojects.com/en/1.1.x/api/#flask.Request.get_json)

        curl -H "Accept : application/json" -X POST
        --data "{"recipes" :{"101":"Abe"}}" http://localhost:5000/rec

Finally, we can still remove the final header by jsonifying the returned value.

        curl -X POST
        --data "{"recipes" :{"101":"Abe"}}" http://localhost:5000/rec

[JSON](https://stackoverflow.com/questions/10434599/get-the-data-received-in-a-flask-request)
[pasre ]
