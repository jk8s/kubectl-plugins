# kubectl-plugins
A collection of plugins for kubectl (for Kubectl versions >= 1.12.0)

###### Note
- These plugins are for kubectl versions at or above 1.12.0 only. Check your version via ```kubectl version```
- EKS plugin requires AWS CLI to be installed with AWS credentials configured ([AWS CLI docs](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html))

## Install on Linux/Mac
```bash
git clone https://github.com/jk8s/kubectl-plugins.git
cd kubectl-plugins
./install-plugins.sh
source ~/.bash_profile
```

### kubectl eks config
- This is useful for accessing EKS private cluster endpoint. It will pull cluster endpoint private IPs and configure your /etc/hosts so that you can resolve the EKS private cluster domain from your local workstation.
```bash
kubectl eks config <eks-cluster-name> <aws-profile (default: "default")>
```
