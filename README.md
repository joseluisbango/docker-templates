# docker-templates
Docker templates to quicky setup different environments

### Structure

* `00-archive`: Old versions (7.0, 7.1, 7.2) and tests
* `00-template`: Base template
* `01-template-staging`: Base template for staging setup
* `202x.qx.x`: Quarterly Releases
* `7310-template`: 7.3 template
* `7413-template`: 7.4 template
* `remote-elastic-2servers`: 2 Liferay servers + 1 Remote ES instance

### DB Connection
A env variable needs to be defined for connecting with your local database system: `MACHINE_HOST_IP`. It is used in `componse.yml` files. 

It can be initialized like that in `~/.bashrc`:

    export MACHINE_HOST_IP=$(hostname -I | awk '{print $1}')

---

#### Important note regarding empty dirs
Empty dirs have been added to the templates using this workaround: https://stackoverflow.com/a/932982. The following `.gitignonre` file has been added to those directories.

    # Ignore everything in this directory
    *
    # Except this file
    !.gitignore

Note that, if you plan to add files to any of those dirs, you may want to remove that `.gitignore` file.
