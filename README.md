# ⚠️ Repository Deprecation Notice
This repository is deprecated and no longer actively maintained.
Status

 - ⛔ No further development
 - ⛔ No bug fixes
 - ⛔ No new features
 - ⛔ No pull requests will be reviewed or merged

 ------------------------------------------------------------------------

# Helm Chart for Bright Sniffer

[Helm](https://helm.sh/) must be installed to use the charts. Please refer to Helm's [documentation](https://helm.sh/docs/) to get started.

## Install the sniffer

Use the Helm command to install the Sniffer:

```shell
helm install sniffer oci://ghcr.io/neuralegion/sniffer -f values.yaml
```

## Override default configuration (using values.yaml)

To customize configurations, modify the `values.yaml` file as follows:

```yaml
api:
  apiKey: '<your API key with entry-points:manage or entry-points:admin scopes>'
  apiURL: 'https://app.brightsec.com/'
  projectID: '<your Bright project ID>'
```

## Uninstall the sniffer

If you want to delete the Sniffer from your Kubernetes cluster, use the following command:

```shell
helm delete sniffer
```

## License

Copyright © 2024 [Bright Security](https://brightsec.com/).

This project is licensed under the MIT License - see the [LICENSE file](LICENSE) for details.
