# CVP onboarding token generation with custom Ansible role

## Steps

1\. Create service account on CloudVision and add it into `./token_dir/svcacc.tok`

Service accounts can be created from the Settings page where a service token can be generated as seen below:

![serviceaccount1](./static/serviceaccount1.png)
![serviceaccount2](./static/serviceaccount2.png)
![serviceaccount3](./static/serviceaccount3.png)

2\. Update the `ansible_user` and `ansible_password` in [generate_onboarding_token.yaml](./generate_onboarding_token.yaml)

3\. Update the CloudVision IP/FQDN in [cv_server.yaml](./host_vars/cv_server.yaml)

5\. Update the [inventory.yaml](./inventory.yml) with your devices

6\. Run the playbook with `ansible-playbook generate_onboarding_token.yaml`
