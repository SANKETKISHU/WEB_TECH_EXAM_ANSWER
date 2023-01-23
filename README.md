# WEB_TECH_EXAM_ANSWER
ALL QUESTION/ANSWER



1.	Define the following schema in My SQL EMP (Eno name, add, Sal, dept). 
CREATE TABLE EMP (
    Eno INT PRIMARY KEY,
    name VARCHAR(255),
    add VARCHAR(255),
    sal DECIMAL(10,2),
    dept VARCHAR(255)
);
Write a php program to execute the following query and show the result. 
Query1: show name of all employees who are working in research and marketing. 
<?php
$conn = mysqli_connect("host", "username", "password", "database");
$result = mysqli_query($conn, "SELECT name FROM EMP WHERE dept='research' OR dept='marketing'");
while ($row = mysqli_fetch_assoc($result)) {
    echo $row['name'] . "<br>";
}
?>
Query2: update salary to 7.5 who belongs to sales department and name is Ravan. 
<?php
$conn = mysqli_connect("host", "username", "password", "database");
$result = mysqli_query($conn, "UPDATE EMP SET sal=7.5 WHERE dept='sales' AND name='Ravan'");
?>



Query3: insert few records in the database. 
<?php
$conn = mysqli_connect("host", "username", "password", "database");
$result = mysqli_query($conn, "INSERT INTO EMP (Eno, name, add, sal, dept) VALUES (1, 'John', 'New York', 50000, 'research'), (2, 'Jane', 'Los Angeles', 60000, 'marketing')");
?>
 
 

2. WAP in JavaScript to add two numbers. 
<!doctype html>
<html>
   <head>
      <script>
         function add()
         {
           var num1, num2, sum;
           num1 =parseInt(document.getElementById("firstnumber").value);
           num2 =parseInt(document.getElementById("secondnumber").value);
           sum = num1 + num2;
           document.getElementById("answer").value = sum;
         }
      </script>
   </head>
   <body>
      <p>First Number: <input id="firstnumber"></p>
      <p>Second Number: <input id="secondnumber"></p>
      <button onclick="add()">Add Them</button>
      <p>Sum = <input id="answer"></p>
   </body>
</html>

 
Or 
function add(a, b) {
    return a + b;
}
console.log(add(2, 3));
3. Advantages of HTML5 over html 4
‘HTML 5 is the latest version of HTML which is the core markup language of the World Wide Web that can be written in both HTML (HTML 5) and XML (XHTML 5) language.’
In this newest version of HTML, a number of APIs have been added such as Timed media playback, Canvas element, Offline storage database, Document editing, Drag-and-drop, Cross-document messaging, Browsing history management etc. that shapes the foundation of Web architecture.
Know some more about HTML 5
HTML 5 allows utilizing new structural elements and attributes, replacing some of the familiar elements. Moreover it’s providing some fresh functionality like audio and video elements which will offer an easy way to semantically structure the page.
‘HTML 5 is specially designed in order to meet the changing Web 2.0 world.’
This new markup language arrives with a simpler and classier way of exhibiting the web design for the website. At present the new CSS3 changes are not supported by all the though browsers like Firefox 3, Safari 4, Chrome 2, Opera 10, etc. are supporting the new design modifications.
Why HTML 5?
HTML 5 is developed to grant the developers a means to build up more flexible, powerful and efficient applications. It overcomes the lacking issues related to HTML 4 and brings in many new tags and enhancements for a broad range of features including form controls, APIs, multimedia, structure, database support and faster processing. Following are the new APIs included in HTML 5:
 
The Canvas element for immediate mode 2D drawing
Offline storage database
Geo-Location
Document editing
Drag-and-drop
Cross-document messaging
MIME type and protocol handler registration
Browser history management
Indexed hierarchical key-value store
Microdata
Local and Web SQL Database
Timed media playback
Indexed Database API
Direct HTML Support for Drawing, Animation, Video and Audio
HTML 5 Benefits
 
