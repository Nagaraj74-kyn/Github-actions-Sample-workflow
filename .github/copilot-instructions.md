# Copilot Instructions for Github-actions-Sample-workflow

## Project Overview
This repository contains sample implementations for DevOps tools:
- **GitHub Actions workflows** in `.github/workflows/` for CI/CD automation
- **Python scripts** in the `../Python/` folder demonstrating basic programming concepts
- **Ansible playbooks** in the `../Ansible/` folder for infrastructure automation

## Key Patterns and Conventions

### Python Scripting
- Use try-except blocks for error handling, returning dictionaries with "Success" and "result" or "Error" keys (see `../Python/callmodule.py`)
- Import functions from custom modules using `from module import func` (e.g., `from My_module import add, subtract`)
- Simple functions for math operations and checks (e.g., even/odd in `../Python/checkevenodd.py`)

### Ansible Automation
- Use `become: yes` for tasks requiring sudo privileges (see `../Ansible/Sample.yaml`)
- Structure playbooks with `hosts: all`, `name`, and `tasks` list
- Common modules: `apt` for package installation, `service` for managing services

### GitHub Actions
- Workflows stored in `.github/workflows/` as YAML files
- Basic structure: `name`, `on` triggers, `jobs` with `runs-on` and `steps`

## Developer Workflows
- **Run Python scripts**: `python filename.py` from the Python directory
- **Execute Ansible playbooks**: `ansible-playbook -i inventory.ini Sample.yaml`
- **GitHub Actions**: Automatically triggered on push/PR to master branch

## File Organization
- Keep workflows in `.github/workflows/`
- Python examples in separate directory for learning purposes
- Ansible samples with accompanying command reference in `.txt` files

## Integration Points
- No external APIs; focuses on local tool demonstrations
- Ansible can integrate with Python scripts via modules if needed