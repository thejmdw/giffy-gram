# giffy-gram

## 1. What components make up this application?

**Login.js** returns the HTML required to render the form.
* 1 click event on the login button

**Post.js** returns the HTML required to render a post. 

**PostEntry.js**  returns the HTML render of the form to fill out new gif posts. It has an event listener looking for a click event to submit a new post. It has an input for the title, URL of gif and the story behind your gif. There is a save button and a cancel button.

**PostList.js** looks like it is returning the HTML required to render a list of specific users, posts, likes and favorites.

**MessageForm.js** returns the HTML that causes the direct message pop up to appear and uses the save button to send messages to the database with a click event.

**MessageList.js** returns the HTML required to render a list of messages. It is importing the messages and users stored in our provider.js from application state.

**PrivateMessages.js** returns the HTML required to render a list of private messages.

**NavBar.js** provides the HTML required to render the Nav Bar
* It provides links to navigate the app.
* 4 click event listeners


**Footer.js** provides the HTML required to render the Footer.
* It provides methods of filtering the posts
* 3 change event listeners


**GiffyGram.js** creates a function that imports and formats the components/functions -- NavBar(), MessageForm(), PostEntry(), PostList(), Footer() -- to be exported to the main.js module, which will then render all the HTML.
