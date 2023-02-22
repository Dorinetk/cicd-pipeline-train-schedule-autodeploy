# cicd-pipeline-train-schedule-autodeploy

This is a simple train schedule app written using nodejs. It is intended to be used as a sample application for a series of hands-on learning activities.

## Running the app

You need a Java JDK 7 or later to run the build. You can run the build like this:

    ./gradlew build

You can run the app with:

    ./gradlew npm_start

Once it is running, you can access it in a browser at http://localhost:8080

## Use Case
Your team is building the train-schedule app. They have put a lot of work into laying out a robust CI/CD Pipeline for the app. This Pipeline requires a final, manual, approval step before production deployment. However, the team is confident in the automation that they have built, and they want to eliminate this step.

You have been asked to remove the manual approval step and implement a basic smoke test in its place. The pipeline already includes a canary deployment to a Kubernetes cluster, so this smoke test should simply query the canary service to verify that it responds correctly. If the code passes the smoke test, the pipeline should proceed with production deployment.

## Notes
Deploy to production first. Then update your Jenkinsfile with version in example solution branch.
Then merge new code branch into master to test the smoke test. 
