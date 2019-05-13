# ansible-sdk

## What is this?

A prototype developers kit for Ansible Collections.

## How to install this

1. Create a virtual env 
```sh
virtualenv --python=$(which python3) sdk.venv
source sdk.venv/bin/activate
pip install git+https://github.com/ansible/ansible
pip install git+https://github.com/jctanner/ansible-test
pip install git+https://github.com/jctanner/ansible-sdk
```

2. Source the venv before you begin working with any of the subsequent commands


## How to get started with a new collection

1. Pick your content directory

```sh
mkdir ~/collections
```

2. Create your namespace

```sh
cd ~/collections
mkdir mynamespace
```

3. "Init" your new collection

```sh
cd ~/collections/mynamespace
molecule init collection -n mynamespace -c mycollection
```

4. Test your new collection

```sh
cd ~/collections/mynamespace/mycollection
molecule test
```

5. Iterate

Create some plugins inside the collection or some roles, and re-run tests until the desired effect is achieved.

6. Build

```sh
cd ~/collections/mynamespace/mycollection
molecule build
```

7. Publish

```sh
cd ~/collections/mynamespace/mycollection
molecule publish
```
