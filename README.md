# Ansible playbook for setup kubernetes cluster

## 1. Install Ansible

```sh
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## 2. Install kubespray collection

```sh
ansible-galaxy install -r requirements.yml
```

## 3. Reset old cluster

```sh
ansible-playbook -i inventory/hosts.yaml  --become -u root reset.yml
```

## 4. Setup new cluster

```sh
ansible-playbook -i inventory/hosts.yaml  --become -u root cluster.yml
```
