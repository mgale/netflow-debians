# netflow-debians

This contains the debian build directory for sources from http://tools.netsa.cert.org/

## Currently supported sources are

 - libfixbuff
 - yaf
 - silk

 The versions are stored in vars/main.yml

# How To

To build the debians you need to execute the playbooy build_debs, there are a few extra-vars that need to be specified:
 - GPGKEY
 - program_name

 For example:
 ```ansible-playbook build_debs.yml --ask-sudo-pass --extra-vars "GPGKEY=<YourKey>"```
 ```ansible-playbook build_debs.yml --ask-sudo-pass --extra-vars "--extra-vars program_name=libfixbuf"```
 ```ansible-playbook build_debs.yml --extra-vars "GPGKEY=<YourKey> program_name=silk" --ask-sudo-pass```
