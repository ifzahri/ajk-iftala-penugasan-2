# Penugasan 2 Oprec AJK (Ansible)

|    NRP     |      Nama      |
| :--------: | :------------: |
| 5025221002 | Iftala Zahri Sukmana |

## Goals

This Ansible workspace is designed to automate the deployment of a full-stack application. It includes roles for setting up the backend, frontend, and MySQL database, as well as configuring Nginx as a reverse proxy.

## Directory Structure

The workspace is organized into several roles, each with its own tasks and variables:

```
.
├── ansible.cfg
├── env
│   └── vars.yml
├── inventory.ini
├── playbooks
│   ├── build.yml
│   ├── deploy.yml
│   ├── main.yml
│   ├── migrate.yml
│   └── prepare.yml
├── README.md
└── roles
    ├── backend-build
    │   ├── tasks
    │   │   └── main.yml
    │   └── vars
    │       └── main.yml
    ├── backend-deploy
    │   ├── handlers
    │   │   └── main.yml
    │   ├── tasks
    │   │   └── main.yml
    │   ├── templates
    │   │   └── nginx-backend.j2
    │   └── vars
    │       └── main.yml
    ├── backend-migrate
    │   ├── tasks
    │   │   └── main.yml
    │   └── vars
    │       └── main.yml
    ├── frontend-build
    │   ├── tasks
    │   │   └── main.yml
    │   └── vars
    │       └── main.yml
    ├── frontend-deploy
    │   ├── handlers
    │   │   └── main.yml
    │   ├── tasks
    │   │   └── main.yml
    │   ├── templates
    │   │   └── nginx-frontend.j2
    │   └── vars
    │       └── main.yml
    ├── mysql-prepare
    │   ├── tasks
    │   │   └── main.yml
    │   └── vars
    │       └── main.yml
    └── nginx-prepare
        ├── handlers
        │   └── main.yml
        ├── tasks
        │   └── main.yml
        └── templates
            └── nginx.conf.j2
```

- `roles/backend-build`: Contains tasks for setting up the backend, including installing dependencies and configuring environment variables.

- `roles/backend-deploy`: Contains tasks for deploying the backend, including configuring Nginx and starting the backend server.

- `roles/frontend-build`: Contains tasks for setting up the frontend, including installing Node.js and Yarn, and building the frontend application.

- `roles/frontend-deploy`: Contains tasks for deploying the frontend, including configuring Nginx and starting the frontend server.

- `roles/mysql-prepare`: Contains tasks for setting up MySQL, including installing the server and setting the root password.

- `roles/nginx-prepare`: Contains tasks for setting up Nginx, including installing the server and configuring firewall rules.

Each role's variables are defined in a `vars/main.yml` file, and tasks are defined in a `tasks/main.yml` file.

## Task Workflow

The deployment process is divided into several stages:

- Prepare the MySQL server: Install the MySQL server and set the root password.
- Prepare Nginx: Install Nginx, configure firewall rules, and disable the default site.
- Build the backend: Install dependencies, configure environment variables, and generate application keys.
- Deploy the backend: Configure Nginx, start the backend server, and test the backend.
- Build the frontend: Install Node.js and Yarn, clone the frontend repository, install dependencies, and build the frontend application.
- Deploy the frontend: Configure Nginx, start the frontend server, and test the frontend.

## Output

![2024-04-24 12_58_47-Clipboard](https://github.com/ifzahri/ajk-iftala-penugasan-2/assets/59218445/5eb73423-f8bd-46a0-b60e-f01078f6d6f3)

![2024-04-25 21_09_02-build yml - ajk-iftala-penugasan-2  SSH_ 192 168 154 138  - Visual Studio Code](https://github.com/ifzahri/ajk-iftala-penugasan-2/assets/59218445/5402d65d-affa-4520-9dac-5f6ea06263b6)

![Screenshot 2024-04-26 000450](https://github.com/ifzahri/ajk-iftala-penugasan-2/assets/59218445/0b57561b-d557-4ca6-9381-31f51faf48f4)

![Screenshot 2024-04-26 003728](https://github.com/ifzahri/ajk-iftala-penugasan-2/assets/59218445/0c34b36c-c96f-42df-a9e1-c621b32ea31f)

![Screenshot 2024-04-26 171712](https://github.com/ifzahri/ajk-iftala-penugasan-2/assets/59218445/ebf147c4-d287-46ce-8b1b-acb8f129aea7)
