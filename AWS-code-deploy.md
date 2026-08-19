AWS CodeDeploy

What is AWS CodeDeploy?

AWS CodeDeploy is a managed deployment service that automates application deployments to compute environments.

It can deploy applications to:

- Amazon EC2
- On-premises servers
- AWS Lambda
- Amazon ECS

Deployment Workflow

Application Artifact
       ↓
CodeDeploy
       ↓
Target Environment
       ↓
Application Deployed

Why Use CodeDeploy?

Manual deployments can cause:

- Human errors
- Configuration inconsistencies
- Slow releases
- Difficult rollbacks

CodeDeploy automates the deployment process.

appspec.yml

For EC2/on-premises deployments, CodeDeploy uses an application specification file called:

appspec.yml

It defines how the application should be deployed.

Example structure:

version: 0.0

os: linux

files:
  - source: /
    destination: /var/www/myapp

hooks:
  ApplicationStop:
    - location: scripts/stop.sh

  ApplicationStart:
    - location: scripts/start.sh

Deployment Lifecycle

Common deployment lifecycle events include:

ApplicationStop
↓
DownloadBundle
↓
BeforeInstall
↓
Install
↓
AfterInstall
↓
ApplicationStart
↓
ValidateService

Deployment Strategies

In-place Deployment

The existing instances are updated with the new application version.

Existing EC2
    ↓
Stop/Update
    ↓
New Version

Blue/Green Deployment

A new environment is created for the new version.

Blue
Current Production
      ↓
Green
New Version
      ↓
Traffic switched

Blue/green deployments reduce deployment risk and make rollback easier.

CodeDeploy with EC2

For EC2 deployments, the CodeDeploy agent is installed on the target instance.

The agent communicates with the CodeDeploy service and executes deployment instructions.

Important Interview Point

CodeDeploy = Deployment

It does not replace the source repository or build service.

CodeCommit → Source
CodeBuild → Build/Test
CodeDeploy → Deploy
