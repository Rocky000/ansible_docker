# Ansible Docker
Recently, I was trying to automate a process of pulling docker image and running the docker image with Ansible. Which has never been done before on our company. Previously it was done via bash command simply running from groovy script, which is prone to result in pipeline failure.

I thought to make it a self-reliant Ansible for docker. That I can use any other projects just by simply modifying some values (like- Repo name, ENV file, volumes etc.)

Using Ansible on EC2 to remove an esixting docker container, pull the latest version of the docker images with unique tag and run it with appropriate ENVs or volumes.

# Ansible Playbook command
$ ansible-playbook -i ansible_docker/hosts ansible_docker/rocky.yml --extra-vars "TAG_VERSION=<docker_image_tag>"
