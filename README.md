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

## 2. What state is being tracked in the application?

* The application is tracking the permanent state of the application and the API, which includes the user name, email and password, messages between users, gif entry including a giff title, URL, story behind the gif and the date of post, and users favorite gifs.

## 3. What state is persistent? Reverse engineer the data and their relationships and build an ERD.

## 4. What state is transient? Is there any state being tracked, but not permanently in the API?

## 5. What event listeners are used in this application? Which components have event listeners?

* The app has a number of event listeners. The login form, message form, post entry module, delete post module and favorite post module all have a click event. The recipient choice in the message form uses a change event for the dropdown menu. There is a change event in the footer for the users and the favorites checkbox.

## 6. What fetch calls are used in this application to modify state? What method (GET, POST, DELETE) is used on each?

There are a number of fetch calls in this app as well. The favorite post component uses a method of ‘POST’. There is a component that marks whether a message is read that uses the ‘GET’ method. The component that saves user messages as well as a component that saves a user’s posts both use the ‘POST’ method. There are fetch calls using the ‘GET’ method for user posts as well as for the users themselves. There is also an option to delete a post using the ‘DELETE’ method.

* Users fetches “users”  and uses the default method: “GET”
* Likes fetches “likes” and uses the default method: ”GET”
* Message fetches “messages” and uses the default method: “GET”
* Posts fetches “posts” and uses the default method: “GET”
* Messages read fetches “messages” and uses the method: “POST”
* Save messages fetches “messages” and uses the method: “POST”,
* Favorite posts fetches “likes” and uses the method: “POST”,
* Save posts fetches “posts” and uses the method: “POST”,
* Delete posts fetches “posts” and uses the method: “DELETE”

## 7 What bugs/incomplete features still need to be fixed or implemented?

- direct messages received show up as undefined and aren't saved to permanent state
- there's no feature to follow other users
- the ‘year since’ in the footer drop down menu doesn’t reflect on the DOM
- the link on the “Posted by {name}” is broken and returns the user to top of page
- default “Posts by user {drop down box}” does not appear but other users do when selected
- no confirmation that message was saved or sent to another user
- the star used to select favorites can be used clicked repeatedly on the same gif post, which generates multiple likes for a single post and there's not undo option to remove a favorite post from a users list.

