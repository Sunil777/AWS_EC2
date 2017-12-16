# AWS_INSTANCE_STOP
Ansible playbook to stop instance before De-Register from ELB

## jenkins Execute shell like As:-
`cd ${WORKSPACE}
echo ${WORKSPACE}
mkdir -p group_vars
cat > group_vars/all.yml <<EOF
instance_ids: [${INSTANCE_IDS}]
EOF
ansible-playbook deattach.yml --extra-var="region=${region} elb_name=${elb_name} aws_access_key=${aws_access} aws_secret_key=${aws_secret} pause_time=${pause_time} " `
