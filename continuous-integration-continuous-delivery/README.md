# Continuous Integration and Continuous Delivery

Martin Fowler has an [extensive description](https://martinfowler.com/articles/continuousIntegration.html) of Continuous Integration (CI). The basics are:

- We have a test suite that each developer runs on their machine.
- When they commit their code to a shared version control repository, the tests are rerun, "integrated" with code from other developers.

As the adage goes, “[if something is painful, do it more often](https://martinfowler.com/bliki/FrequencyReducesDifficulty.html).”

This helps ensure there's nothing specific to the developer's machine making the tests pass. The code in version control needs to run cleanly in production later, so before the code is allowed to be deployed to production, it is run on a CI server or service.

When a build fails, we get alerts in Slack and via email. Click the alert, and we see a backtrace that gives us a hint of how to "fix the build."

When we write the fix and commit to version control again, we'll get a "passing build" alert in Slack and via email. Click the alert, and we see the passing build.

Green is good.

A robust test suite is an absolute requirement for a web application. However, one major problem with test suites is that they get slow as they get large.

CI test runs are triggered when we push to Gitlab and can be seen as part of the status checks of merge requests.

Continuous Delivery (CD), takes CI one step further. After each feature is merged and validated, the application is not only tested for correctness, but it is also packaged and deployed into a staging environment (that ideally matches production). All this happens in a completely automated manner. Finally, based on the strategy agreed with the client, we deploy the changes and features the client wants to release to production by issuing a manual trigger.