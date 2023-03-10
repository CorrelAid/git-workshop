How to quickly set up a gitlab with Azure if the internal server is down

- Request an appropriate Subscription or Resource Group from the Azure d-fine admins
- Create a (linux) VM in Azure and add a dns name to it using the properties panel
- Install gitlab with the correct external_url setting: <https://about.gitlab.com/install>
- Distribute the migration guide (template at the end) and add users using the Admin Area -> Overview -> Users
- Possibly disable Auto DevOps by unchecking the Admin Area -> Settings -> CI/CD -> Continuous Integration and Deployment -> Default to Auto DevOps pipeline for all projects
- Add a gitlab runner in an additional or in the same VM: <https://docs.gitlab.com/runner/install/linux-repository.html>
- Install docker: <https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository>
- Register a gitlab runner with the docker executor: <https://docs.gitlab.com/runner/register/#linux>
- Edit the gitlab config.toml (normally in /etc/gitlab-runner) so that concurrent is larger than 1 (e.g. 8) and privileged is set to true
- If you have permission problems with connecting to the docker daemon, you may need to add gitlab user to the sudo group

Migration Guide ($TEMPLATE, replace the $VARS)

- Create a new account at $URL
- Add your ssh key
- Create a new blank project
- Give your project a name
- Set the visibility to private
- If not selected, select your username as the namespace under the Project URL
- UNTICK Initialize repository with a README
- Follow the instructions under Push an existing Git repository except don't use the https link, but the ssh link under the clone option
