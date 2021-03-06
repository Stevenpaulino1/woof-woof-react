# WOOF WOOF WELCOME TO DOGGO BARK BARK

THIS GOOD APPLICATION FOR LOOKING AT DOGS BOW WOW

WHEN LOOKING AT PUP PUPS USER SHOULD BE ABLE TO:
 - CLICK ON DOGS IN THE DOG BAR TO SEE MORE INFO ABOUT THE GOOD PUPPER
   - MORE INFO INCLUDES A DOG PIC, A DOG NAME, AND A DOG BUTTON THAT INDICATES WHETHER IT IS A GOOD DOG OR A BAD DOG
   - YELLOW OR RED HALO AROUND DOG IN DOG INFO TO SHOW GOODNESS
 - CLICK ON GOOD DOG/BAD DOG BUTTON IN ORDER TO TOGGLE PUP GOODNESS

![Showcasing the layout](woof-woof-demo.gif)

### STEP 1: VIEW THE DATA
All of the dog data is stored in the db.json file. You'll want to access this data
using a json server. In order to do this, run the following commands:
  npm install -g json-server
  json-server --watch db.json

This will setup the data on a server using restful routes at http://localhost:3001/pups.
Go ahead and head to that url in your browser to view the data.
Familiarize yourself with the attributes for each pup. Try going to /pups/:id to see an individual pup as well.

### STEP 2: ADD PUPS TO DOG LIST
On the page, there is a div with the id of "dog-bar". On page load, list each dog's name within a `DogItem` component (ex: <span>Mr. Bonkers</span>).

### STEP 3: SHOW MORE INFO ABOUT EACH PUP
When a user clicks on a pup's span in the dog bar, that pup's info (image, name, and isGoodDog status) should show up in the div with the id of "dog-info".
When you have the pup's information, the dog info div should have the following children:
 - an img tag with the pup's image url
 - an H2 with the pup's name
 - a button that says "Good Dog!" or "Bad Dog!" based on whether isGoodDog is true or false.

  Additionally, if `isGoodDog` is true, they will have a yellow halo. If `isGoodDog` is false, it will be red.


  
 Ex:
 ```
  <img src=dog_image_url>
  <h2>Mr. Bonkers</h2>
  <button>Good Dog!</button>
 ```

 ### STEP 4: TOGGLE GOOD DOG
 When a user clicks the Good Dog/Bad Dog button, two things should happen:
  - The button's text should change from Good to Bad or Bad to Good
  - The corresponding pup object in the database should be updated to reflect the new isGoodDog value
    - Please note, you can update a dog by making a `PATCH` request to `/pups/:id`
