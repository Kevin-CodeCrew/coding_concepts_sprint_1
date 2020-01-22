# Using an IDE

## Source Code
Programs in all programming language start out as text files. The text files hold the instructions to execute (source code) and are named according to the development language being used. The file name extension (the characters after the dot) tip off the tool being used to edit/compile/execute as to how to handle the file.

Examples of Program File Names
1. `HelloWorld.java` - Java
1. `HelloWorld.html` - HTML
1. `HelloWorld.js` - JavaScript
1. `HelloWorld.py` - Python

## Integrated Development Environments (IDE)
Since source code is simply a text file, and text editor can be used to create/modify/view their contents. However, when developing software there are special tools that are required to test/debug/run your code. The types of tools are determine by the programming language you are using. 

The IDE goes a step further than your standard text editor by allowing the developer to add or integrate any additional tools and plugins directly into the environment so that you can perform all your development tasks from a single place.

IDEs also provide other conveniences like programming language syntax coloring and code formatting to make it easier for you to develop code.

## Practice
Create a new file in your home directory called `helloworld`

`code helloworld`

Add the following HTML to the new file then save it

```
<html>
<head>
<title>Hello World!</title>
</head>
<body>
<h1>Hello World!</h1>
</body>
</html>
```

Notice how the code remains monocolored. It is treated as plain old text because it does not recognize that it is HTML
> **Insert screenshot**

Use the `save as...` command from the `File` menu to save the file using the name `helloworld.html`

Notice how the HTML tags are now in color. This is known as `syntax highlighting`. It makes it much easier for developers to read the source code and spot errors. 

Now that the IDE can recognize that it is an HTML file it will make other features available. 

Right click in the editor window and select `Format Document` and you will see that the IDE will format it as HTML for easier reading.
> **Insert screenshot**
