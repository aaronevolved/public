Ansible AWX Install Playbook
----------------------------

Mostly based on Calvin Remsburg's video
https://www.youtube.com/watch?v=Nvjo2A2cBxI

Tested on:
- Alma Linux 9.0

Created:  January 25, 2024
Created by Aaron 

Description:
This playbook installs Kubernetes and AWX on an existing linux server.  

Notes:
I found that I got a lot of errors when I added the "- awx-cr.yaml" file to the kustomaization.yaml file, and would only install the AWX operator.
I then modded the playbook to install the AWX Operator, then modify the kustomatization.yaml file to include the - awx-cr.yaml file.
I was getting CrashLoopBackOff errors on the AWX-WEB pod, which was resolved by disabling the firewall.