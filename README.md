# ansible-tower-samples
Ansible Tower Playbook Samples
1. create one hosts file and add some context as:

127.0.0.1 asible_user=root ansible_password="1qaz@WSX" csv_file="hostname_or_id_from_cmdb"

2. use playbooks for test
#csv file name from inventory 
ansible-playbook -i hosts  hello_csv.yml -e "csv_path='/tmp/job123'" -vv
#csv file name from args
ansible-playbook -i hosts  hello_csv.yml -e "csv_path='/tmp/job123'" -e "csv_file=cmdb_host_name_as_args" -vv
