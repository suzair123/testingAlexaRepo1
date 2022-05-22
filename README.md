# Bespoken Overview Alexa skill - End to end tests

![image](https://user-images.githubusercontent.com/6411740/129514336-d8db394e-fffa-4f93-9e8d-0c94e4512bac.png)

The Bespoken Overview skill for Amazon Alexa provides a quick look at the tools and services Bespoken offers to its customers. It uses the Alexa Presentation Language on devices with a screen and its available in both English and Spanish.

This project contains the end-to-end tests that make sure that the skill  works correctly and, at the same time, shows the different features that our CLI posseses, including: assertions on a prompt, multiple prompts handling, using homophones, using JSONPath to test against APL directives, and more.

Tests are currently configured to run every 3rd day of the week using Github Actions. Once run, results are available as output artifacts. Results are also pushed to Datadog for easier historical visualization.

### How to run this project locally
- Clone and download this repository
- Run npm install
- Create a new Alexa Virtual Device token in the [Bespoken Dashboard](https://apps.bespoken.io)
- Fill the the virtual device token value inside `example.env`, then rename to `.env`
- Remove line 2 on testing.json if you don't want the results being pushed to Datadog.
- Take a look at the tests files under the `test/e2e` folder
- Run these tests by doing `npm test`
