# JupterLab Service on Sparrow

## Accessing the system

You must either be logged into the VPN or on the 
The service is available at
https://
Please log in the username and password that have been provided to you.
*TODO: change to permanent name when available: https://chemistry.sparrow.cf.ac.uk*
*TODO: SCW usernames will be accessible when issue with LDAP integration is resolved.*

When you log into the service for the first time it will take a few minutes for the system to set up your user environment, please be patient.

You can access your JupyterLab environment from multiple locations

## Storage
Your home directory in the JupyerLab is provided by the Ceph storage on the Sparrow system
You can upload files from your local machine using the 
Internet access is  

## Conda environments

There are three Anaconda environments 
1. persistent
2. base/root
3. clean

The `persistent` environment is the recommended environment for you to use and should be set as the default environment (marked with a \*) and the environment used by the "Python 3 (ipykernel)" kernel.
Any packages installed into this Anaconda environment will persist between sessions.
Some additional packages (numpy, matplotlib, pysjef, ...) have been installed into this environment.

The `base` environment (sometimes labelled `root`) has the same configuration as the persistent environment but any changes made to this environment will be lost when the JupyterLab environment is restarted.

The `clean` environment is a clean default Anaconda environment which can be used as the base for user-defined environments if there are any package conflicts with the other conda environments.

### Installing packages

### Creating additional Anaconda environments 

## Access to hawk
An ssh key is generated for each user on first login

https://github.com/nick-wilson/sparrow-examples/blob/master/ssh-copy-id.ipynb

## pysjef & Molpro

## Further documentation
https://docs.jupyter.org
