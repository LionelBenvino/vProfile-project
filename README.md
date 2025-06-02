# vProfile Project – Customized Multi-Tier Web Application

This repository contains a customized implementation of the **vProfile Project**, originally created by [hkhcoder](https://github.com/hkhcoder/vprofile-project), and adapted as part of my DevOps training and portfolio.

The goal of this project is to demonstrate the deployment and configuration of a multi-tier web application using manual and automated provisioning with Vagrant. This setup is intended for local environments and includes multiple services running across several virtual machines.

## Project Overview

The vProfile application simulates a production-like infrastructure composed of the following components:

- Java-based web application deployed on Apache Tomcat
- MySQL (MariaDB) as the relational database
- Memcached for caching
- RabbitMQ for messaging
- Nginx as reverse proxy (on web01)
- Multi-VM environment provisioned using Vagrant and shell scripts

This setup demonstrates the manual and automated provisioning of services and their configuration across multiple VMs to create a complete development environment.

## Repository Structure

- `vagrant/Manual_provisioning_WinMacIntel/`  
  Contains a detailed PDF guide (`VprofileProjectSetupWindowsAndMacIntel.pdf`) with step-by-step instructions for manual setup of each VM and service.

- `vagrant/Automated_provisioning_WinMacIntel/`  
  Contains all necessary provisioning scripts and Vagrantfiles to automatically deploy the full multi-tier application. Running `vagrant up` inside this directory will set up everything end-to-end.

## Customization

This version of the project includes personalized changes in the Java application source code, such as displaying my name in the UI. It serves both as a hands-on DevOps learning exercise and a portfolio project.

# Prerequisites

- JDK 17 or 21
- Maven 3.9
- MySQL 8

# Technologies
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- Tomcat
- MySQL
- Memcached
- Rabbitmq
- ElasticSearch
# Database
Here,we used Mysql DB
sql dump file:
- /src/main/resources/db_backup.sql
- db_backup.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < db_backup.sql

## Usage Instructions

To run the project locally with automated provisioning:

1. Clone the repository:
   ```
   git clone https://github.com/LionelBenvino/vProfile-project.git
   cd vProfile-project/vagrant/Automated_provisioning_WinMacIntel/
   ```

2. Launch the environment:
   ```
   vagrant up
   ```

3. Access the application in your browser at:
   ```
   http://web01/
   ```

4. Default credentials:
   - Username: `admin_vp`
   - Password: `admin_vp`

## Technical Highlights

- Shell scripting for service installation and VM provisioning
- Vagrant multi-VM setup using VirtualBox
- MariaDB initialization with SQL dump
- WAR deployment using Maven and Tomcat
- Troubleshooting and debugging in a local environment

## Credits

The base version of this project was developed by [hkhcoder](https://github.com/hkhcoder/vprofile-project) as part of Imran Teli’s Udemy course: *DevOps Projects | Real Time DevOps & GitOps Projects*. This customized version was created for personal development and demonstration purposes.

## Author

**Lionel Benvino**  
DevOps Trainee | Systems & Cloud Enthusiast  
[GitHub Profile](https://github.com/LionelBenvino)
