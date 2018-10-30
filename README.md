# API Muncher: Recipe API Consumer

<!-- prep them "this is hard, they are not restful." it is not trivial -->

## At a Glance

- Individual, [stage 2](https://github.com/Ada-Developers-Academy/pedagogy/blob/master/rule-of-three.md#stage-2) project
- Due before class, **DATE HERE**

## Learning Goals:

- Configure an API for consumption
- Create authenticated API requests using HTTParty
- Consume JSON responses from an API
- Map response to application-specific data
- Separate API logic from application logic

## Objective

We will create a web application that displays recipes based on a search term. We will utilize an API from Edamam called the [Recipe Search API](https://developer.edamam.com/edamam-recipe-api).

## Getting Started

Before you start writing _any_ code:

- Explore the API documentation to become familiar with the request(s) you can make
- Create a Trello Board listing the features you will need to add and use it to track the progress of your app.

Once you've explored the API docs, this project:

- requires you to create a Rails application
  - conform to Rails conventions on naming and inflection
  - by using `rails new .` you will create a new rails app _inside_ of the fork folder instead of creating a _new_ folder for your rails app
  - [Set `local: true` as default for `form_with` in Rails 5](https://stackoverflow.com/questions/47822826/set-local-true-as-default-for-form-with-in-rails-5/51666415#51666415)
- Use better_errors for debugging purposes
- Deploy your completed app to Heroku


## Requirements

### Search

- As a user, when I can type a search term into a text input and submit it, then the web app:
  - Makes a request to the Edamam Recipe API using the search term
  - Displays the results in a list

### List View

- As a user, when I look at the list of recipes that were the result of a search, then the web app:
  - shows a **paged** list of recipes for a given search term, _ten at a time_
  - shows the name of the recipe and the corresponding photo
  - shows next to within each listed recipe a link to that recipe's detail page

### Show View

- As a user, when I look at a recipe's detail page, then the web app shows the following details about the individual recipe:
  - Name
  - Link to the original recipe (opens in a new tab)
  - Ingredients
  - Dietary information

### Miscellaneous Requirements

- Follow the requirements of attribution to Edamam, as required by their Terms and Conditions
  - [Official documentation from Edamam on attribution](https://developer.edamam.com/attribution)
- Create thorough tests for your any API Wrappers, classes, and controllers using VCR
- Use semantic HTML
- As a user, when I interact with the site and there is a problem, then I can see an error message detailing what the problem is and what I should do

## Important Notes

- How will you go from a list of recipes pulled down from an API, to being able to view a specific recipe in detail? Take time to consider your answer, write down the steps, and make a plan. Then, look at the API documentation to understand the detail of how you will execute it. Use Postman and your debugging skills to aggressively check what your requests look like in order to get specific recipe detail data. **Edamam's API is not RESTful**; this is not trivial. You'll have to use some clever code to get this to work! Be patient, and you'll get there.
- Using this API as a developer limits the number of API calls in a month to 5000. This means that we must try to minimize API calls for testing purposes as much as possible, to ensure you do not exceed this number of API calls in the one week of development we have.

## Optional Enhancements

- Keep track of most recent search terms and allow users to return to those searches
- Implement an OAuth strategy using Google
  - Allow users to save recipes to a "favorites" section that they can return to
-  Provide checkboxes or other controls to limit the search to options such as:
	-  Peanut Free
	-  Soy Free
	-  High Protein
	-  Etc

### Optional Wireframes

You have creative control over the design and layout of this project. Below are optional wireframes you may use. It is not a requirement that you do.

### Homepage

  ![Splash Page Wireframe](assets/Muncher_splash_wireframe.png )

### Results Page

  ![Results Page Wireframe](assets/muncher_results_wireframe.png )

### Recipe Show Page

  ![Results Page Wireframe](assets/muncher_recipe_wireframe.png )


Can you make your layout responsive? When the screen width shrinks to a medium screen, have a row with only two recipes. On a small screen width, have only a single recipe per line.  

## What Instructors Are Looking For
Check out the [feedback template](feedback.md) which lists the items instructors will be looking for as they evaluate your project.
