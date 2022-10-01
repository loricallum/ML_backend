## Built With

- Ruby on Rails

## Live Demo

You can find the complete and functional app here:
[Live Demo Link](https://z6q65i.csb.app/)

## Setup

- To get a local copy up and running follow these simple example steps.
  - Clone the repo and cd in it.
  - Run `bundle install` to get all gems installed on your directory
  - Run `rails db:create` and then `rails db:migrate` to set the Database
  - Run `rails s` to open the server
  - You can go to the frontend repo [here](https://github.com/loricallum/ML_frontend) and follow instructions there. Or you can connect your own frontend (by requesting access first)

## Usage

### Login 

- Post: `https://appointments-api-majovanilla.herokuapp.com/auth/login`
- Parameters:
 ` { name: string,
    email; string
  }`

### SignUp 

- Post: `https://appointments-api-majovanilla.herokuapp.com/signup`
- Parameters:
 ` { name: string,
    email: string,
    password: string
  }`

### Tutors 

- Get: `https://appointments-api-majovanilla.herokuapp.com/tutors`
- Headers:
 `{ Authorization: 'Bearer ${token}'`

### Tutor

- Get: `https://appointments-api-majovanilla.herokuapp.com/tutors/${id}`
- Headers:
 `{ Authorization: 'Bearer ${token}'`

### Appointment 

- Post: `https://appointments-api-majovanilla.herokuapp.com/appointment/new`
- Parameters:
`{
  location: string,
  date: date,
  tutor_id: integer,
  }`
- Headers:
 `{ Authorization: 'Bearer ${token}'`

### Appointments

- Get: `https://appointments-api-majovanilla.herokuapp.com/appointments`
- Headers:
 `{ Authorization: 'Bearer ${token}'`


## Testing

- To check tests you need to comment line 7 and uncomment line 8 of app/lib/json_web_token.rb
  This should also be done if you want to test the app in dev env, otherwise, it won't work.
- Run `rspec` in your terminal (check that you are in the repo's folder) to run all the testing suite.

