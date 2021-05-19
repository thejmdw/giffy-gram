# giffy-gram

## 1. What components make up this application?

* **Login.js** returns the HTML required to render the form.

* **Post.js** returns the HTML required to render a post. 

* **PostEntry.js**  returns the HTML render of the form to fill out new posts.

* **PostList.js** looks like it is returning the HTML required to render a list of specific users, posts, likes and favorites.

* **MessageForm.js** returns the HTML that causes the direct message pop up to appear and uses the save button to send messages to the database with a click event.

* **MessageList.js** returns the HTML required to render a list of messages. It is importing the messages and users stored in our provider.js from application state.

* **PrivateMessages.js** returns the HTML required to render a list of private messages.

* **NavBar.js** provides the HTML required to render the Nav Bar
  * It provides links to navigate the app.

* **Footer.js** provides the HTML required to render the Footer.
  * It provides methods of filtering the posts

* **GiffyGram.js** exports a function that formats the NavBar MessageForm, PostEntry, PostList, and Footer components.

## 2. What state is being tracked in the application?

* The User
  - name
  - email
  - password

* The Message
  - userId
  - text
  - recipientId
  - read

* The Post
  - userId
  - title
  - timestamp
  - description
  - imageURL

* The Likes
  - postId
  - userId


## 3. What state is persistent? Reverse engineer the data and their relationships and build an ERD.

* The User, Message, Post, and Likes are persistent.

* Check out our [ERD](https://dbdiagram.io/d/60a2bc2ab29a09603d154226).

## 4. What state is transient? Is there any state being tracked, but not permanently in the API?

* The "Posts Since Year" dropdown in the Footer
* The "Posts By User" dropdown in the Footer
* The "Show Only Favorites" checkbox in the Footer
* The PostEntry.js input fields
* The MessageForm.js input fields

## 5. What event listeners are used in this application? Which components have event listeners?

* 12 "Click" Events
  - Login.js - Login Button
  - NavBar.js - Home, New DM, DMs, LogOut
  - PostEntry.js - MiniMode, Submit, Cancel
  - MessageForm.js - Submit, Cancel
  - Post.js - Delete, Favorite

* 4 "Change" Events
  - Footer.js - Posts Since, Posts By User, Show Only Faves
  - MessageForm.js - Recipient

## 6. What fetch calls are used in this application to modify state? What method (GET, POST, DELETE) is used on each?

* Users fetches “users”  and uses the default method: “GET”
* Likes fetches “likes” and uses the default method: ”GET”
* Message fetches “messages” and uses the default method: “GET”
* Posts fetches “posts” and uses the default method: “GET”
* Messages read fetches “messages” and uses the method: “POST”
* Save messages fetches “messages” and uses the method: “POST”,
* Favorite posts fetches “likes” and uses the method: “POST”,
* Save posts fetches “posts” and uses the method: “POST”,
* Delete posts fetches “posts” and uses the method: “DELETE”

## 7. What bugs/incomplete features still need to be fixed or implemented?

- Direct message text shows up as undefined and isn't saved to permanent state.
- The follow other users feature has not been implemented.
- The 'Posts since’ drop down menu doesn’t reflect the posts visible in the Posts List.
- The link on the “Posted by {name}” is broken and returns the user to top of page.
- “Posts by user {Ray Medrano}” appears to be the default Post List until another User is selected.
- No confirmation that message was saved or sent to another user.
- The star used to select favorites cannot be toggled on or off. It only can bbe toggled on and clicking continues to add that post to the favorites list.

