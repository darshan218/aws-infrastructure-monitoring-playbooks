# AWS Infrastructure Monitoring Playbooks

This Bitbucket repository contains Ansible playbooks designed to monitor various aspects of AWS infrastructure. Below are the available playbooks:

## Prerequisites:

1. **Ansible installed locally:**
   Ensure that Ansible is installed on your local machine. You can follow the installation instructions on the [Ansible Installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).

2. **AWS CLI installed and configured:**
   Install the AWS Command Line Interface (CLI) and configure it with the necessary permissions. You can follow the instructions on the [AWS CLI User Guide](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html).

## Playbooks:

### 1. ECS Steady State Monitoring:
   - **Playbook Name:** `ecs_steady_state.yml`
   - **Description:** This playbook checks the steady state of ECS clusters by verifying the desired task count and running task count for a specified ECS service.

   #### Usage:
   ```bash
   ansible-playbook ecs_steady_state.yml -e "cluster_name=your-cluster-name service_name=your-service-name"

Replace your-cluster-name and your-service-name with the appropriate values for your ECS cluster and service.

### 2. EC2 Memory Threshold Check:
   - **Playbook Name:** `ec2_memory_threshold.yml`
   - **Description:** This playbook monitors the memory usage of specified mount points on EC2 instances and checks if the usage exceeds the defined threshold.

   #### Usage:
   ```bash
   ansible-playbook ec2_memory_threshold.yml -e "host_group=your-host-group"

Replace your-host-group with the appropriate host group for your EC2 instances.
