# giffy-gram

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


