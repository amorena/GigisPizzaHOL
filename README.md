# GigisPizzaHOL
Hands on Lab - Gigis pizza microservices/serverless app

HOL 5967 [link](https://github.com/oraclespainpresales/GigisPizzaHOL/blob/master/hol5967_userguide.md "HOL5967")

## Interesting information for the demo:

OVA [link](https://objectstorage.eu-frankfurt-1.oraclecloud.com/p/5GHVwD_wVr3dvNhDKRq4V_o1n_Cx8hJo6vF2WM9HjNY/n/wedoinfra/b/DevCS_Clone_WedoDevops/o/HOL5967-OOW2019.ova "ova hol")

OCICLI upgrade to last version (OVA upgrade)
```
bash -c "$(curl -L https://raw.githubusercontent.com/oracle/oci-cli/master/scripts/install/install.sh)"
```

OCI SETUP repair permissions error
```
oci setup repair-file-permissions –file /home/holouser/.oci/private.pem
```

Create OCIR Secret.
```
kubectl create secret docker-registry ocirsecret --docker-server=<region>.ocir.io --docker-username='<tenant_storage_namespace>/<your_user>' --docker-password='<your_auth_token>' --docker-email='<your_email>'
```
Example
```
kubectl create secret docker-registry ocirsecret --docker-server=fra.ocir.io --docker-username='wedoinfra/wedo.devops' --docker-password='92(·38434"4Gjhle14%' --docker-email='test.email@oracle.com'
```

Oracle Cloud Regions:
https://docs.cloud.oracle.com/iaas/Content/General/Concepts/regions.htm

Oracle OCIR Regions:
https://docs.cloud.oracle.com/iaas/Content/Registry/Concepts/registryprerequisites.htm#Availab
