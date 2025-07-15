This repository contains a collection of Ansible playbooks designed to automate system administration tasks, validate playbook syntax, and retrieve network information

📁 Ansible Playbooks Repository

This repository contains a collection of Ansible playbooks designed to:  

- ✅ Validate playbook syntax  
- 🌐 Retrieve network and system information  
- ⚙️ Automate system administration tasks   

___

🧠 ##Language: Ansible, YAML 
- **Ansible**, **YAML**

📦 ##GitHub Repository: 
- `TestAnsibleFiles`  

🛠️ ##GitHub Actions Workflow

- **run_ansible.yaml**  
This GitHub Actions workflow automates the execution of an Ansible playbook whenever changes are pushed to any branch.  
- **publish_confluence.yaml**  
This GitHub Actions workflow is automated when ever changes are made to the README and updates it directly to Confluence.
- **Purpose**: CI/CD automation for infrastructure validation or configuration using Ansible  
- **Runs On**: `ubuntu-latest`  

🔑 **Key Steps**  
- 📦 Installs Ansible  
- 📥 Checks out the repository code  
- 🐍 Sets up Python  
- 🧭 Prints the current directory and file list for debugging  
- ▶️ Executes the specified Ansible playbook (`get_python_version.yaml` by default) using `dawidd6/action-ansible-playbook`  

⚙️ **Customizable Inputs**  
- `playbook`: Change to any playbook in your repo  
- `directory`: Path to your playbook directory  
- `inventory`: Inventory file used for targeting hosts  

🚀 **Running Playbooks**  
To run any of the following playbooks, use:  
`ansible-playbook <playbook-name>.yaml`  

📡 **ip_address.yaml**  
- **Purpose**: Network diagnostics and inventory  
- **Key Feature**: Outputs all IPv4 addresses of the host using Ansible's built-in facts module  

🧹 **removedata.yaml**  
- **Purpose**: Disk space management and system health checks  
- **Key Features**:  
  - Checks if the `/boot` partition is over 80% full  
  - Removes old kernel installations  
  - Mounts a remote NFS share  
  - Executes a system check script from the mounted directory  

🧪 **validator.yaml**  
- **Purpose**: Ensure playbook correctness before deployment  
- **Key Feature**: Recursively finds and checks `.yaml` files in `/etc/ansible/playbooks` for syntax errors  

🖥️ **get_os.yaml**  
- **Purpose**: Identify the OS type and version for inventory or compatibility checks  
- **Key Feature**: Uses Ansible facts to print OS name and version (e.g., Ubuntu 22.04)  

🐍 **get_python_version.yaml**  
- **Purpose**: Ensure compatibility with Python-based tools or scripts  
- **Key Feature**: Outputs the full Python version (e.g., 3.9.16) using Ansible facts  

🧾 **inventory.yaml**  
- **Purpose**: Local testing and development  
- **Key Feature**: Defines a basic Ansible inventory with a single `localhost` target using local connection  

📝 **publish_confluence_playbook.yaml**
- **Purpose**: Publishes to Confluence: It executes an Ansible playbook (publish_confluence_playbook.yaml) that likely updates a Confluence page with the contents of the README.md.
- **Key Features**:  
  - Sets up the environment: It checks out the code, sets up Python, installs Ansible and required dependencies, including the community.general collection.
  - Publishes to Confluence: It executes an Ansible playbook (publish_confluence_playbook.yaml) that likely updates a Confluence page with the contents of the README.md.

🌐 **Visual Diagram**  
![Visual Diagram](Pipelinestructure.png)

https://github.com/rayk101/TestAnsibleFiles/blob/testbranch15v/Pipelinestructure.png?raw=true