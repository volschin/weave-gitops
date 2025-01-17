## gitops create

Creates a resource

### Examples

```

# Create a HelmRepository and HelmRelease to deploy Weave GitOps
gitops create dashboard ww-gitops \
  --password=$PASSWORD \
  --export > ./clusters/my-cluster/weave-gitops-dashboard.yaml

# Create a Terraform object
gitops create terraform my-resource \
  -n my-namespace \
  --source GitRepository/my-project \
  --path ./terraform \
  --interval 1m \
  --export > ./clusters/my-cluster/infra/terraform-my-resource.yaml

```

### Options

```
      --export             Export in YAML format to stdout.
  -h, --help               help for create
      --timeout duration   The timeout for operations during resource creation. (default 3m0s)
```

### Options inherited from parent commands

```
  -e, --endpoint WEAVE_GITOPS_ENTERPRISE_API_URL   The Weave GitOps Enterprise HTTP API endpoint can be set with WEAVE_GITOPS_ENTERPRISE_API_URL environment variable
      --insecure-skip-tls-verify                   If true, the server's certificate will not be checked for validity. This will make your HTTPS connections insecure
      --kubeconfig string                          Paths to a kubeconfig. Only required if out-of-cluster.
  -n, --namespace string                           The namespace scope for this operation (default "flux-system")
  -p, --password WEAVE_GITOPS_PASSWORD             The Weave GitOps Enterprise password for authentication can be set with WEAVE_GITOPS_PASSWORD environment variable
  -u, --username WEAVE_GITOPS_USERNAME             The Weave GitOps Enterprise username for authentication can be set with WEAVE_GITOPS_USERNAME environment variable
```

### SEE ALSO

* [gitops](gitops.md)	 - Weave GitOps
* [gitops create dashboard](gitops_create_dashboard.md)	 - Create a HelmRepository and HelmRelease to deploy Weave GitOps
* [gitops create terraform](gitops_create_terraform.md)	 - Create a Terraform object

###### Auto generated by spf13/cobra on 21-Jun-2023
