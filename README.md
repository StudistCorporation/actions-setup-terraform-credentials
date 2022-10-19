# Setup terraformrc

This action will setup the terraform credential(`~/.terraformrc`) with the given token.

## Usage

```yaml
    steps
    # Install terraform cli via aqua
    - uses: aquaproj/aqua-installer@v1.1.2
      with:
        aqua_version: v1.20.2 # renovate depName=aquaproj/aqua
    - run: aqua i

    # Setup ~/.terraformrc
    - uses: StudistCorporation/actions-setup-tf-credentials@v1
      with:
        token: ${{ secrets.TF_API_TOKEN }}

    - run: terraform init
    - run: terraform plan
```

## Inputs

### token

The token to used for authenticating with Terraform Cloud.

### hostname

The hostname to use in the credential file. 
Default is `app.terraform.io`.
