# https://hub.docker.com/_/microsoft-dotnet
FROM mcr.microsoft.com/dotnet/sdk:7.0.100 AS build
ARG CONFIG=release

WORKDIR /source

# copy csproj and restore as distinct layers
COPY *.csproj .
RUN dotnet restore

# copy everything else and build app
COPY . .
RUN dotnet publish -c $CONFIG -o /app

# final stage/image
FROM mcr.microsoft.com/dotnet/aspnet:6.0-alpine
ARG DEFAULT_ENVIRONMENT="Development"
ENV ASPNETCORE_ENVIRONMENT=$DEFAULT_ENVIRONMENT

WORKDIR /app
COPY --from=build /app ./
ENTRYPOINT ["dotnet", "minimal-webapi.dll"]