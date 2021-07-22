# CI/CD using GitHub Actions
- Fork the repository
- Launch 2 EC2 instances with Amazon Linux 2 AMI with t2.micro capacity.
- Install light-weight httpd web server
- Open Security Group ports 22 to outside world & 80 to your public IP address.
- SSH into the EC2 instances.
- Modify /var/www/html/ directory permissions to ec2-user using chown.
- Create environments in GitHub. 
- Add environment secrets for SCP step in the respective environment.
- Ensure you have 2 branches develop & master pointing to 2 environments respectively having the same code.
- Execute GitHub Actions

# Testing Upgrades
- Update the code in develop branch to reflect the latest changes.
- Create a pull request to master branch and view the latest changes in the production environment.

# Security
- We can have branch protection rules to ensure no one commits code to the master branch.
- We have mapped a branch to an environment but we could have other pipeline strategies.
- We could run static code analysis & security checks on pull requests.

# Refer the following architecture diagram : https://lucid.app/documents/view/37685dcc-42aa-4009-891e-5bdd5be783fc
