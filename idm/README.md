# IdM

A simple inventory to deploy [IdM](https://access.redhat.com/products/identity-management/). 

## Usage

### Running in OpenShift

[OpenShift Applier](https://github.com/redhat-cop/openshift-applier)

Run the following to pull in applier:

```
ansible-galaxy install -r requirements.yml -p galaxy -f
```

Now, deploy to your openshift cluster:

```
oc login <dev cluster>
ansible-playbook -i .applier/ galaxy/openshift-applier/playbooks/openshift-cluster-seed.yml
```

### Runtime Environment Variables

- `IDM_HOSTNAME`: the hostname for the IdM route.
- `IDM_INSTALL_OPTS`: The install options for IdM.
- `IDM_ADMIN_PASSWORD`: The password you want to set for your admin user for IdM.
- `IDM_SERVICE`: The name for the IdM service.
