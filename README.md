# workstation-setup

Ansible playbooks to provision a new Mac with my standard dev environment.

## What's included

| Role | What it does |
|---|---|
| `homebrew` | Installs Homebrew if not present |
| `development_folder` | Creates `~/Development` |
| `oh_my_zsh` | Installs oh-my-zsh |
| `zsh_config` | Adds shell aliases (`cc`, `cdx`, `dev`, `gs`) to `~/.zshrc` |
| `claude` | Installs Claude Code CLI, Plannotator, copies `settings.json`, `CLAUDE.md`, ccstatusline config, and custom skills |
| `agents` | Creates `~/.agents/AGENTS.md` and copies home reference files (`PULL_REQUESTS.md`, `COMMIT_MESSAGES.md`, `OPINIONS.md`, `VOICE.md`) |
| `cmux` | Installs cmux |

## Setup

**1. Install uv**

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**2. Install Ansible**

```bash
uv tool install ansible
```

**3. Clone this repo**

```bash
git clone https://github.com/PurplePros/workstation-setup.git ~/Development/workstation-setup
cd ~/Development/workstation-setup
```

## Run

**Everything:**

```bash
ansible-playbook site.yml -i inventory.ini
```

**Single role:**

```bash
ansible-playbook site.yml -i inventory.ini --tags <role>
```

For example:

```bash
ansible-playbook site.yml -i inventory.ini --tags claude
```

**Dry run:**

```bash
ansible-playbook site.yml -i inventory.ini --check
```

## After provisioning

- mattpocock-skills install automatically from the marketplace the first time Claude Code runs
