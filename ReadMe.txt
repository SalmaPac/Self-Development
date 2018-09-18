Project Title
FriendManagement System

Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

Prerequisites
PostMan Tool have to be installed in order to execute the Rest Webservice. Junit cases can also be executed with preloaded request data with Rest template to invoke the Rest Webservices

Please use the context root as https://friendmanagement.cfapps.io
and append the following to test the rest webservices
1. As a user, I need an API to create a friend connection between two email addresses.
https://friendmanagement.cfapps.io/connectFriends

{
  "friends":
    [
      "andy@example.com",
      "john@example.com"
    ]
}

2. As a user, I need an API to retrieve the friends list for an email address.
https://friendmanagement.cfapps.io/fetchFriends/{emailAddress}
https://friendmanagement.cfapps.io/fetchFriends/andy@example.com

{
  email: 'andy@example.com'
}


3. As a user, I need an API to retrieve the common friends list between two email addresses.
https://friendmanagement.cfapps.io/fetchCommonFriends
{
  "friends":
    [
      "andy@example.com",
      "john@example.com"
    ]
}

4. As a user, I need an API to subscribe to updates from an email address.
https://friendmanagement.cfapps.io/subscribeFriends/Yes

{
  "requestor": "lisa@example.com",
  "target": "john@example.com"
}

5. As a user, I need an API to block updates from an email address.
https://friendmanagement.cfapps.io/subscribeFriends/Blocked

{
  "requestor": "andy@example.com",
  "target": "john@example.com"
}

6. As a user, I need an API to retrieve all email addresses that can receive updates from an email address.
https://friendmanagement.cfapps.io/sendUpdates

{
  "sender":  "john@example.com",
  "text": "Hello World! kate@example.com"
}

Built With
SpringBoot - The web framework is built but not used
Maven - Dependency Management
Rest Webservices - Used for micro services

Authors
Salma
