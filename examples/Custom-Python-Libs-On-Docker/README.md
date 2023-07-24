# installing custom dependencies on custom docker image

This example shows how to create a new custom imagemn based on the original semaphore image in order to install custom dependencies
Those dependencies can be python libs or specific OS packages necessary to run some ansible modules.

the rationale here is:
- Create a new dockerfile 
- within this dockerfile:
  - copy the requirements file to the new image
  - Optinally, configure Sudoers file to allow  passwordless priviledge elevation
  - Install pithon deps via pip

this example includes python libraries used to interact with windows hosts and vmware hypervisor.

