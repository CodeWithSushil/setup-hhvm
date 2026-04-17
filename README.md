## Setup HHVM/Hack
Install HHVM and running your Hack code.

### Usage Example

```yml
steps:
  - name: Checkout code
    uses: actions/checkout@v4

  - name: Setup Hack
    uses: your-username/setup-hacklang@v1
    with:
      hack-version: '4.153'

  - name: Typecheck
    run: hh_client
```
