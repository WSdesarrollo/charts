FROM mcr.microsoft.com/dotnet/aspnet:5.0 AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

ARG ARTIFACTS_DIRECTORY

# Copia los artefactos de la construcción al contenedor
COPY $ARTIFACTS_DIRECTORY .

ENTRYPOINT ["dotnet", "Worldsys.Compliance.Web.Host.dll"]