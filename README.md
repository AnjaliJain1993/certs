# certs
Generating certificates for freeradius 2.x:

Using the link : https://www.ossramblings.com/using-freeradius-ubuntu-server-wifi

###Generate "dh" file

If "dh" file is not present in the freeradius/certs directory, then we need to generate it manually after creating client_android.p12 file:

  make dh
  
Set the proper permissions for dh file and create the link:

  chmod 640 dh
  chgrp ssl-cert dh
  ln -s /var/certs/freeradius/dh dh
  


