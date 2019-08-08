ansible-role-jupyter
=======================

Install the latest version of jupyter.
Intended for use with development virtual machines.

Jupyter is a web app used to run python with various graphic options.

Summary of installation tasks:
    - Install jupyter, ipython and ipykernel.
    - Set up ipython config.
    - Generate jupyter password based on config.
    - Configure and start jupyter daemon which uses the virtualenv.
    - Jupyter server exposed on port 8888.

Requirements
------------

- `Django <https://www.djangoproject.com/>`_
- `docker <https://www.docker.com/>`_

Role environment variables
--------------

See all variables in `<vars/main.yml>`_, see `<default/main.yml>`_ for
defaults.

Dependencies
------------

- https://github.com/yobota/ansible-role-python3

Usage instructions
------------------

Include this line in a requirements.yml::

    - src: https://github.com/yobota/ansible-role-jupyter

And include the role in a playbook.yml::

    - hosts: all
      roles:
         - ansible-role-jupyter

When you next provision your VM, jupyter will be installed by ansible.

Checking syntax and linting
---------------------------

Make sure that you have ``molecule``. If not, read the docs on interaction.

To lint use:

    molecule lint

To check syntax use:

    molecule syntax

Author information
------------------

Billy Liggins <Billy@yobota.xyz>
