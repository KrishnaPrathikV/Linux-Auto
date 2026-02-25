# Network Automation Lab (Python + Ansible)

A practical end-to-end network automation repo that covers:

- Inventory-driven automation (YAML inventory)
- Config backup (per device)
- Jinja2 config rendering (templates)
- Validation checks (simple policy rules)
- Config push (Netmiko) and Ansible playbooks
- Logging + reports
- Tests + GitHub Actions CI

## What this repo automates

1) **Backup** running-config from devices (via SSH / Netmiko or Ansible)
2) **Render** configuration snippets from Jinja2 templates
3) **Validate** output against basic rules (no forbidden commands, required lines present)
4) **Push** approved config changes

## Requirements

- Linux (Ubuntu recommended)
- Python 3.10+
- SSH access to devices (real lab, EVE-NG, or DevNet)
- (Optional) Ansible

## Quick start (Linux)

```bash
git clone <your-repo-url>
cd network-automation-lab

# create venv + install deps
bash scripts/setup_venv.sh

# update inventory
nano inventories/devices.yml

# run backup + render + validate
bash scripts/run_all.sh
