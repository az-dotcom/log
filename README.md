Automation is key for streamlining your work processes, and [GitHub Actions](https://docs.github.com/actions) is the best way to supercharge your workflow.
 
 - **Who is this for**: Developers, DevOps engineers, students, managers, teams, GitHub users.
 - **What you'll learn**: Create workflow files, trigger workflows, find workflow logs.
 - **What you'll learn**: How to create workflow files, trigger workflows, and find workflow logs.
 - **What you'll build**: An Actions workflow that will check emoji shortcode references in Markdown files.
 - **Prerequisites**: In this course you will work with issues and pull requests, as well as edit files. We recommend you take the [Introduction to GitHub](/skills/introduction-to-github) course first!
 - **How long**: This course is five steps long and can be finished in less than two hours to complete.
 - **Prerequisites**: In this course you will work with issues and pull requests, as well as edit files. We recommend you take the [Introduction to GitHub](/skills/introduction-to-github) course first.
 - **How long**: This course is five steps long and can be finished in less than two hours.
 
 ## How to start this course
 
 @@ -53,26 +53,32 @@ Automation is key for streamlining your work processes, and [GitHub Actions](htt
 
 _Welcome to "Hello GitHub Actions"! :wave:_
 
 **What is _GitHub Actions_**: Actions are a flexible way to automate nearly every aspect of your team's software workflow. You can automate testing, continuously deploy, review code, manage issues and pull requests, and much more. The best part, these workflows are stored as code in your repository and easily shared and reused across teams. To learn more, check out the [GitHub Actions feature page](https://github.com/features/actions), or the [GitHub Actions documentation](https://docs.github.com/actions).
 **What is _GitHub Actions_?**: GitHub Actions is a flexible way to automate nearly every aspect of your team's software workflow. You can automate testing, continuously deploy, review code, manage issues and pull requests, and much more. The best part, these workflows are stored as code in your repository and easily shared and reused across teams. To learn more, check out these resources:
 
 First, we'll define a **workflow** that uses the action.
 -  The GitHub Actions feature page, see  [GitHub Actions](https://github.com/features/actions).
 -  The "GitHub Actions" user documentation, see [GitHub Actions](https://docs.github.com/actions).
 
 **What is a _workflow_**: Workflows are defined in special files in the `.github/workflows` directory. Workflows can execute based on your chosen event. For this lab, we'll be using the [`push`](https://docs.github.com/en/developers/webhooks-and-events/webhooks/webhook-events-and-payloads#push) event.
 **What is a _workflow_?**: A workflow is a configurable automated process that will run one or more jobs. Workflows are defined in special files in the `.github/workflows` directory and they execute based on your chosen event. For this exercise, we'll use a `push` event. 
 
 We went ahead and made a branch and pull request for you.
 - To read more about workflows, jobs, and events, see "[Understanding GitHub Actions](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions)".
 - If you want to learn more about the `push` event before using it, see "[push](https://docs.github.com/en/developers/webhooks-and-events/webhooks/webhook-events-and-payloads#push)".
 
 To get you started, we used actions to go ahead and made a branch and pull request for you.
 
 ### :keyboard: Activity: Create a workflow file
 
 1. Open a new browser tab, and work on the steps in your second tab while you read the instructions in this tab.
 1. Open the pull request from the `emoji-workflow` branch.
 1. Add a file at `.github/workflows/emoji.yml` on the `emoji-workflow` branch.
 1. Open a new browser tab, and navigate to this same repository. Then, work on the steps in your second tab while you read the instructions in this tab.
 1. Navigate to the **Code** tab.
 2. From the **main** branch dropdown, click on the **emoji-workflow** branch.
 3. Navigate to the `.github/workflows/` folder, then select **Add file** and click on **Create new file**.
 4. In the **Name your file...** field, enter `emoji.yml`.
 1. Add the following content to the `emoji.yml` file:
    ```yaml
    name: Check emoji shortcode
    on: push
    ```
 1. Commit the changes.
 1. Wait about 20 seconds then refresh this page for the next step.
 2. To commit your changes, click **Commit new file**.
 3. Wait about 20 seconds for actions to run, then refresh this page (the one you're following instructions from) and an action will automatically close this step and open the next one.
 
 </details>
 
 @@ -86,22 +92,23 @@ We went ahead and made a branch and pull request for you.
 <details id=2>
 <summary><h2>Step 2: Add a job to your workflow file</h2></summary>
 
 _Nice work! :tada: You added a workflow!_
 _Nice work! :tada: You added a workflow file!_
 
 Here's what it means:
 
 - `name: A workflow for my Hello World file` gives your workflow a name. This name appears on any pull request or in the Actions tab.
 - `name: A workflow for my Hello World file` gives your workflow a name. This name appears on any pull request or in the Actions tab of your repository.
 - `on: push` indicates that your workflow will execute anytime code is pushed to your repository.
 
 Next, we need to specify jobs to run.
 
 **What is a _job_**: Workflows have jobs, and jobs have steps.
 **What is a _job_?**: A job is a set of steps in a workflow that execute on the same runner (a runner is a server than runs your workflows when triggered). Workflows have jobs, and jobs have steps. Steps are executed in order and are dependent on each other. We'll add steps in the next step of this exercise. To read more about jobs, see "[Jobs](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions#jobs)".
 
 In this step, we will add a "build" job. We will specify `ubuntu-latest` as the fastest and cheapest job runner available.
 In this step of our exercise, we will add a "build" job. We will specify `ubuntu-latest` as the fastest and cheapest job runner available. If you want to read more about why we'll use that runner, see the code explanation for the line `runs-on: ubuntu-latest` in the "[Understanding the workflow file](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions#understanding-the-workflow-file)" article.
 
 ### :keyboard: Activity: Add a job to your workflow file
 
 1. Update `emoji.yml` in the `emoji-workflow` branch to:
 1. Open your `emoji.yml` file. 
 2. Update the contents of the file to:
    ```yaml
    name: Check emoji shortcode
    on: push
 @@ -110,9 +117,9 @@ In this step, we will add a "build" job. We will specify `ubuntu-latest` as the
        name: Check emoji shortcode
        runs-on: ubuntu-latest
    ```
 1. Click **Start commit** in the top right of the workflow editor.
 1. Type your commit message and commit your changes directly to your branch.
 1. Wait about 20 seconds then refresh this page for the next step.
 3. Click **Start commit** in the top right of the workflow editor.
 4. Type your commit message and commit your changes directly to your branch.
 5. Wait about 20 seconds for actions to run, then refresh this page (the one you're following instructions from) and an action will automatically close this step and open the next one.
 
 </details>
 
 @@ -127,18 +134,19 @@ In this step, we will add a "build" job. We will specify `ubuntu-latest` as the
 
 _Nice work adding a job to your workflow! :dancer:_
 
 Workflows have jobs, and jobs have steps. So now we'll add steps.
 Workflows have jobs, and jobs have steps. So now we'll add steps to your workflow.
 
 **What are _steps_**: Action steps will run during our job in order. Each step must pass for the next step to run. Action steps can be used from within the same repository, from any other public repository, or from a published Docker container image.
 **What are _steps_?**: Actions steps will run during our job in order. Each step is either a shell script that will be executed, or an action that will be run. Each step must pass for the next step to run. Actions steps can be used from within the same repository, from any other public repository, or from a published Docker container image.
 
 In our action,
 1. We will `git checkout` the code, using a [pre-built checkout action](https://github.com/actions/checkout).
 2. We'll run a [bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) script to check Markdown files.
 3. We'll fail (`exit 1`) if any Markdown file contains an emoji without using [emoji shortcodes](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md).
 In our action, we will have steps for each of the following:
 1. Checkout the code with `git checkout`, using a [pre-built checkout action](https://github.com/actions/checkout).
 2. Run a [bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) script to check Markdown files.
 3. Fail with (`exit 1`) if any Markdown file contains an emoji without using [emoji shortcodes](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md).
 
 ### :keyboard: Activity: Add actions to your workflow file
 ### :keyboard: Activity: Add Actions steps to your workflow file
 
 1. Update `emoji.yml` in the `emoji-workflow` branch to:
 1. Open your `emoji.yml` file.
 2. Update the contents of the file to:
    ```yaml
    name: Check emoji shortcode
    on: push
 @@ -155,9 +163,9 @@ In our action,
                exit 1
              fi
    ```
 1. Click **Start commit** in the top right of the workflow editor.
 1. Type your commit message and commit your changes directly to your branch.
 1. Wait about 20 seconds then refresh this page for the next step.
 3. Click **Start commit** in the top right of the workflow editor.
 4. Type your commit message and commit your changes directly to your branch.
 5. Wait about 20 seconds for actions to run, then refresh this page (the one you're following instructions from) and an action will automatically close this step and open the next one.
 
 </details>
 
 @@ -170,15 +178,17 @@ In our action,
 <details id=4>
 <summary><h2>Step 4: Merge your workflow file</h2></summary>
 
 _You're now able to write and run Actions workflows! :heart:_
 _You're now able to write and run an Actions workflow! :sparkles:_
 
 Merge this pull request so the action will be a part of the `main` branch.
 Merge your pull request so the action will be a part of the `main` branch.
 
 ### :keyboard: Activity: Merge your workflow file
 
 1. Merge the pull request from branch `emoji-workflow`.
 1. Delete your `emoji-workflow` branch (optional).
 1. Wait about 20 seconds then refresh this page for the next step.
 1. In your repo, click on the **Pull requests** tab.
 2. Click on the **Create emoji shortcode workflow** pull request.
 3. Click **Merge pull request**, then click **Confirm merge**.
 4. Optionally, click **Delete branch** to delete your `emoji-workflow` branch.
 5. Wait about 20 seconds for actions to run, then refresh this page (the one you're following instructions from) and an action will automatically close this step and open the next one.
 
 </details>
 
 @@ -193,19 +203,19 @@ Merge this pull request so the action will be a part of the `main` branch.
 
 _You've now got a fully functioning workflow! :smile:_
 
 This action will run any time a new commit is created or pushed to the remote repository. Since you just created a commit, the workflow should have been triggered.
 Your new action will run any time a new commit is created or pushed to the remote repository. Since you just created a commit, the workflow should have been triggered.
 
 **Seeing your _action_ in action**: The status of your action is shown here in the pull request (look for **All checks have passed** below), or you can click the "Actions" tab in your repository. From there you will see the actions that have run, and you can click on the action's "Log" link to view details.
 **Seeing your _action_ in action**: The status of your action is shown in a pull request before you merge, look for **All checks have passed** when you try out the steps below. You can also view them from the **Actions** tab in your repository. From there, you will see all the actions that have run, and you can click on each action to view details and access log files.
 
 ![View an action's log](https://user-images.githubusercontent.com/16547949/62388049-4e64e600-b52a-11e9-8bf5-db0c5452360f.png)
 
 ### :keyboard: Activity: Trigger the workflow
 
 1. Make a new branch: `test-workflow`.
 1. Commit any change to your branch, such as adding an emoji to your README.md file.
 1. Open a pull request with branch: `test-workflow`.
 1. See your action run on your pull request.
 1. Wait about 20 seconds then refresh this page for the next step.
 1. Make a new branch named `test-workflow`.
 1. Commit any change to your branch, such as adding an emoji to your README.md file. If you want to see what happens if an action fails, add an emoji without using shortcode.
 2. View the pull request on your branch.
 3. See your action run on your pull request.
 4. Wait about 20 seconds for actions to run, then refresh this page (the one you're following instructions from) and an action will automatically close this step and open the next one.
 
 </details>
 
 @@ -223,18 +233,18 @@ _Congratulations friend, you've completed this course!_
 
 Here's a recap of all the tasks you've accomplished in your repository:
 
 - You've created your first GitHub Actions workflow.
 - You've created your first GitHub Actions workflow file.
 - You learned where to make your workflow file.
 - You created an event trigger, a job, and steps for your workflow.
 - You're ready to automate anything you can dream of.
 
 ### What's next?
 
 - Review the [GitHub Actions documentation](https://docs.github.com/actions/learn-github-actions) on GitHub Docs.
 - Learn more about GitHub Actions by reading "[Learn GitHub Actions](https://docs.github.com/actions/learn-github-actions)".
 - Use actions created by others in [awesome-actions](https://github.com/sdras/awesome-actions).
 - We'd love to hear what you thought of this course [in our discussion board](https://github.com/skills/.github/discussions).
 - [Take another GitHub Skills course](https://github.com/skills).
 - [Read the GitHub Getting Started docs](https://docs.github.com/get-started).
 - Learn more about GitHub by reading the "[Get started](https://docs.github.com/get-started)" docs.
 - To find projects to contribute to, check out [GitHub Explore](https://github.com/explore).
 
 </details>