Following are the benefits of HTML 5 making it more compatible than HTML 4:
Better Consistency
The new HTML 5 will provide a far better consistency in terms of HTML code which is used to design a web page thus making it easier to grasp the structuring of a web page for web designers and developers.
Cleaner Code
HTML 5 will allow developers to make use of a cleaner code. New structural elements like article tag and section tag are introduced replacing most div tags.
Client side database
HTML 5 will offer a new SQL-based database API to facilitate data storage locally i.e. client side. By using a real SQL database, a developer can save structured data on the client side. One can stock up the structured data temporarily as it’s not a permanent database. Even when the client is disconnected for a short time period, data can be accessed without any difficulty.
Enhanced Accessibility
HTML 5 new elements improve the accessibility by making it possible for assistive technologies to spread out the features offered by them to the users.
Geo-Location
Any HTML 5 compatible browser-based application can be directly used for finding out a location with the new HTML 5 geo-location APIs. The Google Latitude for the iPhone can be considered as a fine example of it.
Improved Semantics
The semantic values of all web pages will be improved due to the usage of new standardize elements of HTML 5 for coding a web page making it easy to notice various divisions of the web page such as headers, nav, footers, aside, etc.
Interactivity
The greatest benefit of HTML 5 is that the functionality is built into the browser. HTML 5 resolves the web application complexity issues with DOM and HTML support, for high-quality drawings, video & audio embedding, charts & animation and many other types of rich content required by users.
Sharper focus on Web application Requirements
HTML 5 is designed for making search front-ends easier to construct. Functionalities like real-time chat, drag & drop tools, discussion boards etc. are available with more efficiency.
Superior forms
New enhanced forms are introduced with up gradations in text inputs, search boxes and other fields providing better controls for data validation and interaction on the page.
Thread-like Operations
‘Web workers’ is a tool that enables faster thread-like processing with coordination using message-passing.
HTML 5 will free the multimedia content. It will be harder to differentiate between web applications and desktop applications and will surely be a step towards the future of internet.

4. Why content and design of web docs are separated from each other? 
In many cases, the design and development aspects of a project are performed by different people, so keeping both aspects separated ensures both initial production accountability and later maintenance simplification, as in the don't repeat yourself (DRY) principle.
In addition, separating content from design allows the content to be reused in different contexts, such as in different languages, or in different media, such as print or audio.
5. Develop the home page according to this structure: Main Left. Footer 
 
 
Or 
<div id="main">
    <div id="left">
        <!-- Left content goes here -->
    </div>
</div>
<footer>
    <!-- Footer content goes here -->
</footer>
6. WAP in JavaScript to test whether name is empty and phone number having only 10 digits. 
function checkInput(name, phone) {
    if (name.length === 0) {
        console.log("Name is required.");
        return false;
    }
    if (phone.length !== 10) {
        console.log("Phone number must have 10 digits.");
        return false;
    }
    return true;
}
console.log(checkInput("John", "1234567890")); // true
console.log(checkInput("", "123456789")); // Name is required.
console.log(checkInput("Jane", "123456789023")); // Phone number must have 10 digits.


7. Declare one div element, change by color, show border, put margin using CSS 
<div id="myDiv">Content goes here</div>

<style>
#myDiv {
    background-color: blue;
    border: 1px solid black;
    margin: 20px;
}
</style>
8. Difference between div and span and float and over float 
The div element is a block-level element, meaning it takes up the full width of its parent container and creates a new line after it. The span element, on the other hand, is an inline element, meaning it only takes up as much width as its content and does not create a new line.
float property is used to make elements float to left or right of the parent element, and overflow property is used to control how content behaves when it overflows its bounds.
1. The div tag is used to create a division or a section in an HTML document.  2. The span tag is used to group inline-elements in a document.
 3. The float property is used to take an element in normal flow and place it as far to the left or right of the containing element as possible. 
 4. The overflow property specifies what happens if content overflows an element's box.




9. WAP in to test whether password is alphanumeric 
function isAlphaNumeric(password) {
    let alphaNumeric = /^[a-zA-Z0-9]+$/;
    return alphaNumeric.test(password);
}
console.log(isAlphaNumeric("password123")); // true
console.log(isAlphaNumeric("password!")); // false
10. Illustrate the box model of div 
The box model of a div element in CSS refers to the layout of the element, which consists of the content, padding, borders, and margins. The content is the innermost part of the box and is the area where text or images are placed. The padding is the space between the content and the border. The border is the outermost part of the box and is the line that surrounds the content and padding. The margin is the space outside the border and determines the distance between the element and other elements on the page.

11. Discuss image size and visualization size in terms of performance of website. 
1. Use concise and direct image names.
2. Optimize your alt attributes carefully.
3. Choose your image dimensions and product angles wisely.
4. Resize your images.
5. Choose the right image format.
6. Optimize your thumbnails.
7. Use image sitemaps.
8. Beware of decorative images.
Image size and visualization size can affect the performance of a website in several ways. The file size of an image can affect the load time of a website, as larger images will take longer to download. This can cause a delay in the page rendering, leading to a poor user experience. Additionally, using large images that are not optimized for web use can cause a website to consume excessive memory and slow down the performance of the browser. Visualization size refers to the dimensions of the image on the page, the larger the size of the visualization the more memory is consumed and will affect the performance of the website.
12. Point out asthenic issue of image 
1. Use concise and direct image names.
2. Optimize your alt attributes carefully.
3. Choose your image dimensions and product angles wisely.
4. Resize your images.
5. Choose the right image format.
6. Optimize your thumbnails.
7. Use image sitemaps.
8. Beware of decorative images.

