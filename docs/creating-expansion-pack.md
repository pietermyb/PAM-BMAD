# Creating Your Own Expansion Pack

This guide will walk you through the process of creating your own expansion pack for the PAM BMAD Method. Expansion packs allow you to extend the functionality of the BMAD Method by adding new agents, teams, and other resources.

## 1. Create a New Directory

First, create a new directory for your expansion pack in the `expansion-packs` directory. The name of this directory will be the ID of your expansion pack.

```bash
mkdir expansion-packs/my-new-pack
```

## 2. Add a `config.yaml` File

Next, create a `config.yaml` file in the root of your new expansion pack directory. This file will contain the configuration for your expansion pack. For now, you can leave this file empty.

```bash
touch expansion-packs/my-new-pack/config.yaml
```

## 3. Create Subdirectories

Create the following subdirectories in your expansion pack directory, as needed:

*   `agents`: Contains the definitions for your new agents.
*   `agent-teams`: Contains the definitions for your new agent teams.
*   `checklists`: Contains any checklists that your agents will use.
*   `data`: Contains any data files that your agents will use.
*   `tasks`: Contains any task definitions that your agents will use.
*   `templates`: Contains any templates that your agents will use.
*   `workflows`: Contains any workflow definitions that your agents will use.

## 4. Define New Agents

To create a new agent, add a new `.md` file to the `agents` directory. This file will contain the agent's persona, commands, and dependencies. You can use the existing agents in the `bmad-core/agents` directory as a reference.

## 5. Define Agent Teams

To create a new agent team, add a new `.yaml` file to the `agent-teams` directory. This file will define the agents that are part of the team. You can use the existing teams in the `bmad-core/agent-teams` directory as a reference.

## 6. Add Supporting Content

Add any supporting content, such as checklists, data files, tasks, templates, and workflows, to the appropriate subdirectories.

## 7. Build the Expansion Pack

Once you have created your expansion pack, you can build it by running the following command:

```bash
node tools/cli.js build --expansions-only
```

This will create a new bundle for your expansion pack in the `dist/expansion-packs` directory.
