# Setting up from scratch

If you are rebuilding the cluster from scratch and can't pull from the auto secrets in Vault or CoreVault you can manually create the CloudFlare token 


Create a new CloudFlare API Token with READ/WRITE access to all DNS zones under CoRE.

```bash
kubectl create secret generic -n kube-system kjdev-cloudflare --from-literal=cloudflare_api_token=TOKEN_HERE
```
