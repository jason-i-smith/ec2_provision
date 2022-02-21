# EC2 Provision

This role is designed to configure the necessary elements to instantiate an AMI image into AWS EC2.

## Requirements

This role uses various EC2 modules, the boto package is required.

    # pip install boto

## Role Variables

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

### defaults/main.yml:

### Provision

Once the variables have been defined within the role, the playbook can be run to provision the instance within AWS.

    # ansible-playbook main.yml


### Teardown

Default position of this role is to provision instances, so the default value of `teardown` variable is false.  If you want to terminate instance(s) and remove AWS VPC elements, set teardown to true.  This can be done within the defaults/main.yml variable, or at runtime by using the `--extra-vars 'teardown=true'`

    # ansible-playbook --extra-vars 'teardown=true'

or

    # ansible-playbook -e 'teardown=true'

## License

BSD

## Author Information

Jason I Smith (json@redhat.com)
