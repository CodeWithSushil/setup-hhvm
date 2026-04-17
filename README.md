## Setup HHVM/Hack
Install HHVM and running your Hack code.

### Usage Example

```yml
steps:
  - name: Checkout code
    uses: actions/checkout@v4

  - name: setup-Hacklang
    uses: CodeWithSushil/setup-hhvm@v1.0.0
    with:
      hack-version: latest

  - name: Typecheck
    run: hh_client
```
