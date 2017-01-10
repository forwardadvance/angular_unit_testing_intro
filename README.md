# The Unit Testing for Angular course

In this course, you'll learn all about unit testing in Angular. Specifically, you'll learn about:

* Jasmine
* BDD vs TDD
* Unit testing controllers, services, factories and filters
* ngMocks
* Running tests with Karma
* Running tests with Webpack (If you've only ever used Karma, you'll like this one)
* Mocks, Spies and Stubs and when to use them
* Testing AJAX
* Testing Views, directives and components
* Testing Routes

I have a low tolerance of magic, so you'll find none here. Code is code, and we treat it as such. We'll introduce topics one by one, and practice with them until you're happy.

The whole point of unit testing is it should be incredibly simple. The minute it gets too complicated for an average intern to understand, it's no use anymore. It should be possible to read the test and understand what the code does.

This course is aimed at Angular one developers, but most of the ideas are applicable to other frameworks as well.

## BDD or TDD

You might have heard of the terms BDD and TDD. You might be wondering which you need. 

**TDD (Test Driven Development)** refers to the process where we write tests for each little piece of our system before we write the actual code. We test first. Writing code this way helps us to be better developers. We can go home happy at the end of the day, confident in a job well done.

**BDD (Behaviour Driven Development)** is a TDD methodology. We test the behaviour of our system, piece by piece. We are interested more in what the unit of functionality does, and not so much in how it does it.

In BDD, we try to write tests as much as possible in something that approximates natural English:

```
describe( 'my cat', () => {
    it( 'can miow', () => {
        expect(cat.miow()).toBe('Miow');
    });
});
```

## Jasmine is a BDD framework. 

It gives us natural English style matchers `expect(1+1).toEqual(2)`, or `expect( homepage.get() ).not.toThrowError();`.

Most people coming to this way of writing tests find it a little odd to begin with. It's code after all, not English. To these people I would say, go with it for a while, until you learn to love it.

## Why unit test?

Unit testing gives us more than just the knowledge that our code works. It gives us:

* The ability to refactor without fear.
* The ability to upgrade libraries quickly and easily.
* Documentation, for the next person.
* Better code (small functions and objects with clear input and output are easy to test).
* A harness in which to build complex components without refreshing the browser all the time.
* Respect in the developer community. An open source project without tests will gain no traction.
