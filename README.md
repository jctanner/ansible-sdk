# ansible-sdk

## What is this?

A prototype developers kit for Ansible Collections.

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
