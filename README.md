# <center>CLC Product Installation <center>Template

## Overview
The CLC-Product-Installation-Template is a template Ansible playbook which is intended to simplify the process of defining the installation steps of a product.  The template is designed to allow you to centralize your installation tasks 

## Getting Started
To get started you should first focus on defining a playbook which will install your product and configure it to provide the best customer experience.  When this playbook is complete and tested it's time to integrate it into this template.  This template playbook provides the fundemental operations necessary to integrate and register the product installation with the CLC platform.

## Property Updates
There are a few properties which need to be specified by you.  These properties identify the product and you as the vendor.

These properties are found in this template in the file `roles/product_registration/defaults/main.yml`.
These properties are:

- providerAlias
	- This is your CLC Account Alias.
- productId
	- This is the product ID which is defined by you and the platform team for billing and management purposes.
- name
	- This is simply the name of your product.	 

Example:

```
	"providerAlias": "PROV"
	"productId": "MKTPLC-MONTHLY-TEST-01"
	"name": "sample product"
```

## Installation Tasks
Installation tasks are specified in the `roles/install_product/tasks/main.yml` file.  There are multiple approaches to adding your tasks to this project.  These approaches are described below.

## Different Approaches 
### Direct Definition
This approach assumes that you currently don't have a playbook for installing your product.  The steps below outline the highlevel actions needed to create your copy of the template and define your installation process.

1. Fork the this template project.
2. Update the roles/product_registration/defaults/main.yml file with information about you and your product.
3. Update the roles/install_product/tasks/main.yml file with the tasks required to install your product.  Add your tasks within the `block` section of the file.

### Bootstrap
This approach assume that you currently have play (or a single Ansible yml task file) which defines the tasks necessary to install your product.

1. Fork this template product.
2. Update the roles/product_registration/defaults/main.yml file with information about you and your product.
3. Copy your current playbook yml files into roles/install_product/tasks
4. Update roles/install_product/tasks/main.yml.  Change the contents of the `block` by adding an `- include: <file.yml>` 


### Instrumenting Your Own Playbook
This approach is for a product owner who has a complete playbook implementation for installing their product.  In this approach we are simply instrumenting the playbook with the roles and variables that need to be defined in order to integrate with the CLC platform.

1. Clone this project.
2. Copy the product_registration role from this project into your product playbook project.
3. Update the roles/product_registartion/defaults/main.yml file with information about you and your product.
4. Update your main.yml file by adding a call to the product_registration role.  For example:

```
	roles:
	  - product_registration
```
	  
## Getting Your Product To Market
At CLC we have an ECO-System team which works with Vendors and companies to get their products listed in our maket place.  Please reach out to the CLC ECO-System team for more information.
