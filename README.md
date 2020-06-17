# GoLang_ReactJS_Todolist


A simple application using Go, React and MongoDB

![golangapp](https://user-images.githubusercontent.com/48954255/84936872-4d409700-b0b1-11ea-9d90-c69c67742451.jpg)


_________________
# Server Side 
![Badge](https://img.shields.io/static/v1?label=Language&message=GoLang&color=blue&style=plastic&logo=GOLANG)


Open server folder

We are going to use the official MongoDB Go Driver from MongoDB.
To install it run the below command in the terminal or command window.
````
go get go.mongodb.org/mongo-driver
````

Second, install the gorilla/mux package for the router. mux is one of the most popular packages for the router in the Golang.
To install it run the below command in the terminal or command window.
````
go get -u github.com/gorilla/mux
````

### MongoDB Set up
First set up the MongoDB connection.
Here I am using MongoDB Atlas for the demo. You can sign up for free tier, it gives you 512MB of storage, that is more than enough for learning purpose.
Sign up for MongoDB Atlas. Follow the link instructions.
Once you have your cluster ready, a few things need to be done.

First, white list your IP address.

* Click on “Network Access” under “Security”.
* Click “ADD IP ADDRESS” and select “ADD CURRENT IP ADDRESS”. This will allow only your computer to interact with it.

![atlas_mongo](https://miro.medium.com/max/2000/1*C7nfL2-4BU4v2DlpuxRtow.png)

Second, create a user. You can learn more about the user in this link.

* Click “Database Access” under “Security” and create a new user.
* I have admin as a user.

![atlas_mongo](https://miro.medium.com/max/2000/1*AbdyOLCDGCDb57YKSU2sQQ.png)

Now, its time to get the connection string.

* Go to “Cluster” and click “connect” and then “Connect Your Application”.
* Copy the connection string and paste it in connectionStringin middleware.go

![atlas_mongo](https://miro.medium.com/max/2000/1*QP82h8R88HQz_ZOQ_hRS2Q.png)

* Replace <password> with the password for the mongodb user. 
* Replace <dbname> with the name of the database that connections will use by default. 
Ensure any option params are URL encoded.

Open the terminal from the server directory and run the below command to serve the server. 
You’ll see the output as the image.

````
go run main.go
````

![cmd](https://user-images.githubusercontent.com/48954255/84941803-42d5cb80-b0b8-11ea-9a1d-79c1a06447f3.jpg)



_____________________
# Cliet Side
![Badge](https://img.shields.io/static/v1?label=framework&message=react&color=blue&style=plastic&logo=REACT)


Now open client folder and follow the steps for run the client side in your machine.


In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

