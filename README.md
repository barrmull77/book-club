# Book club
This app provides a book club-like service, where a user can create an account and add a book they're reading (incl. genre and total amount of pages), then make updates regarding the number of pages they have read. Upon completion of the book the user can then leave a review and share the review in social media. 
User's profile displays info about current reading progress, and a history of read books. 

This app was built using Vue, Pinia and tailwind CSS.
A dummy API is created with JSON server

### Setup
- Install dependencies
npm install 

- Run test server
json-server --watch db.json

- Run app
npm run dev

- Run tests
npm run test

### Improvements:
Design and layout overall could be greatly improved, I would like to add a better UI and some animations on the transitions to add some elegance.

I would also add more comprehensive testing to the app