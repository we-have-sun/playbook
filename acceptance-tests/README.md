# Acceptance Tests

Acceptance tests are User Stories turned into code. Behaviour Driven Development (BDD) is particularly useful for Acceptance Tests since User Stories are at the heart of BDD methodology. It advocates that a developer first writes a User Story. This User Story is used both for documenting the feature and triggering the acceptance tests.

Developers only implement behaviors which contribute most directly to these business outcomes, to minimize waste. Behaviors are described in a single notation which is directly accessible to domain experts, testers and developers, to improve communication.

If the customer really would rather sacrifice the quality of their automated acceptance test suite to get it to market quickly, they are entitled to make that decision - but the consequences should be made quite clear.

When the test passes, the developer commits the code into version control with a message such as:

> Guest creates pledge

The code is then run on the Continuous Integration server to make sure the acceptance test still passes in an environment that matches the production environment.

When the acceptance test is green for the CI server and you and any other designers, developers, or clients are satisfied that the jobs story is complete on staging, the feature can be deployed to production at will. This can result in features being pushed to production very frequently, and therefore more value is being delivered to customers sooner.

Our Acceptance tests are done with [Cypress](https://www.cypress.io/), and we use [Faker.js](https://github.com/marak/Faker.js/) to generate testing data. There are other popular solutions for User Acceptance Testing, but we found Cypress as a perfect fit for our projects.