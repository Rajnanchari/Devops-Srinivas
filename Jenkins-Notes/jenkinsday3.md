
### 1) What if Jenkins User Forgets the Password?

As a Jenkins Administrator, there is a provision to reset user credentials:

- **Steps to reset the user password**:
  1. Navigate to **Manage Jenkins → Security → Users**.
  2. Find the user whose password needs to be reset.
  3. Click on **Security** (on the left side).
  4. In the Password and Confirm Password fields, change the password and click **Save**.

- After changing the password, inform the user to follow these steps to update it:
  1. Log in to the Jenkins GUI.
  2. Click on the username (top right corner).
  3. Go to **Security**, and change the password there.
  4. Click **Submit**.

---

### 2) What if Jenkins Administrator Forgets the Password?

If a Jenkins administrator forgets the password, they can reset it using one of the following methods:

- **Method 1: Reset via CLI (If Available)**
- **Method 2: Delete the Admin Password from `config.xml`**
- **Method 3: Reset Admin Password via User XML File**
- **Method 4: Check Initial Admin Password (For Fresh Installations)**

---

### 3) Jenkins Folder Structure

In **Windows OS**, all Jenkins information and configuration details are stored under:
```
c:\ProgramData\Jenkins\.jenkins
```

- Key directories and their contents:
  - **Users Folder**: Contains all Jenkins user data.
  - **Workspace Folder**: Contains information related to configured jobs.
  - **Secrets Folder**: Stores configured secrets.
  - **Plugins Folder**: Contains all installed plugins (both manually and automatically).
  - **Nodes Folder**: Stores all configured nodes.
  - **Logs Folder**: Contains logs for slaves (if configured) and tasks.
  - **`config.xml` File**: Jenkins configuration file (ensure you back it up before editing).

  **Jenkins Logs**:
  - Navigate to **Manage Jenkins → Status Information → System Log** to view logs.
  - **Jenkins Version**: Check the bottom-right corner of the Jenkins GUI or navigate to **Manage Jenkins → Status Information → About Jenkins**.

---

### 4) Webhooks in Git

- **What is a Git Webhook?**
  A Git webhook is a method used for a repository to send real-time notifications to external services when certain events occur (such as push, pull request, or merge). Webhooks are commonly used for CI/CD automation, triggering deployments, notifications, and integrations with other tools.

- **Why Use Git Webhooks?**
  - Enforce coding standards (e.g., run linters before committing).
  - Automate tasks (e.g., generate documentation on commits).
  - Improve security (e.g., prevent committing secrets).
  - Streamline workflows (e.g., trigger CI/CD processes locally).

- **Types of Git Hooks**:
  1. **Client-Side Hooks** (Run on Developer's Machine):
     - `pre-commit`: Runs before a commit is created (e.g., check code style).
     - `commit-msg`: Runs after the commit message is written (e.g., enforce commit message format).
     - `pre-push`: Runs before pushing changes (e.g., run tests).
     - `post-commit`: Runs after a commit (e.g., send notifications).

  2. **Server-Side Hooks** (Run on Remote Repository):
     - `pre-receive`: Runs before accepting a push (e.g., check branch policies).
     - `update`: Runs when a branch is updated (e.g., enforce rules).
     - `post-receive`: Runs after a push is completed (e.g., trigger deployments).

---

### 5) Ways to Trigger Jenkins Jobs

You can set up automated actions that start your build based on specific events, like code changes or scheduled times.

#### a) **Trigger Builds Remotely** (e.g., from scripts)
- To use this option, first generate the authentication token for the job.
- Enable this option to trigger builds via a predefined URL, useful for scripts. This option requires an authorization token to ensure secure access.
  
**URL format**:  
```
JENKINS_URL/job/rasjsw/build?token=TOKEN_NAME  
or  
/job/rasjsw/buildWithParameters?token=TOKEN_NAME
```

#### b) **Build After Other Projects Are Built**
- Set up a trigger to start this project once other projects finish building.
- Useful for running extensive tests after a build.
  
**Projects to Watch Options**:
  - Trigger only if the build is stable.
  - Trigger even if the build is unstable.
  - Trigger even if the build fails.
  - Always trigger, even if the build is aborted.

#### c) **Build Periodically** (Using Cron Syntax)
- Set up builds to trigger on a schedule (similar to cron jobs).

**Cron Format**:  
```
MINUTE HOUR DOM MONTH DOW
```
Where:
  - **MINUTE**: Minutes within the hour (0–59).
  - **HOUR**: Hour of the day (0–23).
  - **DOM**: Day of the month (1–31).
  - **MONTH**: Month of the year (1–12).
  - **DOW**: Day of the week (0–7, where 0 and 7 represent Sunday).
  
For reference, use [crontab.guru](https://crontab.guru/).

#### d) **GitHub Hook Trigger for Git SCM Polling**
- This trigger is used when Jenkins receives a GitHub push hook.
- The GitHub Plugin checks if the hook matches the Git repository defined in the **SCM/Git** section of the job.

#### e) **Poll SCM**
- Configure Jenkins to poll for changes in the SCM.

#### f) **Manual Trigger**
- Jobs can also be triggered manually via the **Trigger** option in Jenkins.

