# superblucandy

Restoring of word-press blog on a new Red Hat 7 Enterprise Server:


cat <<EOF >> restore.sh 
#!/bin/bash
yum update -y && \
yum install wget unzip -y && \
wget https://github.com/marbew/superbluecandy/archive/master.zip && \
unzip master.zip && \
cd superbluecandy-master/
chmod 700 redhat7_Lamp_restore 
./redhat7_Lamp_restore
EOF
chmod 700 restore.sh && ./restore.sh
