# STAGE 1: Build
FROM mcr.microsoft.com/dotnet/sdk:10.0 AS build
WORKDIR /src

COPY . .

RUN dotnet restore "SaaSBoilerplate.Api/SaaSBoilerplate.Api.csproj"

RUN dotnet publish "SaaSBoilerplate.Api/SaaSBoilerplate.Api.csproj" -c Release -o /app/publish

FROM mcr.microsoft.com/dotnet/aspnet:10.0 AS runtime
WORKDIR /app

COPY --from=build /app/publish .

EXPOSE 8080

ENTRYPOINT ["dotnet", "SaaSBoilerplate.Api.dll"]