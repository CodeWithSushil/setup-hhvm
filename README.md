## Setup HHVM/Hack

Install HHVM and running your Hack code. Makesure `Ubuntu version 22.04` or `20.04` version supported only not support on `ubuntu-latest` (24.04) version.

---

### Usage Example

```yml

runs-on: ubuntu-22.04
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
