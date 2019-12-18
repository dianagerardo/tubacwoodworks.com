# Tubac Woodworks

Tubac Woodworks Inc, building custom cabinetry, entertainment center, bookcases, desks, and a variety of other wood products for home, office, or business.
 
*Collaborators:* 
 
*Diana, Chris, Matthew*
 
## About 
 
Full stack application.
This is the ( 1 of 2 ) README.md files. This file is to show the restrictions placed on the project and the expectations. The second README.md file is application information. 

## Index 
 
[Project *requirements ](#Project-*requirements) 
 
[Deliverables](#Deliverables) 

[MERN](#Mongo_db)
 
## Project *requirements 
 
  1. Something that can be used. (solves a problem)
 
  2. Research required. How your research affects your project.
 
  3. Track and put in the hours.
 
  4. Report issues in the issues tab of github
 
  5. project management system [Agile] Sprint and Scrum. Gant Chart in git.
 
  6. What documents were used. Frameworks, libraries, and stack.
 
  7. React.js, Node.js & Express, Mongo_db, CRUD/REST, Heroku, two external libraries ["GSAP", "SASS", "GTM / GA"], authentication for users (employees), Front-End UI, MVC, coding standards (scoping, naming, indentation.), API keys.
 
## Deliverables
 
Plan, Design, and Research

- Overview of 'why' the project is important.
- Design / sitemap and UI/UX needs. (mobile layout)
- Roles for Agile methodology
- Milestones via timeline.
- Github issue and project board.

---
 
 ## Coming soon...

 ## User Authentication
The owner of the site will be able to login with a set of credentials. Once logged in, that user will have access to additional UI elements that will allow them to replace portfolio pictures via the UI. People who visit the site that aren't logged in won't have this same access. User authentication will use a local strategy which involves storing credentials in a local MySQL database. The password field will be hashed and salted so that the value won't be stored in plain text.

### NPM packages used for authentication
* passport
* passport-local
* bcryptjs (for hashing and salting password)
* express-session (keeping track of user's authenticated session while browsing)
* mysql2 and sequelize (to interact with the MySQL database storing user credentials)

### Routes and Middleware
There is a middleware function applied to routes to validate if the user is logged in or not. If the user is not logged in, they will not be presented with the additional options to update photos.

### Mongo_DB 
I added this to test.

## Mongo_db

Will be converted the schema notes into mongoose models next:

Employees
* _id - ObjectId auto-generated by db
* username - String - Not Null - Unique - must be between 6 and 12 bytes, no special characters
* password - String - Not Null - (will be hashed value) 
* firstName - String - Not Null - At least 1 byte
* lastName - String - Not Null  - At least 1 byte
* role - String - Not Null - Choice of {Admin, User}
* createdAt - Date/Timestamp not null - from when entry is created
* updatedAt - Date/Timestamp not null - updated every time this document is updated 

```javascript
{
  username: {
    type: String,
    required: "String is Required",
    unique:true,
    minlength: [6, 'Username must be at least 6 characters.'],
    maxlength: [12, 'Username must be less than 12 characters.'],
    validate: [
      function(input) {
      // return RegEx code for special characters
      },
      "Your username must not contain special characters."
    ]
  },
  password: {
    type: String,
    required: "String is Required",
    match: [/.+@.+\..+/, "Please enter a valid e-mail address"]
  },
  firstName: {
    type: String,
    required: "String is Required",
    minlength: [1, 'First name must be at least 1 character.']
  },
  lastName: {
    type: String,
    required: "String is Required",
    minlength: [1, 'Last name must be at least 1 character.']
  },
  role: {
    type: String,
    required: "String is Required",
    // choice: [
    //   "admin",
    //   "user"
    // ]
  },
  createdAt: {
    type: Date,
    default: Date.now,
  },
  updateAt: {
    type: Date,
    date: new Date(Date.now())
  }
}

```

Customers

* _id - Object Id auto-generated by db
* Title - string
* firstName - String - Not Null - At least 1 byte
* middleName - String
* lastName - String - Not Null - At least 1 byte
* Nickname - String
* Email - String - unique - Not Null - email validation
* phoneNumber - String - not null - all numbers
* numberType - String - not null - Choice of {mobile,landline,work}
* promoContactByEmail - boolean not null default false
* promoContactBySms - boolean not null default false
* apptContactByEmail - boolean not null default true
* apptContactBySms - boolean not null default false
* streetAddress - string
* City - string
* State - string 
* Zipcode
* Zip4
* leadType - string 
* leadSource - string
* createdAt - Date/Timestamp not null - from when entry is created
* updatedAt - Date/Timestamp not null - updated every time this document is updated 
	

Appointment (1 customer can have many appointments)
* _id - object id auto-generated by db
* CustomerId - foreign key (_id from customers table) - not null
* apptDate - date of appointment.- not null
* apptTime - time of appointment - not null
* assignedEmployee - id of employee going to appointment
* updatedBy - id of employee who made appt
* createdAt - Date/Timestamp not null - from when entry is created
* updatedAt - Date/Timestamp not null - updated every time this document is updated 

Notes (1 customer can have many contact notes from multiple contact points)
* _id - object id auto-generated by db
* CustomerId - foreign key (_id from customers table) - not null
* noteDetail - String - not null - notes from contact point
* Date/timestamp of when contacted - not null
* updatedBy - id of employee who made notes - not null
* contactMethod - String - not null - choice of {email, sms, phone}
* createdAt - Date/Timestamp not null - from when entry is created
* updatedAt - Date/Timestamp not null - updated every time this document is updated 
	
```json
{
  "key" : "value"
}
```

## Express
```javascript

```
## React.js
```javascript

```

## Node.js
```javascript

```

### SCSS & Pre Pros
```css

```

### Site Map
<img src="" alt="site map for the page." />

---


 [Back to top](#)
