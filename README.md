## FashionMnist_API

### Solution to host a CNN model generated from Fashion MNist dataset in a flask application and expose it as an endpoint.

### Requirements
  1) Make sure you have docker installed on your machine. 
  2) Refer to this link for docker installation steps https://docs.docker.com/engine/install/

## Usage

 1) Download the zip or clone the repo using your local git
 2) Open terminal on your local machine
 3) Navigate to the root folder
 4) Run the following docker command to build the image

```
  docker build -t fashion_image 

```
4) Then you need to create a docker container from the image by running this command

```
docker run -p 5000:5000 fashion_image
```

5) The container will boot up and listen to port 5000


## Testing

There are 2 ways to test this endpoint

1) The easiest way is to use the included python notebook  ('https://github.com/behrahub/FashionMnist_API/blob/master/fashion_mnist_model_generation.ipynb')
2) Run the entire notebook which will setup the test data.
3) At the bottom of the notebook, you have a test infrastructure which will hit the local container. 

1) The second way to test is via http test clients such as postman
2) Do a post request to the url ('http://127.0.0.1:5000/predict') and in the form body submit a image file. 


    

