# CobraLab

A place to experiment with Cobra and Viper

## Why?

Cobra and Viper are powerful tools, with minimal documentation, as the primary author is crazy busy
being a Golang core contributor. Cobra's docs lag behind the code, for example, when I created this,
the examples on Cobra's generator page did not work.

I wanted a minimal environment in which I could explore what was actually happening under the hood
with Cobra, Viper, PFlag, Mapstructure, etc. A way to test hypotheses I would make about behavior
based on reading the code.

## What's with the fork?

CobraLab uses my fork of Cobra via a replace directive. The fork has a variety of pending PRs from 
the Cobra project merged. Once Cobra finishes the process of moving to a 1.0 release, if I'm still
using this, I'll retool it onto that release.

Until I make a release, the replace points to a local clone of the fork, as it was simpler.

## Examples

1. [Generator page](https://github.com/spf13/cobra/blob/master/cobra/README.md)

In branch [generator_page_example](https://github.com/hilary/cobraLab/tree/generator_page_example),
the example from the README for Cobra's generator.

With PRs [841](https://github.com/spf13/cobra/pull/841) and [842](https://github.com/spf13/cobra/pull/842)
merged, the example works: when you run `go run main.go --help` you get the help statement, when you
run `go run main.go config create` it prints `create called`, etc.

Without the PRs, running any of the commands returns the generic long description.
