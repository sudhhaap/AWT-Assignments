`TITLE 1: HTTP Methods & HTTP Status Codes`

`HTTP- Hyper Link Transfer Protocol` 
 It is the protocol used to fetch resources like html documents, css, images, etc. in web.

HOW ??
 1. user (client) sends a request
    when you type www.google.com in a broswer. The browser (client) creats sends http request to the respective server.
    eg.
        GET /index.html HTTP/1.1
        Host: www.example.com
2.  Server receives the request and process it
    it processesit(eg.look for index.html) and prepares the response.
3.  server responds with a http response
eg.
HTTP/1.1 200 OK
Content-Type: text/html
Content-Length: 1024

<html>...your webpage...</html>

4.  The browser renders the response and creats other requests for css, JavaScripts, images etc.



`HTTP MEthods`
 1.  GET    -   Retrieve data
 2.  POST   -   create data
 3.  PUT    -   update
 4.  PATCH  -   partial update
 5.  DELETE -   remove

status code
 1. 2XX - sucess
     201 - created
     204 No content

 2.3XX - Redirection
    301 MOves Permanently
    302 Found
    304 Not Modified

3. 4XX CLient Error
    400 Bad Request 
    403 Forbidden 
    405 Method Not Allowed

4. Server Error
    500 Internal Server Error
    502 Bad Gateway 
    503 Service Unavailable






`TITLE 2: CSS selectors`

1. Universal Selector (*)

It is used to select all elements on the page.

Example:
* {
  margin: 0;
  padding: 0;
}



2. Element (Type) Selector

It is used to select all elements of a specific type (tag).

Example:
p{
  font-size: 16px;
}



3. Class Selector (.classname)
 It is used to select all elements with a specific class attribute.

Example:
.highlight {
  background-color: yellow;
}




4. ID Selector (#idname)

IT is used to selects a single element with a specific ID.

Example:
#header {
  text-align: center;
}








`TITLE 3: Git basics`

Git is a version control system.
It is used to:
1. To track changes in code
2. Collaborate with others
3. To revert to previous versions when needed. 

It works locally on your computer but can also sync with remote 
repositories like GitHub for team collaboration and backup.


Basics of Git:

1. git init
Purpose:To Initialize a new Git repository.

code:
git init

Effect: Creates a .git folder in your project directory to start  tracking version history.



2.  git add
Purpose: Stages changes (files) to be committed.

git add filename     # Add specific file
git add .            # Add all changes in the directory



3. git commit
Purpose: Saves (commits) the staged changes to the local repository with a message.

git commit -m "Your commit message"



4. git push
Purpose: Uploads your local commits to a remote repository (e.g., GitHub).

git push origin main



5. git pull
Purpose: Fetches and merges changes from the remote repository into your local repo.

git pull origin main



6.  git clone
Purpose: Creates a copy of an existing remote repository on your local machine.

git clone https://github.com/username/repo.git



7. git branch
Purpose: Lists, creates, or deletes branches.

git branch           # List branches
git branch new-branch   # Create a new branch
git checkout new-branch # Switch to that branch










`TITLE 4: Callback & Higher-Order Function`

1. Callback Function
A callback is a function passed as an argument to another function.

Example:

function greet(name) {
  console.log("Hello, " + name);
}

function processUser(callback) {
  const name = "DataBae";
  callback(name);  // callback is called here
}

processUser(greet);







2. Higher-Order Function
A higher-order function is a function that takes another function as an argument, returns a function, or both.

Example:

function higherOrder(fn) {
  return function(name) {
    fn(name);
  };
}

const greet = name => console.log("Hi, " + name);
const customGreet = higherOrder(greet);
customGreet("Chatu");











`TITLE 5: Arrays`

1. filter()
Purpose: Returns a new array with elements that pass a test (returns true).

Example:
const nums = [1, 2, 3, 4];
const even = nums.filter(n => n % 2 === 0);
console.log(even); // [2, 4]



2. map()
Purpose: Creates a new array by transforming each element.

Example:

const nums = [1, 2, 3];
const doubled = nums.map(n => n * 2);
console.log(doubled); // [2, 4, 6]



3. forEach()
Purpose: Executes a function for each element, but does not return a new array.

Example:

const fruits = ["apple", "banana"];
fruits.forEach(fruit => console.log(fruit));




4. push()
Purpose: Adds element(s) to the end of the array.

Example:
```
const items = [1, 2];
items.push(3);
console.log(items); // [1, 2, 3]```





5. pop()
Purpose: Removes the last element from the array and returns it.

Example:

```const items = [1, 2, 3];
const last = items.pop();
console.log(last);  // 3
console.log(items); // [1, 2]```