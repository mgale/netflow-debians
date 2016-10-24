# netflow-debians

This contains the debian build directory for sources from http://tools.netsa.cert.org/

## Currently supports sources are

 - libfixbuff
 - yaf
 - silk

# How To

To build the debians you need to execute the playbooy build_debs with a few extra-vars:
 - progam_name <--- The name of the software you want to build the debian for
 - version     <--- The version you want to download
 - GPGKEY

 For example:
 ```ansible-playbook -i build_host_inventory.ini build_debs.yml --extra-vars "program_name=yaf GPGKEY=<YourKey>" --tags yaf```
