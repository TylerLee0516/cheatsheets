```
sudo /usr/sbin/kadmin.local -q 'listprincs'
sudo /usr/sbin/kadmin.local -q "addprinc -randkey $principal@$realm"
sudo /usr/sbin/kadmin.local -q "ktadd -k $keytab_path $principal@$realm"
kadmin -p "principal" -q "<command>"
sudo /usr/sbin/kadmin.local -q 'get_principal $principal'

sudo /usr/sbin/kdb5_util dump /var/kerberos/krb5kdc/slave_datatrans
sudo /usr/sbin/kprop -f /var/kerberos/krb5kdc/slave_datatrans $kdc

sudo /usr/sbin/kdb5_util dump ~/bk_"`date +%Y%m%d`"/kadmin_data
sudo /usr/sbin/kdb5_util load ~/bk_"`date +%Y%m%d`"/kadmin_data

sudo kadmin -r "realm" -p "chef/admin" -kt "/home/kli/chef.headless.keytab" -q "listprincs"
sudo kadmin -r "realm" -p "chef/admin" -w "password" -q "listprincs"
```