Asthetic issues of image include:
a. Poor resolution or quality of the image
b. Incorrect color balance or contrast
c. Incorrect cropping or composition
d. Incorrect file format
e. Excessively large file size
13. Apply the image map 
 
An image map is a way to create multiple clickable areas on a single image. This can be useful for creating interactive images where different areas of the image correspond to different links. To create an image map, you can use the map and area elements in HTML. Example:

<img src="image.jpg" usemap="#mapname">

<map name="mapname">
  <area shape="rect" coords="0,0,100,100" href="link1.html">
  <area shape="circle" coords="150,150,50" href="link2.html">
</map>
14. Write code to apply the same style in one para and in one H1 
p, h1 {
    color: blue;
    font-size: 16px;
    font-family: Arial;
}
15. XML schema is static or dynamic? Explain 
XML Schema is a static schema. It is a static schema because it is defined before the XML document is created.
XML schema is a static structure that defines the elements, attributes, and relationships of an XML document. It is used to define the structure of an XML document and ensure that the document adheres to a specific format. It is a way to define the structure of an XML document and ensure that the document adheres to a specific format.
16. How organizing data into XML is different from relational model / relational DBMS 
Organizing data into XML is different from a relational DBMS in several ways:

a. XML is a markup language that is used to describe the structure and content of a document, while a relational DBMS is a database management system that is used to store and retrieve data.
b. XML data is often hierarchical in nature, with a parent-child relationship between elements, while relational data is organized into tables with rows and columns.
c. XML data can be self-describing, meaning that the structure and meaning of the data is embedded within the document, while relational data relies on a separate schema to define the structure of the data.
d. XML data can be queried using XQuery or XPath, while relational data is queried using SQL.
e. XML data can be easily exchanged between different systems, while relational data is typically stored within a specific database management system.

1. XML is a markup language, while relational DBMS is a database management system.
2. XML is a data format, while relational DBMS is a data storage system.
17. Advantages medical data processing using xml 
Advantages of medical data processing using data include:
a. Improved patient care: Medical data can be used to identify patterns and trends in patient health, which can help healthcare providers make more informed decisions about patient care.
b. Efficiency: Automated data processing can help reduce administrative tasks and improve the efficiency of medical practices.
c. Cost savings: Medical data can be used to identify inefficiencies in healthcare delivery, which can lead to cost savings for both patients and healthcare providers.
d. Improved research: Medical data can be used to conduct research on disease patterns, treatment effectiveness, and other areas of medical science.
18. Explain class selector 
In CSS, a class selector allows you to select elements with a specific class attribute. A class attribute is added to an HTML element using the class attribute. For example:

<p class="myClass">This is a paragraph.</p>

You can then use the class selector in CSS to apply styles to all elements with the class attribute "myClass":

.myClass {
    color: blue;
    font-size: 16px;
}
19. Could you add one attribute at runtime in XML schema? Explain 
Yes, it is possible to add an attribute to an XML schema. In an XML schema, an attribute is defined using the <xs:attribute> element. The attribute can be added to an element using the name and type attributes. For example, to add a "color" attribute to an "item" element, you can use the following code snippet:

<xs:attribute name="color" type="xs:string"/>


20. Explain ID selector of CSS 
In CSS, an ID selector allows you to select a specific element with a unique ID attribute. An ID attribute is added to an HTML element using the id attribute. For example:

<p id="myID">This is a paragraph.</p>

You can then use the ID selector in CSS to apply styles to the specific element with the ID attribute "myID":

#myID {
    color: blue;
    font-size: 16px;
}

21. Explain the mechanism to access the XML data.
There are several ways to access XML data:
a. XPath: A query language that is used to navigate through the elements and attributes of an XML document.
b. XQuery: A query language that is used to retrieve data from XML documents.
c. DOM (Document Object Model): An API that allows you to programmatically access and manipulate XML data.
d. SAX (Simple API for XML): An event-based API that allows you to read through an XML document sequentially.

22. Why hierarchy is not good to organize relational data model? What is the solution?

Hierarchy is not a good way to organize relational data model because it can make it difficult to represent many-to-many relationships and can lead to data redundancy. The solution is to normalize the data model into multiple tables with relationships defined between them using primary keys and foreign keys. This allows for the data to be stored in an efficient manner and reduces data redundancy.

