# fabric-metadata
![ci](https://github.com/youyuanwu/fabric-metadata/actions/workflows/build.yaml/badge.svg)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://raw.githubusercontent.com/youyuanwu/fabric-metadata/main/LICENSE)

Metadata of service-fabric copied and selected from: [service-fabric](https://github.com/microsoft/service-fabric) 

# Depenencies
* service fabric runtime installation. See [get-started](https://learn.microsoft.com/en-us/azure/service-fabric/service-fabric-get-started)

# Code Generation Dependencies
The use of this repo as a dependency does not require these dependencies.
* Midl for c/cpp header generation
* dotnet `winget install Microsoft.DotNet.SDK.6` and `winget install Microsoft.DotNet.Runtime.6`
* ClangSharpPInvokeGenerator `dotnet tool install --global ClangSharpPInvokeGenerator --version 16.0.0`

# Contents
idl from https://github.com/microsoft/service-fabric/tree/master/src/prod/src/idl into [idl](./idl/) and [internal_idl](./internal_idl/)

cpp headers in this repo are generated from idls in [fabric](./src/fabric/) and [fabric_internal](./src/fabric_internal/)

Windows support libs are generated from dll binaries from service fabric runtime installation.

cmake targets `fabric_sdk` and `fabric_internal_sdk` can be used for accessing cpp headers.

winmd for service-fabric that is used to generate csharp or rust code in [.windows](./.windows) folder.

# Example usage
See [fabric-rpc](https://github.com/youyuanwu/fabric-rpc) for example of how to use this project.

# Rust
Exposes fabric support libs to rust lang through build.rs.
winmd is used by windows rust tool chain to generate rust bindings. See [service-fabric-rs](https://github.com/youyuanwu/service-fabric-rs) for details.

# License
idl files and generated cpp and c files have Microsoft MIT license.
The project has MIT license.