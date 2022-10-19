# Setup terraformrc

This action will setup the terraform credential(`~/.terraformrc`) with the given token.

## Usage

```yaml
  steps
  - uses: StudistCorporation/actions-setup-tf-credentials@v1
    with:
      token: ${{ secrets.TF_API_TOKEN }}
```
