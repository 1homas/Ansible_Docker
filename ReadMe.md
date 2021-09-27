# Docker Ubuntu Container

Launches a simple NGINX container instance in your local [Docker Desktop](https://docker.com) environment.

## Run


1. Launch [Docker Desktop](https://docker.com) on your local computer

1. Setup your environment with pipenv

    ```bash
    pip install --upgrade pip
    pip install pipenv
    pipenv install --python 3.9
    pipenv install docker ansible six
    pipenv shell
    ```

1. Launch a container in Docker Desktop using Ansible :

   ```bash
   ansible-playbook containers.yaml
   ```

1. Connect to the local instance:
   - alpine
     - `https://localhost:8080`
     - `docker run -it alpine sh`
   - nginx
     - `docker run -it nginx sh`
   - ubuntu
     - `docker run -it ubuntu bash`



## Resources

- [community.docker.docker_container](https://docs.ansible.com/ansible/latest/collections/community/docker/docker_container_module.html) Ansible module


## License

This repository is licensed under the [MIT License](https://choosealicense.com/licenses/mit/).

