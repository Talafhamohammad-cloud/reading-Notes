# Reading 06 summery

***the first part of reading is talking about OBJECTS and is def and we can conclude that objects are group of variables and functions and we call the variables property and the functions are methods and we can creating objects by using literal notation***
**example of and object using literal notation**

 var person = {

  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;

  }
 };

## we can accessing the property by using square brackets also we can accesss methods and proprty by dot(.) notation

**the second part of this reading is talking about document object model (D O M)**
which is in general about how the browsers should creat model of an HTML pages and how javascrpit can access and ubdate the contents of the webpage while its in the browser window and some time we call DOM is API or application programming interface  the basic model of the web page is called DOM tree and we can find the elements in DOM tree by using DOM queries.

*DOM tree example:*

<!DOCTYPE HTML>
< html >
< head >
  < title >About</title>
</head>
< body >
  The truth about
</body>
</ html >

*DOM queries methods:*

1- document.getElementById(id)
2- document.getElementsByClassName(className)
3- document.getElementsByTagName(tagName)
4- document.querySelector(cssSelector)
5- document.querySelectorAll(cssSelector)
