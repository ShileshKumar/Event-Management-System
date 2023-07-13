# Event Management System

## Home Page
![Event Management System](https://user-images.githubusercontent.com/92677342/201507545-7f4b62dd-e31a-4f77-9777-71734b620ce7.png)
## Registration Page
![image](https://github.com/ShileshKumar/Event-Management-System/assets/55770859/0b508898-0ba6-409a-8105-29f9de260b0d)


## Technologies Used :
- Flask / Python
- MySQL
- HTML5
- Docker
- Jenkins
  
## ER Diagram
![ER-Diagram](https://user-images.githubusercontent.com/92677342/201560821-96115972-5b09-4cb1-8c4e-c367c2ce047f.png)


## Creating the environment

```
$ git clone https://github.com/ShileshKumar/Event-Management-System.git
```

```
$ sudo mysql -uroot -p
```


`Create the database by copying the contents of ./database/events.sql and executing them`


`Change password in app.py to your MySQL root password`

## Installing Dependencies

```
$ pip install -r requirements.txt
```

## Running the project

```
$ flask run
```

- `Open` [http://127.0.0.1:5000](http://127.0.0.1:5000)

## Dockerizing the Event Management System

To dockerize the Event Management System, follow these steps:

#### Step 1: Clone the Repository
Clone the project repository to your local machine using the following command:
```
git clone https://github.com/ShileshKumar/Event-Management-System.git
```
#### Step 2: Navigate to the Project Directory
Navigate to the project directory using the following command:

```
cd Event-Management-System
```
#### Step 3: Create a Dockerfile
Create a file named Dockerfile in the project directory and add the following content:
Dockerfile
```
#Base image
FROM python:3.8-slim-buster

#Set the working directory
WORKDIR /app

#Install dependencies
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

#Copy the application code
COPY . .

#Expose the application port
EXPOSE 5000

#Start the application
CMD ["python", "app.py"]
```
#### Step 4: Create a requirements.txt File
In the project directory, there is already a requirements.txt file. Open it and ensure that it contains all the necessary dependencies for your Event Management System.

#### Step 5: Build the Docker Image
Build the Docker image using the following command:
```
docker build -t event-management-app .
```
#### Step 6: Run the Docker Container
Start a container based on the built image using the following command:
```
docker run -p 5000:5000 event-management-app
```
#### Step 7: Access Your Event Management System
Open a web browser and navigate to [http://localhost:5000](http://localhost:5000) to access your Event Management System.

By following these steps, you will be able to dockerize your Event Management System.
