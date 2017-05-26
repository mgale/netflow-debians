# netflow-debians

This contains the debian build directory for sources from http://tools.netsa.cert.org/

## Currently supported sources are

 - libfixbuff
 - yaf
 - silk

# How To

To build the debians you need to execute the playbooy build_debs, there are a few extra-vars that can be specified:
 - GPGKEY
 - build_items <--- Dictionary containing the program and version

 For example:
 ```ansible-playbook build_debs.yml --ask-sudo-pass --extra-vars "GPGKEY=<YourKey>"```
 ```ansible-playbook build_debs.yml --ask-sudo-pass --extra-vars "--extra-vars '{"build_items":{"test":"123"}}'```
