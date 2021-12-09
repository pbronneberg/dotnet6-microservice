# DOTNET 6 Microservice Examples 

Repository to check new .Net 6 functionality.

## Prerequisites

- Install [.Net 6 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
- -OR- use [docker](https://hub.docker.com/_/microsoft-dotnet-aspnet)
- [Visual Studio Code](https://code.visualstudio.com/)

## Minimal API

API style competing with 'Python FAST API'

- Scaffolding: `dotnet new webapi -minimal -o minimal`
- Location: [./minimal](minimal)
- Background info: [MSDN Tutorial](https://docs.microsoft.com/en-us/aspnet/core/tutorials/min-web-api?view=aspnetcore-6.0&tabs=visual-studio)

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


