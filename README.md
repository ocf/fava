Host [Fava](), a web interface for the text-file accounting program [beancount](), on Kubernetes.

There are two sidecar containers: one is Keycloak, since Fava by design does not do authentication.

The other is git-sync, which pulls from the ocf/beancount git repository, the single source of truth.
The live web interface is meant to be read-only, so edits to our beancount ledgers should be done locally and pushed to ocf/beancount.
