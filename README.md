## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

`helm repo add firzam https://firzam.github.io/helm-chart/`

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
` to see the charts.

To install the  chart:

    helm install deno-webserver firzam/deno-webserver

To uninstall the chart:

    helm delete deno-webserver

## Changelog

deno-webserver:
- 0.3.0
  - Use release variable to create deploy
  - Change deno-webserver image to `codebuds/deno-webserver:1.5.1`
  - Know issue:
    - mariadb container might failed to create (Will be fixed in next release)
- 0.2.0
  - Add GitHub action to create release
  - Add GitPage
  - Change MariaDB to StatefulSet
- 0.1.0
  - Create helm chart
  - Create deno-webserver
  - Create mariadb