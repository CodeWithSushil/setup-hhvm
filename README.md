## Setup HHVM / Hack Environment 

This setup installs HHVM and enables execution of Hack language code in a controlled environment.
> **Compatibility Notice** <br>
> HHVM currently supports only specific Ubuntu LTS versions. Ensure your environment uses one of the following:

* Ubuntu 22.04 (Jammy)
* Ubuntu 20.04 (Focal)

The ubuntu-latest runner (currently 24.04) is **not supported** and will lead to installation or runtime issues.

### Recommended Approach

For consistency and reliability—especially in CI/CD pipelines—use a **Docker container** based on Ubuntu 20.04. This guarantees compatibility with HHVM and avoids dependency conflicts introduced in newer distributions. <br>
**It is recommended to create a Docker image using Ubuntu 20.04 as the base for running HHVM/Hack.**

### Key Points

* Avoid using ubuntu-latest in GitHub Actions for HHVM workflows.
* Prefer explicit OS versioning (ubuntu-22.04 or ubuntu-20.04).
* Use Docker when portability and reproducibility are required.

---

### Usage Example

```yml

runs-on: ubuntu-latest
container:
  image: ubuntu:20.04

steps:
  - name: Checkout code
    uses: actions/checkout@v5

  - name: setup-Hacklang
    uses: CodeWithSushil/setup-hhvm@v1.0.0
    with:
      hack-version: latest

  - name: Typecheck
    run: hh_client
```

---
