APT Package pinning for openstack-ansible
=========================================

This role will set package pinning for APT packages. The role will create a
preference file used to pin packages to a *release*, *origin*, or *version*.
The pinning syntax is a simple data driven format which is a list of
dictionaries. The items must contain a *package* entry and pinning type.
Pinning types are *release*, *origin*, or *version*.


Basic Role Example
^^^^^^^^^^^^^^^^^^

.. code-block:: yaml

    - role: "{{ rolename }}"
      apt_package_pinning_file_name: test.pref
      apt_pinned_packages:
        - { package: "test-package-version", version: "9.9.9-version" }
        - { package: "test-package-origin", origin: "test-origin.org" }
        - { package: "test-package-release.*", release: "TestRelease", priority: 101 }
