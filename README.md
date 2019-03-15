# Config gitlab-runner
Repo to install and configure a [gitlab-runner](https://docs.gitlab.com/runner/) using [ansible](https://www.ansible.com/)

## Step to install register a GitLab Runner
1. Install [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) in your computer.
2. Clone [this repo](https://github.com/NLESC-JCER/gitlab_runner).
3. Edit the [inventory](https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html) file with the address of the server(s) where you want to install the runner.
4. Make sure that you can ssh your server(s).
5. Install the runner with the following command:
   ``ansible-playbook -i inventory playbook.yml``
