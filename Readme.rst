Provisioning
============

Setup
-----

Create *hosts* file with the content::

    [local]
    localhost 

    # in case you use virtual environment you will need as well
    [local]
    localhost ansible_python_interpreter=/PATH_TO/Venv/python


Make a directory *mkdir ~/.ansible*

Download the inventory script *wget -O ~/.ansible/ec2.py https://raw.github.com/ansible/ansible/devel/plugins/inventory/ec2.py*

Download the configuration for the inventory script *wget -O ~/.ansible/ec2.ini https://raw.github.com/ansible/ansible/devel/plugins/inventory/ec2.ini*

Make executable *chmod +x ~/.ansible/ec2.py*. 

Install aws tools *pip awscli*, this comes with *boto* which is a python library to call the AWS library.

Credentials
~~~~~~~~~~~

You can use the cli environment by setting up

Credentials:: 

    AWS_SECRET_ACCESS_KEY
    AWS_ACCESS_KEY_ID


Running
-------


Provision the stack *ansible-playbook -i hosts -vv provision-ec2-classic.yml* - this will connect to AWS and
provision servers.



