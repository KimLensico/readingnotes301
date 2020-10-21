# Sending Form Data

The architecture between the server and the client: the client requests the data and the server responds by sending an HTTPS.

### client: defining how to send the data

#### ACTION
`<form>` element defines how the data will be sent 
  - All of its attributes are designed to let you configure the request to be sent when a user hits a submit button
  - The two most important attributes are action and method.

- `action` - (attribute) defines where the data gets sent 
  - value must be a valid relative or absolute URL 
  - if this attribute isn't provided, the data will be sent to the URL of the page containing the form — the current page

#### METHOD
`method` - (attribute) defines how data is sent 
  - HTTP protocol provides several ways to perform a request: 
    - HTML form data can be transmitted via a number of different methods 
    - the most common being the GET method and the POST method

 Each time you want to reach a resource on the Web, the browser sends a request to a URL 
 
 An HTTP request consists of two parts: 
  - a header that contains a set of global metadata about the browser's capabilities
  - a body that can contain information necessary for the server to process the specific request.

`GET` - (method) is the method used by the browser to ask the server to send back a given resource

#### POST
Post is the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request
  - If a form is sent using this method, the data is appended to the body of the HTTP request.

  ***HTTP requests are never displayed to the user - to see them, you need to use tools such as Firefox Network Monitor/Chrome Developer Tools.***

### server: retrieving the data
(Whichever) HTTP method you choose, the server receives a string that will be parsed in order to get the data as a list of key/value pairs
  - the way you access this list depends on the development platform you use and on any specific frameworks you may be using with it

### special case: sending files
Sending files with HTML forms - *special case* 
  - Files are binary data 
  - all other data is text data
    - because HTTP is a text protocol, there are special requirements for handling binary data

#### enctype 
`enctype` - (attribute) lets you specify the value of the Content-Type HTTP header included in the request generated when the form is submitted
  - this header is very important because it tells the server what kind of data is being sent
    - alternative way of saying it: "This is form data that has been encoded into URL parameters."

#### to send files, take three extra steps:

1. set the method attribute to `POST` 
  - file content can't be put inside URL parameters
2. set the **value** of enctype to multipart/form-data 
  - the data will be split into multiple parts 
  - one for each file plus one for the text data included in the form body (if text is also entered into the form)
3. include 1+ <input type="file"> controls to allow your users to select the file(s) that will be uploaded.

***Servers can be configured with a size limit for files and HTTP requests in order to prevent abuse.***

### security issues
> each time you send data to a server, you need to consider security 

**HTML forms are by far the most common server attack vectors. The problems never come from the HTML forms themselves — they come from how the server handles data.**

**Be paranoid:** Never trust your users
The most important rule is: 

## never ever trust your users, including yourself; even a trusted user could have been hijacked.

*All data that comes to your server must be checked and sanitized. Always. No exception*

escape potentially dangerous characters 
  - the specific characters you should be cautious with vary depending on the context in which the data is used and the server platform you employ 
  - all server-side languages have functions for this 
  - Things to watch out for: 
    - character sequences that look like executable code (JavaScript or SQL commands)
  - limit the incoming amount of data to allow only what's necessary.
  - Sandbox uploaded files 
    - store them on a different server and allow access to the file only through a different subdomain or even better through a completely different domain.

#### tldr;
- sending form data is easy, but securing an application can be tricky
- a front-end developer is not the one who should define the security model of the data
- it's possible to perform client-side form validation
  -BUT the server can't trust this validation because it has no way to truly know what has really happened on the client-side