<div align="center">
<h1>🚀 AWS EC2 Bash Manager 🚀</h1>
<p>
A collection of Bash scripts to streamline the management of AWS EC2 instances on Ubuntu, focusing on automation of instance lifecycle and security key operations.
</p>

<p>
<img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT">
<img src="https://img.shields.io/badge/Platform-Ubuntu-orange.svg" alt="Platform: Ubuntu">
<img src="https://img.shields.io/badge/AWS-EC2-yellow.svg" alt="Service: AWS EC2">
<img src="https://img.shields.io/badge/Shell-Bash-lightgrey.svg" alt="Shell: Bash">
</p>
</div>
📖 Table of Contents

    Description

    Features

    Prerequisites

    Installation

    Usage

    Contributing

    License

📝 Description

This project provides a set of powerful Bash scripts designed to simplify common tasks for managing AWS EC2 instances. Whether you are launching new instances, stopping existing ones, or managing security credentials, these scripts automate the process right from your Ubuntu terminal. This toolkit is ideal for developers, system administrators, and DevOps engineers who work with AWS and want to improve their workflow efficiency.
✨ Features

    🚀 Launch EC2 Instances: Quickly launch pre-configured EC2 instances.

    🔌 Stop/Start/Terminate Instances: Manage the state of your instances with simple commands.

    🔐 Security Key Management: Automate the creation and management of .pem security keys.

    💻 SSH Automation: Scripts to simplify SSH connections to your instances.

    📋 Instance Listing: View details of your running EC2 instances.

    ⚙️ Configurable: Easily configure instance types, AMIs, and other parameters.

🛠️ Prerequisites

Before you begin, ensure you have the following set up:

    An AWS Account with the necessary permissions to manage EC2 instances.

    AWS CLI installed and configured on your local machine. You can install it by following the official AWS CLI installation guide.

    Ubuntu as your operating system (or any Debian-based Linux distribution).

    jq installed for parsing JSON responses from the AWS CLI. Install it using:

    sudo apt-get update && sudo apt-get install -y jq

💾 Installation

    Clone the repository:

    git clone https://github.com/your-username/aws-ec2-bash-manager.git
    cd aws-ec2-bash-manager

    Make the scripts executable:

    chmod +x *.sh

👨‍💻 Usage

Below are some examples of how to use the scripts.
Launch a New EC2 Instance

This script will create a new security key, launch an EC2 instance, and associate the key with it.

./launch_instance.sh --instance-type t2.micro --ami-id ami-0c55b159cbfafe1f0 --key-name MyNewKey

Connect to an Instance via SSH

Use this script to easily SSH into a running instance using its instance ID and the corresponding security key.

./connect_ssh.sh --instance-id i-0123456789abcdef0 --key-path ~/.ssh/MyNewKey.pem

Stop an EC2 Instance

To stop a running instance, simply provide its instance ID.

./stop_instance.sh --instance-id i-0123456789abcdef0

🤝 Contributing

Contributions are welcome! If you have suggestions for improvements or new features, feel free to fork the repository and submit a pull request. You can also open an issue with the "enhancement" tag.

    Fork the Project

    Create your Feature Branch (git checkout -b feature/AmazingFeature)

    Commit your Changes (git commit -m 'Add some AmazingFeature')

    Push to the Branch (git push origin feature/AmazingFeature)

    Open a Pull Request

    📄 License

This project is distributed under the MIT License. See the LICENSE file for more information.
