# celsiusnarhwal/inputs-to-env

JavaScript and Docker container actions automatically recieve the `inputs` context as a series of environment variables
beginning with `INPUT_`, but composite actions do not. This action aims to close that gap somewhat.

## Usage

```yaml
- uses: celsiusnarhwal/inputs-to-env@v1
  env:
    INPUTS: ${{ toJson(inputs) }}
```

All subsequent steps of your action or workflow will be able to access the inputs context as environment variables
just as JavaScript and Docker container acctions can.