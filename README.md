# fabric-metadata
![ci](https://github.com/youyuanwu/fabric-metadata/actions/workflows/build.yaml/badge.svg)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://raw.githubusercontent.com/youyuanwu/fabric-metadata/main/LICENSE)

Metadata of service-fabric copied and selected from: [service-fabric](https://github.com/microsoft/service-fabric) 

# Depenencies
* service fabric runtime installation. See [get-started](https://learn.microsoft.com/en-us/azure/service-fabric/service-fabric-get-started)

# Contents
idl from https://github.com/microsoft/service-fabric/tree/master/src/prod/src/idl into [idl](./idl/) and [internal_idl](./internal_idl/)

cpp headers in this repo are generated from idls in [fabric](./src/fabric/) and [fabric_internal](./src/fabric_internal/)

Windows support libs are generated from dll binaries from service fabric runtime installation.

cmake targets `fabric_sdk` and `fabric_internal_sdk` can be used for accessing cpp headers.

# Example usage
See [fabric-rpc](https://github.com/youyuanwu/fabric-rpc) for example of how to use this project.

# License
idl files and generated cpp and c files have Microsoft MIT license.
The project has MIT license.