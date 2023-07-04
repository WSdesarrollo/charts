FROM mcr.microsoft.com/dotnet/aspnet:5.0 AS base

# Create a group and user
RUN groupadd -r backend && useradd -r -g backend -m backend

# Tell docker that all future commands should run as the nonroot user

WORKDIR /app
EXPOSE 5000

ARG ARTIFACTS_DIRECTORY

RUN mkdir -p /app/wwwroot/Plugins && chmod -R 777 /app/wwwroot/Plugins

USER backend

# Copy the build artifacts into the container
COPY $ARTIFACTS_DIRECTORY .

ENTRYPOINT ["dotnet", "Worldsys.Compliance.Web.Host.dll"]
