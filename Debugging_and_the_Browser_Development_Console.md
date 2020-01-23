# Debugging and the Browser Development Console
Debugging your code is one of the most crucial skills as a developer. Several tools are at your disposal to assist you in this effort. 

## Browser Developer Console
All modern IDEs provide advanced debug capabilities, but today's web browsers all also include debugging facilities. While not on par with what you may get from your IDE, the built-in web browser development console is a powerful tool and will be used extensively in class.

How you access the development console for a given browser depends on the browser you are using, but in general, if you right-click on the web page you need to debug you can select `Inspect Element`from the popup menu and the tool will display.

### Inspecting the DOM
The inspection tool allows you to look at the details of all objects being rendered in the browser. This view is super useful when debugging issues with the display of your web pages. 

Highlighting an object in the document object model (discussed more later) will give you all details about the element including styling (CSS) details. The developer consoles in browsers even allow you to temporairly edit the details of the document displayed so you can determine the exact settings you want for the display you desire.

> Note that changes in the developer console DO NOT actually modify the source code that generated the output. The changes are just temporary and meant for debugging and tweaking your styling.

![The Firefox Developer Tool](./img/ff_developer_tools.png)

### Reading Errors
Regardless of the programming language. When an error occurs, it will return a stack trace. A stack trace shows the last few areas of code that led up to the error being generated, including the line of code where the crash occurred. 

Sometimes a stack trace looks scary, but just start at the bottom of the output and work your way up. Some of the code referenced might not be code you wrote and instead be code in the tool or framework you are using. 

Look for clues in the stack trace output that give you a better idea of where therror occurred and why. Most stack traces will include actual line numbers from the source code file where the error was encountered. Watch out for them and start your debugging search there.

### Network Tab
Internet applications consists of several requests/responses. Even though you are viewing a single web page, far more than one network request is being made to retrieve all the code, images, and other linked items via a network protocol called HTTP (HyperText Transport Protocol). Each HTTP request returns a status code, along with the requested data (when request successful). 

[HTTP Status Codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes)

## Debugging Code in the Browser
When your web page doesn't display as expected in the browser, the first thing to do is popup the developer tools and check the `console` tab.

The `console` tab will display any exceptions generated while attempting to render the page. The tool is especially when JavaScript is being used. Should an exception (error) occur in your code, the console will display what is called a `stack trace`. A stack trace shows you the last lines of code that were executed leading up to the error. 


### console.log

### debugger

### Breakpoints

## Debugging in Visual Studio Code

## Exception Handling

### try/catch


