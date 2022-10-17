#Microservices with Node JS and React

 A Mini-Microservices App

<br/>

 Project Setup

    $ npm install -g nodemon

    $ cd app

    $ npx create-react-app client

<br/>

    $ cd app

    $ mkdir posts
    $ cd posts
    $ npm init -y

    $ npm install --save express cors axios

<br/>

    $ cd app

    $ mkdir comments
    $ cd comments
    $ npm init -y

    $ npm install --save express cors axios


<br/>

    $ cd posts
    $ npm run start

<br/>

### 04. Testing the Posts Service

<br/>

    $ curl \
    --request POST http://localhost:4000/posts/ \
    --header "Content-Type: application/json" \
    | python -m json.tool

<br/>

    $ curl \
    --request GET http://localhost:4000/posts/ \
    --header "Content-Type: application/json" \
    | python -m json.tool

<br/>

 Implementing a Comments Service

<br/>

    $ echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p

<br/>

**to solve issue:**

```
[nodemon] Internal watch failed: ENOSPC: System limit for number of file watchers reached, watch ***
```

    $ cd comments
    $ npm run start

<br/>

 Quick Comments Test

<br/>

    $ curl \
    --data '{"content":"I am a comment"}' \
    --header "Content-Type: application/json" \
    --request POST http://localhost:4001/posts/123/comments \
    | python -m json.tool

<br/>

    $ curl \
    --request GET http://localhost:4001/posts/123/comments \
    --header "Content-Type: application/json" \
    | python -m json.tool

<br/>

 React Project Setup
<br/>

    $ cd client

    $ npm install --save axios
    $ npm start

<br/>

 Building Post Submission



Handling CORS Errors



 Fetching and Rendering Posts

<br/>

 Creating Comments

<br/>

 Displaying Comments
<br/>

 Request Minimization Strategies

<br/>

 An Async Solution

<br/>

 Common Questions Around Async Events

<br/>

 Event Bus Overview
<br/>

 A Basic Event Bus Implementation

    $ cd app
    $ mkdir event-bus
    $ cd event-bus

    $ npm init -y
    $ npm install --save express axios

<br/>

    $ npm run start

<br/>

 Emitting Events

<br/>

 Emitting Comment Creation Events

<br/>

 Receiving Events
<br/>

 Creating the Data Query Service

<br/>

    $ cd app
    $ mkdir query
    $ cd query

    $ npm init -y
    $ npm install --save express cors axios

<br/>

    $ npm run start
