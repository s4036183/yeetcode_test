#  YeetCode CI Pipeline

For this project, the pipeline uses a **Continuous Integration** model using **GitHub Actions**.  
The main purpose of the pipeline is to automate the process of a project's building, testing, and deployment.  
It can be triggered whenever events such as **pushes** or **pull requests** happen in any branch of the GitHub repository.


##  How the CI Pipeline Works

The pipeline runs automatically by GitHub Actions whenever the following occurs:

- Someone pushes code to any branch inside the repository (e.g. `main`, `feature/README.md`)
- A pull request is created

This happens automatically because GitHub watches the repository and triggers the `ci-pipeline.yml` file when any of the above actions occur.

##  What the Pipeline Does

The pipeline created by our team runs three steps (called **jobs**).  
These jobs are defined in the `ci.yml` file:

###  Lint Job

- Runs the command `npm run lint` to make sure the code follows ESLint rules.
- The push will fail if the code style or formatting is incorrect.
- This helps catch small mistakes early in development.

###  Unit Tests Job

- Runs the command `npm run test-unit` (using Jest).
- Ensures the app’s functions behave correctly.
- Helps catch bugs early during development.

###  Build Artefact Job (Main Branch Only)

- This step only runs when on the `main` branch.
- Builds a zip file of the whole app into a file called `yeetcode.zip`.
- Uploads the file as a downloadable artefact on GitHub Actions.

