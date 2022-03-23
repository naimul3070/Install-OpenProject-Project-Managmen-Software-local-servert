# Install-OpenProject-Project-Managmen-Software-local-server

Install And get Backup OpenProject in Local Server


# Install Process
# What we need
Ubuntu OS (Installed)
Pg-Admin (Installed)

# For install PG-Admin can folloy the link:  https://github.com/naimul3070/Install-PG-Admin.git

Commands for Install open project 

# Add PGP Key
wget -qO- https://dl.packager.io/srv/opf/openproject/key | sudo apt-key add -


# Integrate OpenProject repository in Ubuntu 20.04

sudo wget -O /etc/apt/sources.list.d/openproject.list https://dl.packager.io/srv/opf/openproject/stable/12/installer/ubuntu/20.04.repo


# Press Y for confirmation

# Run system update

sudo apt update

# Command to install OpenProject in Ubuntu 20.04 LTS

sudo apt install openproject


Press Y for confirmation 

# Start configuring OpenProject

sudo openproject configure

Use The IP of the OS

# Skib SSL
# Install subversion repository support
# skip STMP


Now check the Domain You Will get the open Project
