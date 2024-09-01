**Azure VM Terraform Deployment**
Welcome! This repository helps you set up a Linux Virtual Machine on Microsoft Azure using Terraform. Whether you’re looking to spin up a new VM for development, testing, or just exploring, you’re in the right place!

**What’s Inside?**
Here’s what this Terraform setup will create for you:

**Resource Group:** A container for your Azure resources.
**Virtual Network:** The network within which your VM will reside.
**Subnet: **A smaller network within the Virtual Network.
**Public IP Address:** An IP address to connect to your VM from the outside world.
**Network Interface:** Connects your VM to the Virtual Network.
**Linux Virtual Machine:** The actual VM that you’ll work on.
_**Prerequisites**_
Before you get started, make sure you have:

**Terraform:** Download and install it from Terraform’s website.
**Azure CLI:** Install it from Azure’s installation guide.
Getting Started

**1. Authenticate with Azure**
First things first, you need to be logged into Azure. Open your _terminal and run:_

_bash_
Copy code
**az login**
This will open a browser window where you can sign in to your Azure account.

**2. Set Up GitHub Authentication**
If you’re planning to push changes to GitHub, you’ll need a _Personal Access Token (PAT)._ Here’s how you can use it:

_Generate a PAT: Go to your GitHub settings and generate a new PAT with appropriate scopes.
Configure Git: Update your remote URL to use this PAT:_

_bash_
Copy code
_git remote set-url origin https://<username>:<PAT>@github.com/<username>/<repo>.git
Replace <username>, <PAT>, and <repo> with your GitHub username, your PAT, and your repository name._

**3. Customize Your Configuration**
In the terraform.tfvars file, you can customize:

**admin_username:** The username for your VM.
**admin_password:** The password for your VM.
Feel free to set these to whatever you prefer!

**4. Deploy Your Infrastructure**
Now that you’re all set up, it’s time to deploy! Follow these steps:

**Initialize Terraform:**

_bash_
Copy code
**terraform init**
This prepares Terraform to work with your configuration.

**Preview the Changes:**

_bash_
Copy code
**terraform plan**
This shows you what Terraform is going to do. It’s a good chance to double-check everything.

**Apply the Configuration:**

_bash_
Copy code
**terraform apply**
This creates your resources on Azure.

**Clean Up (if needed):**

If you want to remove everything, use:

_bash_
Copy code
**terraform destroy**
VM Details
**VM Size:** _Standard_F2._ This is a general-purpose VM size, suitable for most basic tasks and testing.
**Need Help?**

If you run into any issues or have questions, feel free to reach out or check the Terraform Azure Provider documentation for more help.

License
This project is licensed under the **MIT License.** See the LICENSE file for details.
