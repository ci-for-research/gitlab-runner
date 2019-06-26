## Configure a customized continuos integration service using GitlabCI

This repository contains a recipe to use the [Gitlab CI/CD infrastucture](https://docs.gitlab.com/ee/ci/README.html) with a Github repository.The recipe installs and configures a [gitlab-runner](https://docs.gitlab.com/runner/) using [ansible](https://www.ansible.com/).

## Step to install register a GitLab Runner
Before going trhrough the following steps, make sure that you have a [gitlab account](https://about.gitlab.com/) then follow the instructions described at using the [Gitlab CI/CD with Github](https://docs.gitlab.com/ee/ci/ci_cd_for_external_repos/github_integration.html).

1. Install [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) in your computer.
2. Clone [this repo](https://github.com/NLESC-JCER/gitlab_runner).
3. Edit the [inventory](https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html) file with the address of the server(s) where you want to install the runner.
4. Edit the [playbook](https://docs.ansible.com/ansible/latest/user_guide/playbooks.html) file with the `remote_user` name for the hosts.
5. Make sure that you can ssh your server(s).
6. Install the runner with the following command:
   ``ansible-playbook -i inventory playbook.yml``

## Note:
*The script will ask you for a token for your new runner, you can find such token in the configuration of the CI/CD at the mirror repository that Gitlab automatically create for you. See the [configuration instructions](https://docs.gitlab.com/ee/ci/runners/#registering-a-specific-runner-with-a-project-registration-token).*

### Tags
*GitlabCI* makes use of [tags](https://docs.gitlab.com/ee/ci/yaml/#tags) to select specific runner from the available pool. You can create your own tag to name your `gitlab-runner` and use it as default.
