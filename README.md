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

**Contributing:**
Contributions are welcome. Feel free to open issues or submit pull requests.
