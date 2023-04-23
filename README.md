# Cookiecutter Zephyr Downstream Project

A cookiecutter to create a standardized Zephyr downstream project ready for production.

## Features

* canonical project structure with needed boilerplate in place
  * west integration
  * cmake integration
  * Kconfig integration
* scaffolds for downstream
  * applications
  * drivers
  * libs
  * tests

## Prerequisites 

You should have Python 3.8+ and [Cookiecutter](http://cookiecutter.readthedocs.org/en/latest/installation.html) installed. 

## Scaffold a new Project

```bash
mkdir ws && cd ws
cookiecutter https://github.com/tiacsys/cookiecutter-zephyr-downstream.git
```

You may now `git init` your project and/or follow the `README.md` inside your newly created project. 

## Prompts

When you create the project, you are prompted to enter these values.

### Templated Values

| Key  | Default Value  |
|---|---|
| project_name  | Zephyr Downstream  |
| project_name_slug  | derived from project_name but can be overridden if so desired  |
| project_org  | Acme Inc.  |
| project_org_slug  | derived from project_name but can be overridden if so desired  |
| repo_url| derived from project_name_slug and project_org_slug but can be overriden if so desired |