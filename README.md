![9](https://user-images.githubusercontent.com/69017022/156702035-ca5be6c9-1607-40bd-8e66-34e509eb6cd8.png)


# Mod3 Group Consultancy Project

reference: [Turing documentation](https://backend.turing.edu/module3/projects/consultancy)

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#getting-started">Getting Started</a>
       <ul>
       <li><a href="#set-up">Set Up</a></li>
         <li>
           <a href="#use-of-this-repository">Use of this Repository</a>
           <ul>
             <li>Backend Server</li>
             <li>Frontend Server</li>
           </ul>
         </li>
         <li><a href="#use-of-the-bookclub-application">Use of BookClub Application</a></li>
         <li><a href="#google-oauth2">Google OAuth2</a></li>
       </ul>
    </li>
    <li>
      <a href="#project-description">About This Project</a>
      <ul>
        <li><a href="#learning-goals-for-project">Learning Goals for Project</a></li>
        <li><a href="#inception">Inception</a></li>
        <li><a href="#app-screenshots">Example Pages From App</a></li>
        <li><a href="#versions">Versions</a></li>
        <li><a href="#important-gems">Important Gems</a></li>
      </ul>
    </li>
    <li><a href="#apis">Book Club API</a></li>
    <li><a href="#project-contributors">Collaborators</a></li>
  </ol>
</details>

----------

## Getting Started

### Set Up
On your local system, open a terminal session to run the following commands:
1. Clone this repository `$ git clone git@github.com:Book-Club-Project/book_club_FE.git`
2. Navigate to the newly cloned directory `$ cd book_club_FE`
3. If bundler is not installed run `$ gem install bundler`
4. If or after bundler is installed run `$ bundle install` to install the required Gems
5. If errors occur, check for proper installation and versions of `bundler`, `ruby`, and `rails`
6. Set up the database locally with `$ rails db:{:drop,:create,:migrate,:seed}`
7. Open your text editor and check to see that `schema.rb` exists
8. You may also run the RSpec test suite locally with the command `$ bundle exec rspec` to ensure everything is functioning as expected.

### Use of this Repository
In order to run this application you need both this Frontend Repository and the associated [Backend Repository](https://github.com/Book-Club-Project/book_club_BE)

**Backend Server**
 
For a full explanation to set-up the backend server, please see the docs [Here](https://github.com/Book-Club-Project/book_club_BE#readme)

<!-- On you command line:
1. Navigate to the local directory where the backend repo is housed
2. Start the Backend server with `$ rails s` and navigate to http://localhost:3000/ in your web browser. Here you are able to interact with the API endpoints.

OR -->

1. Navigate to https://hidden-garden-43020.herokuapp.com/ to interact with the endpoints.

**Frontend Server**
 
<!-- On your command line:
1. Navigate to local directory where the frontend repo is housed
2. Run `$ rails s` to run the server locally
3. Open a web browser and navigate to http://localhost:5000/
4. Now you may explore the web application!

OR -->

1. Navigate to https://bookclub2022.herokuapp.com/ and take a look around!
### Use of the BookClub Application


### Google OAuth2
Book Club Consultancy Project uses Google OAuth2 to register and login a user. In order to login and register with Google OAuth2, you must set up Google OAuth2 and and set the client id for the web application.

  1. Open Google API Console Credentials page https://console.cloud.google.com/apis/credentials?project=services-oauth
  2. Use an existing Google project or create a new project
  3. Select + Create Credentials, then OAuth client ID
  4. It's possible that you may be prompted to set a product name on the Consent screen; if so, click Configure consent screen, supply the requested information, and click Save to return to the Credentials screen.
  5. Select Web Application as the Application type and enter any additional information.
  6. For the Authorized Redirect URIs, make sure to enter the following URLs for local development: http://localhost:3000, then click + ADD URI. This is the default URL when starting Book Club Consultancy Project in development mode.
  7. Click Create
  8. Navigate to the Book Club Front End directory using terminal `$ cd book_club_FE`
  9. While in terminal run `bundle exec figaro install` (this will create a file your need for you to store client id and client secret)
  9. Copy the client id and client secret, and in book_club_FE (config/application.yml) enter both as shown

```yml
    GOOGLE_CLIENT_ID: YOUR_CLIENT_ID
    GOOGLE_CLIENT_SECRET: YOUR_CLIENT_SECRET
 ```
----------

## Project Description

This is a back-end project designed to explore the fundamentals of exposing and consuming an API in order to develop an app that integrates microservices. Book Club builds community through literature. Users can connect through groups, messaging, and a bountiful resource of books. Functionality is achieved by combining our own database, the Google Books API, and external communication APIs to allow real-time communication, discussions, and recommendations.

----------

## Learning Goals for Project:

Explicit
- Expose an API
- Consume an API
- Use serializers to format JSON responses
- Implement CircleCI
- Implement OAuth2

Implicit
- Project planning
- Reading/Writing documentation
- Time Management/Prioritizing Work
- Break down large project goals into manageable steps
- Implement agile workflows
- GitHub workflow and project management tools

----------

### Inception

- Miro Board: [Group Brainstorm](https://miro.com/app/board/uXjVOL7SYZg=/)
  (including mission statement, initial feature dump, initial MVP design, determined stretch features)

- Wireframes: [Wireframes Board](https://miro.com/app/board/uXjVOLawnDs=/)

- Project Board: [User Stories](https://github.com/devin-p-lay/book_club_FE/projects/1)

- User Flow: [Mind Map](https://miro.com/app/board/uXjVOLajDBA=/)

- Group DTR: [DTR responses](https://docs.google.com/document/d/1dr8PcOvEctROQARJs0yk_TheJf21qY06tW8OX3wtlSw/edit)


----------
### App Screenshots
<details open="closed">

![Screen Shot 2022-03-03 at 10 33 43 PM](https://user-images.githubusercontent.com/89213429/156705612-1c63fac3-8d92-4254-95d9-a3e2601b0348.png)
![Screen Shot 2022-03-04 at 9 15 21 AM](https://user-images.githubusercontent.com/69017022/156799433-547857cb-37be-4fd8-a317-9d803199daaf.png)

![Screen Shot 2022-03-03 at 11 00 07 PM](https://user-images.githubusercontent.com/89213429/156708377-17c7520c-20f9-4ceb-b2fb-632d10af5f22.png)
![Screen Shot 2022-03-03 at 11 01 11 PM](https://user-images.githubusercontent.com/89213429/156708497-304f7b62-6fd6-466f-8aea-cbff0b97330a.png)
![Screen Shot 2022-03-03 at 11 01 36 PM](https://user-images.githubusercontent.com/89213429/156708538-7a652ecc-1bef-4e68-9c2a-d498eefba84f.png)
![Screen Shot 2022-03-03 at 11 03 32 PM](https://user-images.githubusercontent.com/89213429/156708715-d3d9a5fc-2b88-4ddd-9f88-8981c631d248.png)
![Screen Shot 2022-03-03 at 10 59 18 PM](https://user-images.githubusercontent.com/89213429/156708297-258966c2-c0f5-4a0c-b665-d3978f2ebb88.png)
![Screen Shot 2022-03-03 at 10 55 02 PM](https://user-images.githubusercontent.com/89213429/156707822-521f5570-2429-4479-8466-0935a98233cc.png)

</details>

### Versions

- Ruby 2.7.2
- Rails 5.2.6

----------

### Important Gems

- Testing: [rspec-rails](https://github.com/rspec/rspec-rails), [simplecov](https://github.com/simplecov-ruby/simplecov), [capybara](https://github.com/teamcapybara/capybara), [webmock](https://github.com/bblimke/webmock), [vcr](https://github.com/vcr/vcr)

- API: [jsonapi-serializer](https://github.com/fotinakis/jsonapi-serializers), [figaro](https://medium.com/@MinimalGhost/the-figaro-gem-an-easier-way-to-securely-configure-rails-applications-c6f963b7e993), [faraday](https://github.com/lostisland/faraday)

- User Authentication and Security: [omniauth-google-oauth2](https://github.com/zquestz/omniauth-google-oauth2)

----------

## APIs

See [book club BE repo](https://github.com/Book-Club-Project/book_club_BE)

----------

## Project Contributors
([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <!-- Arnaldo -->
    <td align="center"><a href="https://github.com/arnaldoaparicio"><img src="https://avatars.githubusercontent.com/u/88012780?v=4" width="100px;" alt=""/><br /><sub><b>Arnaldo (he/him)</b></sub></a><br /><a href="https://github.com/Book-Club-Project/book_club_FE/commits?author=arnaldoaparicio" title="Code">💻</a> <a href="#ideas-arnaldoaparicio" title="Ideas, Planning, & Feedback">🤔</a> <a href="https://github.com/Book-Club-Project/book_club_FE/commits?author=arnaldoaparicio" title="Tests">⚠️</a> <a href="https://github.com/Book-Club-Project/book_club_FE/pulls?q=is%3Apr+reviewed-by%3Ajarnaldoaparicio" title="Reviewed Pull Requests">👀</a></td>
    <!-- Eric -->
    <td align="center"><a href="https://github.com/echon006"><img src="https://avatars.githubusercontent.com/u/89038271?v=4" width="100px;" alt=""/><br /><sub><b>Eric (he/him)</b></sub></a><br /><a href="https://github.com/Book-Club-Project/book_club_FE/commits?author=echon006" title="Code">💻</a> <a href="#ideas-echon006" title="Ideas, Planning, & Feedback">🤔</a> <a href="https://github.com/Book-Club-Project/book_club_FE/commits?author=echon006" title="Tests">⚠️</a> <a href="https://github.com/Book-Club-Project/book_club_FE/pulls?q=is%3Apr+reviewed-by%3Ajechon006" title="Reviewed Pull Requests">👀</a></td>
    <!-- Mallory -->
    <td align="center"><a href="https://github.com/Malllll12"><img src="https://user-images.githubusercontent.com/87088092/155652176-cb2263b4-550c-4a80-b38c-519308bd166f.png" width="100px;" alt=""/><br /><sub><b>Mallory (she/her)</b></sub></a><br /><a href="https://github.com/Book-Club-Project/book_club_FE/commits?author=Malllll12" title="Code">💻</a> <a href="#ideas-Malllll12" title="Ideas, Planning, & Feedback">🤔</a> <a href="https://github.com/Book-Club-Project/book_club_FE/commits?author=Malllll12" title="Tests">⚠️</a> <a href="https://github.com/Book-Club-Project/book_club_FE/pulls?q=is%3Apr+reviewed-by%3AMalllll12" title="Reviewed Pull Requests">👀</a></td>
    <!-- Sierra -->
     <td align="center"><a href="https://github.com/Sierra-T-9598"><img src="https://user-images.githubusercontent.com/87088092/155652453-38a801c4-1243-46ce-a42f-b8416cff0423.png" width="100px;" alt=""/><br /><sub><b>Sierra (she/her)</b></sub></a><br /><a href="https://github.com/Book-Club-Project/book_club_FE/commits?author=Sierra-T-9598" title="Code">💻</a> <a href="#ideas-Sierra-T-9598" title="Ideas, Planning, & Feedback">🤔</a> <a href="https://github.com/Book-Club-Project/book_club_FE/commits?author=Sierra-T-9598" title="Tests">⚠️</a> <a href="https://github.com/Book-Club-Project/book_club_FE/pulls?q=is%3Apr+reviewed-by%3ASierra-T-9598" title="Reviewed Pull Requests">👀</a></td>
    <!-- Brad -->
     <td align="center"><a href="https://github.com/jbreit88"><img src="https://avatars.githubusercontent.com/u/88853324?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Brad (he/him)</b></sub></a><br /><a href="https://github.com/Book-Club-Project/book_club_FE/commits?author=jbreit88" title="Code">💻</a> <a href="#ideas-jbreit88" title="Ideas, Planning, & Feedback">🤔</a> <a href="https://github.com/Book-Club-Project/book_club_FE/commits?author=jbreit88" title="Tests">⚠️</a> <a href="https://github.com/Book-Club-Project/book_club_FE/pulls?q=is%3Apr+reviewed-by%3Ajbreit88" title="Reviewed Pull Requests">👀</a></td>
    <!-- Devin -->
    <td align="center"><a href="https://github.com/devin-p-lay"><img src="https://avatars.githubusercontent.com/u/87088092?v=4" width="100px;" alt=""/><br /><sub><b>Devin (he/him)</b></sub></a><br /><a href="https://github.com/Book-Club-Project/book_club_FE/commits?author=devin-p-lay" title="Code">💻</a> <a href="#ideas-devin-p-lay" title="Ideas, Planning, & Feedback">🤔</a> <a href="https://github.com/Book-Club-Project/book_club_FE/commits?author=devin-p-lay" title="Tests">⚠️</a> <a href="https://github.com/Book-Club-Project/book_club_FE/pulls?q=is%3Apr+reviewed-by%3Ajdevin-p-lay" title="Reviewed Pull Requests">👀</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification.
<!--
