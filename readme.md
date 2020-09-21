# MLOps Project

This project is a web application created using django in python which accepts video feeds from different sources and checks the distance between the people present in the video feed and also checks if the people are wearing a mask or not. An alert is raised when either a person is not wearing a mask or is not following social distancing.
Jenkins is used for CI/CD and a machine learning model is used for mask detection.  <br/>Complete video Description of project is - [Video Description](https://drive.google.com/file/d/1kCUVkRA0dc2doaRP8X_56rg1ZLFcVg18/view?usp=sharing)

# CI/CD

The CI/CD has two tasks 

 1. get_dist_code_proj
 2. run_dist
 
![Job Pipeline](https://github.com/narayanhari/dist/blob/master/114.jpeg)
 
 get_dist_code_proj fetches source data from github and copies it to a desired location in the base os.
 
![get_dist_code_proj (1)](https://github.com/narayanhari/dist/blob/master/121.jpeg)

![get_dist_code_proj (2)](https://github.com/narayanhari/dist/blob/master/122.jpeg)

run_dist task runs the server code. This task runs automatically if the build of the get_dist_code_proj task is stable. The server will run on port 8000 of the base os.

![run_dist (1)](https://github.com/narayanhari/dist/blob/master/118.jpeg)

![run_dist (2)](https://github.com/narayanhari/dist/blob/master/119.jpeg)
> note: run_dist will execute until the server is running and stopping this task will result in stopping the server

# Start server

To start the server following steps need to be followed:

### setup environment
Before the actual code is run the environment needs to be setup.
To achieve that run the following code.

> pip3 install -r requirements.txt

 ### Run Code
 To start the server run the following code.
 The server will run on port 8000 of the base os.

> python3 manage.py runserver --nothreading --noreload

 

## Website tour

![LoginPage](https://github.com/narayanhari/dist/blob/master/Screenshot%20%28123%29.png)

> username : **omkar**
>
> password : **Omkar2107@**

![FeedPage](https://github.com/narayanhari/dist/blob/master/Screenshot%20%28124%29.png)

![Video1](https://github.com/narayanhari/dist/blob/master/Screenshot%20%28125%29.png)
no mask

![Video2](https://github.com/narayanhari/dist/blob/master/Screenshot%20%28127%29.png)
no mask , no social distance

![Video3](https://github.com/narayanhari/dist/blob/master/Screenshot%20%28129%29.png)
mask and social distance
