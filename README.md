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

## What's with the fork?

Some branches of CobraLab use my fork of Cobra via a replace
directive. The fork has a variety of pending PRs from the Cobra
project merged.

The replace directive points to a local clone of the fork, as it was
simpler.

## Examples

1. [Generator page](https://github.com/spf13/cobra/blob/master/cobra/README.md)

    In branch
    [generator_page_example](https://github.com/hilary/cobraLab/tree/generator_page_example),
    the example from the README for Cobra's generator.

