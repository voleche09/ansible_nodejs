# Node Js deployed using ansible

This is a sample project of how you can deploy a node JS application using ansible and vagrant.

This will install the following on a CentOS 7 VM

- Node.js
- Express
- A sample of the node js app

## Getting Started

You will need to install the following

- [Virtual Box](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant](https://www.vagrantup.com/downloads)
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

### Installing

To get the project running download the project.

Open the terminal and cd to the project (directory containing the README.md and Vagrantfile)

    cd [project name]

Build virtual machine by running command below

    vagrant up

If an error occurs when running vagrant up or if you have changed anything on the playbook after running vagrant up you can run the command below

    vagrant provision

Note: vagrant provision is only ran after errors that may occur after vagrant up has been ran or if you have changed the playbook.

Edit your host file [Follow link to see how to](https://docs.rackspace.com/support/how-to/modify-your-hosts-file/) by adding the line

    192.168.60.4 nodejs.test

This allows you to connect to the vm using a test hostname rather than the ip

Open your browser and access link [http://nodejs.test/](http://nodejs.test/)

### To shutdown or kill vm

To shutdown the VM run the following command on the project directory

    vagrant halt

To kill or destroy the VM run the following command on the project directory

    vagrant destroy

## Authors

- **Kevin Mugwe** - [Voleche09](https://github.com/voleche09)

## License

This project is licensed under the [CC0 1.0 Universal](LICENSE.md)
Creative Commons License - see the [LICENSE.md](LICENSE.md) file for
details

## Acknowledgments

- [Jeff Geerling](https://github.com/geerlingguy)
