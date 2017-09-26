# assignment_designing_nosql_data_models
I'll have one data model hold the SQL please

By Tyler Ketron.


Basic

You're building an application that requires user login. Once logged in the user has a bunch of profile information and preference settings available to them. They will need to be able set their birthday, gender, phone number and location (city, state, country). They should be able to provide text to tell about themselves. They also should be able to enable and disable visibility of their birthday, gender, phone number and location.

## users
* username: String
* profile: Array
  * birthday: Datetime
  * birthday_visiblity: boolean
  * gender: String
  * gender_visibility: boolean
  * phone_number: String
  * phone_number_visibility: boolean
  * city: String
  * state: String
  * country: String
  * location_visibility: boolean



Intermediate

You're building a restaurant table reserving app that allows users to reserve tables for specified numbers of people. The app will need to show only tables that are available and the times they are available. The app will need to store reservations under a given name with a phone number and number of guests.

## tables
  * table_number: Integer
  * table_available: boolean
  * table_capacity: Integer

## reservations
  * reservation_id: Integer
  * table_number: Itteger
  * guest_name: String
  * phone_number: String
  * guests_number: Integer


You're building a backend for a university that requires students to be able to login. Once logged in, the students can view the exam grades for their classes. They should be able to view results by semester. Each semester should only show the classes in which that student is enrolled that semester.

## Students
  * username: String
  * password: String
  * grades: Array
    * semester: String
    * class_id: String
    * grade: String

## Classes
  * class_id: String
  * class_description: String

Advanced

Your eCommerce business needs to keep track of products and their prices. The products each belong to a department. The business needs to keep track of revenue as product prices change over time. The business also needs to keep track of receipts of transactions and the number of units each product has in stock.

## Products
  * product_id: Integer
  * product_name: String
  * product_price: Double
  * product_department: String

## Transactions
  * transcation_id: Integer
  * transaction_receipt: Array
    * product_id: Integer
    * product_quantity: Integer
  * transaction_amount: Double
  * transaction_time: Datetime

## Inventory
  * product_id: Integer
  * product_count: Integer


You're building an activity feed for a social media site. The feed must display a chronological list of activities for the current user's friends. These activities could potentially be any action performed on the site including uploading a photo, changing their profile, friending another user, commenting, liking etc... Further, you only want to display activities for users that the current user interacts with frequently.

## Users
  * username: String
  * password: String
  * email: String
  * last_logged_in: Datetime
  * friends: Array
    * friend_username: String
    * friend_interaction_count: Integer
    * friend_interaction_date: Datetime

## Activities
  * username: String
  * activities: Array
    * activity_id: Integer
    * activity_description: String
    * activity_time: Datetime
