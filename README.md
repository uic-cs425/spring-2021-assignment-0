# CS425 - Computer Graphics I (Spring 2021)

## Assignment 0: Introduction to JavaScript and WebGL
The goal of this first assignment is to get you familiar with JavaScript, WebGL calls, development environment, and the assignment submission process. You will develop a web application to render triangles with vertex position and colors defined in an external JSON file, specified by the user through a configuration panel.

There are five tasks, and you are free to re-use any code from the labs ([lab 1 code](https://www.dropbox.com/s/ht3hwdbd6ra9b42/gl.html?dl=1) and [lab 2 code](https://www.dropbox.com/sh/ydkn3isxt4vkuck/AAAcVd2-3w8T4hq8C_3n7g_Aa?dl=1)).

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
Connect the elements of the configuration panel and the WebGL canvas. The first four slides should change the RGBA color of the triangles, and the fifth slider should change the number of triangles being rendered (between 1 and n). The file input button should allow the users to load a JSON file; after loaded, the previous slider should be updated so that its range go from 1 to n (number of triangles in the new file). The checkbox element should toggle between two modes: 1) triangle color specified by the configuration panel, and 2) triangle color specified by loaded JSON file.

#### Task 4
The application should contain a file [input](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/file) element responsible for loading a JSON file. This JSON file will contain vertex position and color information for all n triangles. You should load this JSON file, [parse it](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse) and use the data to fill one (or two) buffer arrays. The JSON will be in the following format:

```
{"positions": [x_1,y_1,z_1,x_2,y_2,z_2,...,x_n,y_n,z_n], "colors": [r_1,g_1,b_1,a_1,r_2,g_2,b_2,a_2,...,r_n,g_n,b_n,a_n]}}
```

You can download a complete example in this repository (file [example.json](https://github.com/uic-cs425/spring-2021-assignment-0/blob/main/example.json)). In order to read the file uploaded by the user, use the [FileReader](https://developer.mozilla.org/en-US/docs/Web/API/FileReader) object, and the [onload](https://developer.mozilla.org/en-US/docs/Web/API/FileReader/onload) event handler. If by any chance a file not following the specified format is loaded, then the application should display an [alert](https://developer.mozilla.org/en-US/docs/Web/API/Window/alert).



#### Task 5
Write a README.md file with a description of the program. The goal of this file is to 1) explain how to run the program, and 2) detail the main methods and functionalities that were implemented. You are encouraged to use images and diagrams (add them to the repository), make sure to reference them in the text itself.

### Submission
The delivery of the assignments will be done using GitHub Classes. It will not be necessary to use any external JavaScript library for your assignments. If you do find the need to use additional libraries, please send us an email or Discord message to get approval. Your assignment should contain at least the following files:
- index.html: the main HTML file.
- assignment0.js: assignment main source code.
- README.md and image files: markdown readme file with a description of your program.

### GitHub Classroom
[git](https://en.wikipedia.org/wiki/Git) is a version control system, designed to help developers track different versions of your code, synchronize them across different machines, and collaborate with others. Follow the instructions [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) to install git on your computer. [GitHub](https://github.com/) is a website that supports git as a service. [This](https://guides.github.com/activities/hello-world/) a nice tutorial on how to get started with git and GitHub.

We will provide a GitHub Classroom link for each assignment. Follow the link to create a repository. Use `git clone` to get a local copy of the newly created repository. After writing your code, you can push your modifications to the server using `git commit` followed by `git push`. For example, if your username is `uic-user`:

```
git clone git@github.com:uic-cs425/assignment-0-uic-user.git
touch index.html
git add index.html
git commit -am "index.html file"
git push
```

### Grading
The code will be evaluated on Firefox. Your submission will be graded according to the quality of the image results, interactions, and correctness of the implemented algorithms.
