# Testing

Testing forms a core part of our work and philosophy at CAST

All work (from product development through to tech) should be guided and backed up by tests (*test driven*)

### Why testing?

+ Projects without tests often become more and more fragile as they grow
+ Changing one thing can often break multiple other things
+ Adding tests makes these breakages obvious and easier to diagnose
+ Defining tests help clarify your intent (what do I want this code to *do*?)
+ A projects's tests are a form of documentation
+ Other developers coming onto the project can look at the tests and see exactly what the software is supposed to do

### TDD

TDD (test driven development) is a discipline where a test is written *first* and *then* code is written to make that test pass. The process is often described in three steps: red, green, refactor:

+ write the test and watch it fail
+ make it pass by adding code
+ refactor the code after each cycle (rinse and repeat)

![red-green-refactor](https://camo.githubusercontent.com/d32708d5ddec97f67800fb1982f57b52b95b2475/687474703a2f2f692e696d6775722e636f6d2f525165324e51542e6a7067)

+ [tdd leads to much more robust software](https://medium.com/@fagnerbrack/why-test-driven-development-4fb92d56487c#.6htslag7v)
+ we don't write unnecessary code that doesn't contribute to functionality
+ what you *want* the software to do is what drives the code, not the other way round

We should strive wherever possible to employ this discipline

### Unit Testing

Unit tests are an ideal way to gradually build complex functionality out of smaller pieces

+ Unit tests assert that small pieces of the software behave in certain ways
+ Unit tests encourage the writing of modular code which improves code quality and reusability.
+ We should strive for no commits without unit tests (where functionality is being added)


### End to End testing

End to end tests (also known as integration tests) should be used to help validate that complete functionality of a piece of software behaves as we want it to

+ E2e tests allow a more "user centred" perspective (the test is checking what the user should "see" at each point)
+ A great way of thinking about how to write e2e test is to consider how the user will "behave" at each point
+ In this sense the tests should be *"behaviour driven"* (behaviour driven development - BDD)
+ E2e tests can be used as "acceptance tests" for user stories (i.e. they validate that the user can complete a task with our software)

```rb
# an example of an e2e test in Ruby

scenario 'When I forget my password,
          I want to be able to reset it,
          so I can access my account' do
  helper.request_reset
  expect(ActionMailer::Base.deliveries.last.subject)
    .to eq 'Reset your password - Beehive'
  expect(current_path).to eq sign_in_path
  helper.set_new_password
  expect(current_path).to eq sign_in_path
end
```


### References

+ [dwyl learn tdd](https://github.com/dwyl/learn-tdd)
+ [5 common misconceptions about test driven development and unit tests](https://medium.com/javascript-scene/5-common-misconceptions-about-tdd-unit-tests-863d5beb3ce9#.8s3ciqmio)
+ [behaviour driven development](https://www.agilealliance.org/glossary/bdd/)
+ [when tdd doesn't work](https://8thlight.com/blog/uncle-bob/2014/04/30/When-tdd-does-not-work.html)
+ [acceptance test driven development](https://www.agilealliance.org/glossary/atdd/)
+ [dwyl learn nightwatch](https://github.com/dwyl/learn-nightwatch)
