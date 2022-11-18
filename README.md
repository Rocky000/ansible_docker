# ansible_docker
I am using Ansible on EC2 to remove an esixting docker container, pull the latest version of the docker images with unique tag and run it with appropriate ENVs or volumes


# Ansible Playbook command
$ ansible-playbook -i ansible_docker/hosts ansible_docker/rocky.yml --extra-vars "TAG_VERSION=<docker_image_tag>"
