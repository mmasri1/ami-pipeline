# ami-pipeline

`ami-pipeline` helps you build secure Ubuntu AMIs fast. It automates the process of hardening, scanning, and signing images.

**What it does:**
* Creates Ubuntu images using [Packer](https://www.packer.io/)
* Applies OS hardening with Bash scripts
* Performs CIS benchmark checks to ensure compliance
* Keeps dependencies up to date automatically
* Runs security scans with:
  * [Trivy](https://github.com/aquasecurity/trivy)
  * [Lynis](https://github.com/CISOfy/lynis)
* Signs images using [cosign](https://github.com/sigstore/cosign)
* Publishes the AMI to AWS

**Prerequisites**

* [Packer](https://www.packer.io/) installed and available in your `$PATH`
* **AWS credentials configured** for Packer, either by:

  * Running `aws configure` to set up your access key, secret key, and region, **or**
  * Exporting credentials manually:

    ```bash
    export AWS_ACCESS_KEY_ID="access_key_id"
    export AWS_SECRET_ACCESS_KEY="secret_access_key"
    export AWS_DEFAULT_REGION="region"
    ```

**Setup**
1. Make sure scripts are executable:
```bash
chmod +x *.sh
```

2. Building an AMI

Run the main build script:
```bash
./build_ami.sh
```

This script will:
- [X] Build a base Ubuntu image using Packer
- [ ] Apply OS hardening and CIS benchmarks
- [ ] Update packages and dependencies
- [ ] Run security scans (Trivy, Lynis)
- [ ] Sign the resulting AMI

**Contributing:**
Contributions are welcome. Feel free to open issues or submit pull requests.