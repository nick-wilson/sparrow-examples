# JupterLab Service on Sparrow

## Accessing the system
You must either be logged into the VPN or on the campus network to access the service.
The service is available at https://chemy-hub.sparrow.cf.ac.uk

## Registering account
You currently need a separate account from your normal ARCCA/SCW account to use this service. The procedure to set up an account is as follows:

 - Click on the "Sign up to create a new user" link
 - Register with same SCW username as used on Hawk and other ARCCA machines
 - After registering for account please email the admins with the the username you have specified so they can verify and track registration
 - Once account has been authorized by the admins then you will be able to log into the service

When you log into the service for the first time it will take a few minutes for the system to set up your user environment, please be patient if it is waiting at the message "Started container notebook".

<!--
TODO: Process with LDAP integration is resolved
TODO: You can access your JupyterLab environment from multiple locations, can use workspaces for different views
TODO: How to shut down notebook
TODO: timeout of 1 week
-->

## Storage
Your home directory in the JupyerLab is provided by the Ceph storage on the Sparrow system.

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

## Access to the Hawk cluster
An ssh key is automatically generated for each user on first login. Instructions for how to add this key to your ssh authorized_keys file to allow you passwordless access to the Hawk cluster can be found in the following notebook:

https://github.com/nick-wilson/sparrow-examples/blob/master/ssh-copy-id.ipynb

## pysjef & Molpro

## Troubleshooting

### Resetting Anaconda environment to the version shipped in the container image
If you have broken the `persistent` environment in your user directory and would like to reset it back to the version shipped with the container image then please use the following procedure:
1. Open a terminal
2. Run the command `conda-resync`
3. Once the command is complete restart the JupyterLab server by navigating to https://chemy-hub.sparrow.cf.ac.uk/hub/home and clicking on "Stop My Server" and "Start My Server" (this page is also available by selecting "Hub Control Panel" from the "File" menu)

If a newer version of the container image has been published since you started your current JupterLab server and you would like to update the `persistent` environment in your user directory then you will need to restart the JupyterLab server, run the `conda-resync` command and then restart the Jupyter server again.

## Further documentation
https://docs.jupyter.org
