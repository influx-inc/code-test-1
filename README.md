# code-test-1
A test for candidates to Influx's engineering team.

## Introduction

The test should take about 8 hours.

When you have finished, send your Influx recruiter a URL to a github repo.  An Influx engineer will:
```
git clone <yoururl>
cd <yourapp>
bundle install
rake db:create
rake db:setup
rake db:migrate
rails s
```
You can expect us to get back to you within 2-3 days.  If for any reason that doesn't happen, feel free to follow up!

## Instructions

Please write a Ruby on Rails App as follows:

* the app is to have a User model and a Client model
* Client has_many Users.
* User and Client have a “name” attribute.
* names should not be longer than 180 characters
* Client has a “status” attribute with values: green, yellow and red

For the database, SQLite is fine, but feel free to demonstrate your knowledge of Postgres.

Populate the database with two users and three clients.

Use ActiveAdmin to implement :index, :show, :edit and :delete views for User and Client.

The client :index and :show views should show the number of associated users.

The Client :index view should show three scopes: *red*, *non-red*, *all*.

The User :index view should have two filters:
* filter by name
* filter by created_at where created_at is one of "2018-01", "2018-02", "2018-03" ... current month. The filter constrains users to ones created in the selected month.
