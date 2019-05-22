# helloworld_ec2_ansible_php
A very simple PHP app that is deployed to an EC2 Red Hat (ami-079596bf7a949ddf8)

# Requirements
In order for this to work, you'll need to have an Amazon EC2 Red Hat instance running. Copy and paste the Public DNS for your EC2 instance in the hosts file where it says insert-public-dns-here.

You'll also need the key pair .pem file generated when you started the EC2 instance, or one that you've previously saved. Make sure it's in your .ssh directory.

Once your EC2 instance is available, you can run the Ansible playbook with the following command, but replace keypair-file.pem with the name of the .pem file in your .ssh directory.
```
ansible-playbook -i hosts aws_lamp_setup.yml --key-file "~/.ssh/keypair-file.pem"
```

Then all you have to do is copy & paste the Public DNS of your EC2 instance into your favorite web browser, and you'll see a simple hello-world PHP page.
