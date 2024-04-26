# docker-templates
Docker templates to quicky setup different environments

### Structure

* 00-archive: Old versions (7.0, 7.1, 7.2) and tests
* 00-template: Base template
* 01-template-staging: Base template for staging setup
* 202x.qx.x: Quarterly Releases

### DB Connection
A env variable needs to be defined for connecting with your local database system: `MACHINE_HOST_IP`. It is used in `componse.yml` files. 

It can be initialized like that in `~/.bashrc`:

    export MACHINE_HOST_IP=$(hostname -I | awk '{print $1}')
