# DOTNET 6 Microservice Examples 

[![CI](https://github.com/pbronneberg/dotnet6-microservice/actions/workflows/CI.yml/badge.svg)](https://github.com/pbronneberg/dotnet6-microservice/actions/workflows/CI.yml)

Repository to check new .Net 6 functionality.

## Prerequisites

- Install [.Net 6 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
- -OR- use [docker](https://hub.docker.com/_/microsoft-dotnet-aspnet)
- [Visual Studio Code](https://code.visualstudio.com/)

## Notes

Support on AWS for .Net 6 is documented by Amazon in [GitHub](https://github.com/aws-samples/aws-net-guides/tree/master/RuntimeSupport/dotnet6).
As can be seen from the [AWS Developer documentation](https://aws.amazon.com/blogs/developer/net-6-on-aws/) .Net 6 is a first-class citizen on AWS. 

## Minimal API

API style competing with 'Python FAST API'

- Scaffolding: `dotnet new webapi -minimal -o minimal`
- Location: [./minimal](minimal)
- Background info: [MSDN Tutorial](https://docs.microsoft.com/en-us/aspnet/core/tutorials/min-web-api?view=aspnetcore-6.0&tabs=visual-studio)
- Docker Image size: 104MB (alpine)

### Building

Building & running on a local machine with SDK installed:
```BASH
dotnet restore minimal
dotnet run minimal
```

Building & running using docker
```BASH
docker run -p:8000:80 minimal
```