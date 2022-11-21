# Image processing API

+ An API that can be used in two different ways. As a simple placeholder API, the first allows you to place images into your frontend with the size set via URL parameters (and additional stylization if you choose) for rapid prototyping. The second use case is as a library to serve properly scaled versions of your images to the front end to reduce page load size. Rather than needing to resize and upload multiple copies of the same image to be used throughout your site, the API you create will handle resizing and serving stored images for you.

## Objective
This project aims to give we a real-world scenario in which we would read and write to our disk via a Node.js express server rather than a database. The project we create serves two purposes: to prepare us for setting up scalable code and architecture for real-world projects and tie together some of the most popular middleware and utilities found in Node.js projects. This project barely touches the surface of what is possible but will prove your ability to use what you’ve learned in real-world scenarios.

## Approach
+ Resize any image of jpg format by name and customized width and height as parameters in the URL.
+ The output image will retain the same name as the original, created on the width and height specified in the parameters. for identification.
+ In the case of image being existing prior to creation, the server responds with the existing image, instead of processing it again to avoid rredundant execution of the script.

## Local execution
- GitHub url:  ```git clone https://https://github.com/vamshi-krishna-prime/image-processing-api```
- Run ```npm i```

## Testing
- Run ```npm run test``` to run the tests stablished in ```tests``` with names *Spec*.ts.
- Testing is implemented with jasmine
- ScreenShot of executed test cases is: ![TestCase SS](../images/testcase-ss.png)

## Run developer server
- Run ```npm run start-dev```
- The project includes nodemon so any modifications made to a file saved will restart the server.


## Build the project
- Run ```npm run build```
- Compile the code and create `js` fie to dist.


## Run project and Validate image API's
- Start the app with ```npm run start```
- Run all the script created to run app.
- Script execution: ```"start": "npm run prettier && npm run lint && npm run test && npm run start-dev"```
- Resize `.jpg` image: ```assets/images/input-files```.
- URL: ```http://localhost:3000/api/image``` and set the name of the image (filename) and the desired width and height as parameters, for example: ```http://localhost:3000/api/image?filename=fjord&width=900&height=900```
- Resized image is reflected in the browser at location: ```assets/images/output-files```
![fjord SS](../images/fjord-900-900.png)