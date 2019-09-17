# form-test

This is a code test to create an application to see how the components work in Vue and how you can create a preview of what you want in real time.

## To install the application once downloaded
```
npm install
```

### To run the application once everything is installed
```
npm run serve
```

### Overview

The application is made with Vue CLI 3, so it will run on the localhost port:8080.

The application has two components, 

A first component parent (App) or also called Builder in the application that collects the information passed by the user in several inputs.

And a second component child (Preview) that is responsible for painting the information collected by the parent. 

As information we have a name, a description, an image that is painted when a correct url image is passed and the transformation of a net hourly wage into a gross monthly wage.

### Future versions of the application

1. Implement an improvement to see if the url of the image is correct and warn the user directly with an icon or visually that the url you are entering can not be transformed into an image.

1. Implement improvement in writing the description, you can justify the text and each time you write more text can be made smaller, allowing the user to enter the text he wants.

1. Improve the function of salary to convert, being able to select hours or months, or total annual salary, also to make a converter that transforms directly the salary to other currencies.

1. Improve the mobile version implementing a grid that allows you to see the application on mobile without losing detail.

1. Download the preview in the form of pdf or jpg image, to save it or publish it directly on social networks.
