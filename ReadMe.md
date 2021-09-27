# Launch Docker Desktop Containers with Ansible

Use Ansible to launch one or more container instance(s) in your local [Docker Desktop](https://docker.com) environment.

## Run


1. Download, install and run [Docker Desktop](https://docker.com) on your workstation

1. Setup your environment with pipenv

    ```bash
    pip install --upgrade pip
    pip install pipenv
    pipenv install --python 3.9
    pipenv install docker ansible six
    pipenv shell
    ```

2. Edit the `containers.yaml` file and [un]comment the respective Ansible role(s) you want launched in Docker


3. Run the playbook to launch the container(s) in Docker Desktop using Ansible :

   ```bash
   ansible-playbook containers.yaml
   ```

4. Connect to the local instance with the appropriate options:
   - alpine
     - `docker run -it alpine sh`
   - nginx
     - `https://localhost:8080`
     - `docker run -it nginx sh`
   - ubuntu
     - `docker run -it ubuntu bash`



## Resources

- [community.docker.docker_container](https://docs.ansible.com/ansible/latest/collections/community/docker/docker_container_module.html) Ansible module


## License

This repository is licensed under the [MIT License](https://choosealicense.com/licenses/mit/).

