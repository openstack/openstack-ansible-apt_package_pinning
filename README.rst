=========================================
APT Package pinning for OpenStack-Ansible
=========================================

This role will set package pinning for APT packages. The role will create a
preference file used to pin packages to a *release*, *origin*, or *version*.
The pinning syntax is a simple data driven format which is a list of
dictionaries. The items must contain a *package* entry and pinning type.
Pinning types are *release*, *origin*, or *version*.
