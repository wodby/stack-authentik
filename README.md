# authentik application stack for Kubernetes on Wodby

Deploy authentik applications on Kubernetes with Wodby.

This repository defines the Wodby stack manifests and default service
composition for authentik.

<!-- wodby:generated:start -->

## Stack contract

- [authentik stack on Wodby](https://wodby.com/stacks/authentik)
- [Browse Wodby application stacks](https://wodby.com/stacks)
- [authentik stack guide](https://wodby.com/docs/2.0/stacks/catalog/authentik/)
- [Wodby stack documentation](https://wodby.com/docs/2.0/stacks/)
- [Stack manifest reference](https://wodby.com/docs/2.0/stacks/template/)

## Service definitions

- [authentik service](https://github.com/wodby/service-authentik)
- [PostgreSQL service](https://github.com/wodby/service-postgres)
- [Ganesha NFS provisioner service](https://github.com/wodby/service-nfs-provisioner)
- [OpenSMTPD service](https://github.com/wodby/service-opensmtpd)

## What's included

| Component / service | Default configuration |
| --- | --- |
| authentik<br>`authentik` | required; enabled by default; volumes: `data` 5 GB; links: `postgres` → `postgres`, `storage` → `storage`, `sendmail` → `opensmtpd` |
| PostgreSQL<br>`postgres` | required; enabled by default; volumes: `data` 10 GB |
| Shared file storage<br>`storage` | required; enabled by default; volumes: `data` 10 GB |
| OpenSMTPD<br>`opensmtpd` | optional; disabled by default |

Enabled optional services are selected by default but can be excluded when an
app is created. Disabled optional services are available but not selected by
default. Required services cannot be excluded.

## Validate the stack manifest

```bash
wodby stack validate-manifest stack.yml --org <org-id>
```

<!-- wodby:generated:end -->
