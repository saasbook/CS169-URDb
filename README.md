# Hello, fellow developers!

Welcome to URDb, your go-to source for all things movies related. Whether it be movie ratings, actors, or reviews, you know you can find it all here! (Kind of.)

 As successful as we have been so far, we've run into alot of bugs - and because of that, we've hired you to come and write an extensive (ish) test suite to prevent problems in the future. Let's get you set up.

## Setup

To begin, clone/fork this repository.

Afterwards, run:

```
bundle install
```

to install rspec, our testing framework of choice.

To create our database, run:

```
rake db:create && rake db:migrate
```

Let's make sure our testing framework is working by running

```
rspec
```
You should see tests run....and fail. What happened?

What do the failed tests tell you? What expectation is not being met? What aspects of the app could be failing? Discuss your ideas with your partner!

When you're done, let's keep going.

## Part 1

Let's first take a look at what we have so far - it looks like we have a movies model, that has a name, and a rating - see `/app/models/movie.rb`.

The tests you ran earlier were in `spec/models`. We need to make sure the data is validated before we save our models - unfortunately URDb didn't have time to make the tests pass before giving the code to you.

Your job: Add the proper validations to the movie model to make the tests pass.

Hint: Take a look at the rails documentation to see how validations on data are implemented.

## Part 2

Now that you've been able to take a peek into our testing framework, it's time practice TDD and write your own tests. URDb wants to add a new feature that averages the ratings from a list of movies that we 'fetch' from Paramount Pictures. We've added a method where you can implement that in the movies model. (`average_paramount_rating`).

First, let's write some tests for the expected behavior for our method. If you take a look at the `self.from_paramount` method in the movies class, you'll see that we've simulated a ten second sleep, which would usually come from calling the Paramount Pictures API.

Your job:

1. Stub that method so that we don't have to wait ten seconds every time we call this method.

2. Add more test cases to test corner cases (as well as normal use cases) - what if the list is empty?

If you need help, consult the rspec documentation first before asking a GSI!

Note: Remember that you should be writing your tests before writing that actual implementations of these methods.

