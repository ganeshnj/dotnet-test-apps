FROM mcr.microsoft.com/dotnet/core/aspnet:3.1-buster-slim AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

FROM mcr.microsoft.com/dotnet/core/sdk:3.1-buster AS build
WORKDIR /src
COPY ["src/WeatherReactSpa/WeatherReactSpa.csproj", "src/WeatherReactSpa/"]
COPY ["src/BlazorWasm/BlazorWasm.csproj", "src/BlazorWasm/"]
COPY ["src/MvcWebApplication/MvcWebApplication.csproj", "src/MvcWebApplication/"]
RUN dotnet restore "src/MvcWebApplication/MvcWebApplication.csproj"
COPY . .
WORKDIR "/src/src/MvcWebApplication"
RUN dotnet build "MvcWebApplication.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "MvcWebApplication.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "MvcWebApplication.dll"]