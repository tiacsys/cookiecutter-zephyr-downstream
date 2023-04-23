# {{cookiecutter.project_name}}

Here goes some description

## Getting Started


### Step 1

Prepare a fresh workspace, we prefer to keep all additional python packages inside a python virtualenv:

```bash
mkdir {{cookiecutter.project_name_slug}}_ws && cd {{cookiecutter.project_name_slug}}_ws
python3 -m venv .venv
source .venv/bin/activate
pip install pip --upgrade
pip install west
```

### Step 2

Clone the repo, initialize the workspace and populate with the required modules. Check `{{cookiecutter.project_name_slug}}/west.yml` for details:

```bash
git clone {{cookiecutter.repo_url}}
west init -l {{cookiecutter.project_name_slug}}
west update
```

### Step 3

Install needed python dependencies

```bash
pip install -r zephyr/scripts/requirements.txt
pip install -r {{cookiecutter.project_name_slug}}/scripts/requirements.txt
```

You also need a recent version of `cmake` and a compiler toolchain suitable to build Zephyr applications installed. 
Check the official upstream documentation [how to install one](https://docs.zephyrproject.org/latest/develop/getting_started/index.html#install-zephyr-sdk). 

## Building first applications

Build the `hello_world` example from the Zephyr upstream repo

```bash
west build -b qemu_cortex_m3 zephyr/samples/hello_world/
```

and run it (assuming you installed the official Zephyr SDK)

```bash
west build -t run
```


## Credits

This project was bootstrapped with cookiecutter-zephyr-downstream.