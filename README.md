# Task for Python Fullstack Developer

Hi!

We are glad that you want to join us. This is a task based around our web stack. It will aid us in considering your application and is a way for you to shine among other candidates! Read the instructions carefully and send us back the link with your solution.

## Objective

We want to see how do you approach various problems and structure the code. This shouldn't be a full-blown application, keep it simple and clean.

## Tech stack

- Angular

## Specification

The main objective of this task is to build a simple CRUD app which consists of fundamental elements SPA. The app will be a portal with advertisements.

Data in the app consists of two models:

- `Category` with following fields:
  - `id`
  - `name` - human-readable and shown in the frontend
  - `ordering` - a numeric value to determine ordering of category list (as it is seen to
    the final user). For example, if category _Apples_ is meant to be after category _Potatoes_,
    values in this field could be 2 and 1, respectively.
- `Offer`, related many-to-one with `Category`, with following fields:
  - `id`
  - `title`
  - `description`
  - `price`
  - `created_at` - timestamp

Endpoints which are available on https://backend-recruitment-api.herokuapp.com/ :

- `GET /offers` - returns all offers from the database with their ID, title, price and category ID.  
  Accepts category ID as a query parameter, named `category`. In this case, returns offers filtered accordingly.
- `GET /category` - returns all categories ordered by `ordering` field
- `GET /offers/{id}` - returns a single offer, with all fields associated with it.
- `POST PUT DELETE /offers/{id}` - manipulate a single offer. For `POST` and `PUT`, all fields are obligatory.
- `POST PUT DELETE /category/{id}` - manipulate category. For `POST` and `PUT`, all fields are obligatory.

**In frontend, implement the following:**

- displaying a list of offers,
- display each offer in detail (after clicking on it in the list view),
- in offer list view, implement filtering offers based on category
- separate view with form to create offer
- option to remove offers

For the sake of simplicity, don't worry about the authentication process (so anyone can use all endpoints).

## Would be awesome if you (with hints):

- Create docker file for application
- Deploy app on heroku or similar platform
- Cover functionality with tests

## Rules

The application's code should be kept in a public repository so that we can read it, pull it and build it ourselves. Remember to include README file with basic notes on application requirements and setup - we should be able to get it easily up and running.

**Good luck!** If you have any questions feel free to ping us!

**In case of problems with API please contact tomasz.rzesikowski@insert.com.pl**
