## Python

These settings apply only when `--python` is specified on the command line.
Please also specify `--python-sdks-folder=<path to the root directory of your azure-sdk-for-python clone>`.
Use `--python-mode=update` if you already have a setup.py and just want to update the code itself.

```yaml
python-mode: create
package-version: 0.1.0
azure-arm: true
license-header: MICROSOFT_MIT_NO_VERSION
payload-flattening-threshold: 2
override-client-name: AVSClient
namespace: azure.mgmt.avs
package-name: azure-mgmt-avs
clear-output-folder: true
```
``` yaml $(python-mode) == 'update'
no-namespace-folders: true
output-folder: $(python-sdks-folder)/compute/azure-mgmt-avs/azure/mgmt/avs
```
``` yaml $(python-mode) == 'create'
basic-setup-py: true
output-folder: $(python-sdks-folder)/compute/azure-mgmt-avs
```
