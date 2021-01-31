# CS425 - Computer Graphics I (Spring 2021)

## Assignment 0: Introduction to JavaScript and WebGL
The goal of this first assignment is to get you familiar with JavaScript, WebGL calls, development environment, and the assignment submission process. You will develop a web application to render triangles with vertex position and colors defined in an external JSON file, specified by the user through a configuration panel.

There are four tasks, and you are free to re-use any code from the labs ([lab 1 code](https://www.dropbox.com/s/ht3hwdbd6ra9b42/gl.html?dl=1) and [lab 2 code](https://www.dropbox.com/sh/ydkn3isxt4vkuck/AAAcVd2-3w8T4hq8C_3n7g_Aa?dl=1)).

### Tasks

#### Task 1
Create a configuration panel with seven elements:
1) Four [sliders](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/range) with values between 0 and 255.
2) A [slider](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/range) with value between 1 and n, where n is the number of triangles in the file specified by the user.
3) A file [input](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/file) element responsible for loading a JSON file.
4) A [checkbox](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/checkbox) element to toggle between the colors of the triangles.

You are free to choose the layout and color of the configuration panel elements.

#### Task 2
Create a WebGL canvas that will display the rendered triangles.

#### Task 3
Connect the elements of the configuration panel and the WebGL canvas. The first four slides should change the RGBA color of the triangles, and the fifth slider should change the number of triangles being rendered (between 1 and n). The file input button should allow the users to load a JSON file; after loaded, the previous slider should be updated so that its range go from 1 to n (number of triangles in the new file). The checkbox element should troggle between two modes: 1) triangle color specified by the configuration panel, and 2) triangle color specified by loaded JSON file.

#### Task 4
The application should contain a file [input](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/file) element responsible for loading a JSON file. This JSON file will contain vertex position and color information for all n triangles. You should load this JSON file, [parse it](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse) and use the data to fill one (or two) buffer arrays. The JSON will be in the following format:

```
{"positions": [x_1,y_1,z_1,x_2,y_2,z_2,...,x_n,y_n,z_n], "colors": [r_1,g_1,b_1,a_1,r_2,g_2,b_2,a_2,...,r_n,g_n,b_n,a_n]}}
```

You can download a complete example in this repository (file example.json). If by any chance a file not following the specified format is loaded, then the application should display an [alert](https://developer.mozilla.org/en-US/docs/Web/API/Window/alert).

### Submission
The delivery of the assignments will be done using GitHub Classes. It will not be necessary to use any external JavaScript library for your assignments. If you do find the need to use additional libraries, please send us an email or Discord message to get approval.

### Grading
The code will be evaluated on Firefox. Your submission will be graded according to the quality of the image results, interactions, and correctness of the implemented algorithms.
