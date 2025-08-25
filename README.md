For this project pipeline uses a continuous integration model using GitHub actions. The main purpose of a pipeline is to automate the process of a project's building, testing and deployment. It can be triggered whenever events such as push or pull requests are altered in any branch of the GitHub repository. Additionally, 
“Control program”.


How the CI Pipeline Works?
The pipeline runs automatically by GitHub actions whenever the following occurs:
- Someone pushes some code to any branch inside of the repo (main, feature/README.md)
- If a pull request is created 

This happens automatically by GitHub as it will watch the repo and trigger the CI-pipeline.yml file when any of the actions above happen.

What the Pipeline Does?
The pipeline created by our team runs three steps; they are called jobs. The three jobs we have on the ci.yml file are Lint Job, Unit Tests Job and the build artefact job
Lint Job
-The lint job runs the command of npm run lint to make sure the code being pushed to the repo is following the coding rules of ESLint. 
-The push request will fail if the coding style or formatting is wrong
-It will catch small mistakes early in the coding stage 

Unit Tests Job
-The Unit Tests Job will run the command of npm run test-unit which uses Jest.
-The Unit testing also makes sure the app’s function behave correctly 
-The Unit testing also helps catch bugs early in the development stage of the code

Build Artefact Job- This only applies to the main branch
-This step only will occur if you are on the main branch
-The artefact job will build a zip file of the whole app into a file called yeetcode.zip
-Then the artefact job will upload the file which can be downloaded from the GitHub Actions page
-This step simulates the app for deployment
