# CLC Product Installation Template

## Overview
The CLC-Product-Installation-Template is a template Ansible playbook which is intended to simplify the process of defining the installation steps of a product.  The template is designed to allow you to centralize your installation tasks 

## Getting Started

## Property Updates

## Installation Tasks

## Different Approaches 
### Direct Definition
This approach assumes that you currently don't have a playbook for installing your product.  The steps below outline the highlevel actions needed to create your copy of the template and define your installation process.

1. Fork the this template project.
2. Update the roles/product_registration/defaults/main.yml file with information about you and your product.
3. Update the roles/install_product/tasks/main.yml file with the tasks required to install your product.  Add your tasks within the `block` section of the file.

### Bootstrap
This aaproach assume that you currently have play (or a single Ansible yml task file) which defines the tasks necessary to install your product.

1. Fork this template product.
2. Update the roles/product_registration/defa
### Instrumenting Your Own Playbook


## Getting Your Product To Market
At CLC we have an ECO-System team which works with Vendors and companies to get their products listed in our maket place.  Please reach out to the CLC ECO-System team for more information.
