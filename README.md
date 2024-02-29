# Helm Chart for Bright Sniffer

[Helm](https://helm.sh/) must be installed to use the charts. Please refer to Helm's [documentation](https://helm.sh/docs/) to get started.

## Clone the repository:

```shell
git clone git@github.com:NeuraLegion/sniffer-helm.git --depth 1
cd ./sniffer-helm
```

## Render the Helm templates:

```shell
helm template .
```

## Install the agent:

Use the Helm command to install the Sniffer agent:

```shell
helm install sniffer-agent . -f values.yaml
```

## Override default configurations (using values.yaml):

To customize configurations, modify the `values.yaml` file as follows:

```yaml
api:
  apiKey: '<your API key with entry-points:manage or entry-points:admin scopes>'
  apiURL: 'https://app.brightsec.com/'
  projectID: '<your Bright project ID>'

sniffer:
  image:
    pullPolicy: Always

  extraArgs:
    group-public-ips: true
    send-traffic-delta: true
    ebpf-dns-tracer-enabled: false
```

## Uninstall the agent:

To remove the Sniffer agent, use the following command:

```shell
helm uninstall sniffer-agent
```

## License

Copyright © 2024 [Bright Security](https://brightsec.com/).

This project is licensed under the MIT License - see the [LICENSE file](LICENSE) for details.
