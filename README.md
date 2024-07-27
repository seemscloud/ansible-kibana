# Observability Logging

## Tags

### Permissions / Spaces

| Users              | Roles              | Space               | Data Views              | Settings              |
|--------------------|--------------------|---------------------|-------------------------|-----------------------|
| kibana-users-run   | kibana-roles-run   | kibana-spaces-run   | kibana-data-views-run   | kibana-settings-run   |
| kibana-users-debug | kibana-roles-debug | kibana-spaces-debug | kibana-data-views-debug | kibana-settings-debug |

### APM

| Agent Policies              | Integrations              |
|-----------------------------|---------------------------|
| kibana-agent-policies-run   | kibana-integrations-run   |
| kibana-agent-policies-debug | kibana-integrations-debug |

### Run all

| Name             |
|------------------|
| kibana-run-all   |
| kibana-debug-all |

---

## Playbook Execution Snippets

### Ansible Vault Password from File

```bash
--vault-password-file /home/mkatana/configs/ansible/vault-logging-system.txt
```

### Onprem Prod

```bash
ansible-playbook playbooks/onprem-prod.yaml \
  --ask-vault-pass \
  --inventory inventories/hosts.yaml \
  --tags kibana-run-all
```

### Onprem Test

```bash
ansible-playbook playbooks/onprem-test.yaml \
  --ask-vault-pass \
  --inventory inventories/hosts.yaml \
  --tags kibana-run-all
```

### GCP Prod

```bash
ansible-playbook playbooks/gcp-prod.yaml \
  --ask-vault-pass \
  --inventory inventories/hosts.yaml \
  --tags kibana-run-all
```

### GCP Test

```bash
ansible-playbook playbooks/gcp-test.yaml \
  --ask-vault-pass \
  --inventory inventories/hosts.yaml \
  --tags kibana-run-all
```

### Azure Prod

```bash
ansible-playbook playbooks/azure-prod.yaml \
  --ask-vault-pass \
  --inventory inventories/hosts.yaml \
  --tags kibana-run-all
```
