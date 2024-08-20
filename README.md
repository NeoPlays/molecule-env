# Molecule Test Environment

This repository contains a poetry project to handle dependencies for a molecule test environment.

The current [pyproject.toml](pyproject.toml) file is configured to suit the [ethereum-node](https://github.com/stereum-dev/ethereum-node) repository.

## Usage
This is all you need if you want to run molecule tests for the [ethereum-node](https://github.com/stereum-dev/ethereum-node) repository.

```
poetry shell    # Activate the virtual environment
poetry install  # Install dependencies
ansible-galaxy collection install community.docker -p .venv/lib/python3.10/site-packages/ansible_collections
```
Manage your dependencies with the following commands:
```
poetry add <package>    # Add a package to the project
poetry remove <package> # Remove a package from the project
```
If your project is dependent on an ansible collection, you can install it with the following command:
```
ansible-galaxy collection install <ansible-collection> -p .venv/lib/python3.10/site-packages/ansible_collections
```
