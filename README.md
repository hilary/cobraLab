# CobraLab

A place to experiment with Cobra and Viper

## Why?

Cobra and Viper are powerful tools, with minimal documentation, as the primary author is crazy busy
being a Golang core contributor. Cobra's docs lag behind the code, for example, when I created this,
the examples on Cobra's generator page did not work as given (you have to run `go mod init [module]`
where `[module]` is the same as what you gave as `--pkg-name` in `cobra init`).

I wanted a minimal environment in which I could explore what was actually happening under the hood
with Cobra, Viper, PFlag, Mapstructure, etc. A way to test hypotheses I would make about behavior
based on reading the code.

## Examples

1. [Multilevel modern](https://github.com/hilary/cobraLab/tree/multilevel_modern)

    Multilevel commands, but uses the community pattern for CLIs, with `cmd/cobraLab/main.go`.

1. [Multilevel command](https://github.com/hilary/cobraLab/tree/multilevel_command)

   Has multilevel commands:
    
````
cobraLab k8s cluster
cobraLab k8s options
````

   where `cobraLab k8s` is not Runnable. Cobra shows help in all the various ways (`--help`, 
   `help k8s`, and `cobraLab k8s`) despite the [open issue to the contrary](https://github.com/spf13/cobra/issues/790).

1. [Generator page](https://github.com/spf13/cobra/blob/master/cobra/README.md)

    [generator_page_example](https://github.com/hilary/cobraLab/tree/generator_page_example) has
    the example from the README for Cobra's generator. Works fine once you run `go mod init [module]`
    as discussed above.

