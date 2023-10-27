# Development

## Design Choice

#### Use subset of Papyrus-RT vs whole

Choice:  
Subset

Rational:  
The size of zipped Papyrus-RT 1.0.0 is over 300 MB! while subset of PapyrusRT which is enough to perform codegen is around 20 MB.
Using whole Papyrus-RT on GitHub workflow takes lots of resources such as storage, time and network load.
For example, if whole Papyrus-RT is included in this repository,
repository gets large(and GitHub rejects push).
And if whole Papyrus-RT is downloaded on every run of workflow,
download takes long time and traffic between the GitHub and the Eclipse Foundation.  
Therefore, use subset of Papyrus-RT to save resource.

#### Include Papyrus-RT in this repository vs download it on workflow

Choice:  
Include

Rational:  
To save time and traffic. And robustness against network trouble.


## Installation Area

#### Linux and macOS

```
/opt/papyrusrt -+--- 1.0.0/plugins/
                \--- (Other versions)/plugins/

```

#### Windows

```
${env:USERPROFILE}\tools\papyrusrt -+--- 1.0.0\plugins\
                                    \--- (Other versions)\plugins\

```
