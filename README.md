# Setup Papyrus-RT

A GitHub Action which sets up your workflow with specified version of the Papyrus-RT standalone code generator.

Intended user
* The person who wants to build C/C++ project with the Papyrus-RT on the GitHub Actions workflow.

If you are interested in modeling with the Papyrus-RT application, this repository does not suit for your usage.
Because this repository contains subset of Papyrus-RT which is possible to perform codegen only.


## Usage

#### Basic

```yaml
steps:
  - uses: Bacondish2023/setup-papyrusrt@v1
    with:
      papyrusrt-version: 1.0.0
```

Inputs

|Item|Description|Mandatory?|Default|
|:---|:---|:---|:---|
|papyrusrt-version|The version of Papyrus-RT.<br>One of {1.0.0}.|No|The latest(1.0.0)|
|is-setup-envvars|The switch of environment variables definition.<br>If true, the `PAPYRUSRT_ROOT` and `UMLRTS_ROOT` will be defined with corresponding values.|No|True|

Outputs

|Item|Description|
|:---|:---|
|papyrusrt-root|The absolute path of the Papyrus-RT. Without trailing slash.|
|umlrts-root|The absolute path of the Runtime Service Library. Without trailing slash.|


#### Misc

A build tool [Bacondish2023/model_compiler_for_papyrusrt](https://github.com/Bacondish2023/model_compiler_for_papyrusrt)
and its example project are used in test workflow of this repository.
Details are in **setup-papyrusrt/.github/workflows/smoke_test.yml** .


## Prerequisites

#### Supported Platform

* Linux
* Windows


## License

This project is free and open-source software licensed under the **Eclipse Public License 1.0**
except for contents in **papyrusrt** directory.  
The **papyrusrt** directory contains copies of other works.
Details are on [Packages](papyrusrt/packages.md) .
