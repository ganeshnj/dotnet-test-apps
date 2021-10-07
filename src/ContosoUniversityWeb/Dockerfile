FROM mcr.microsoft.com/dotnet/aspnet:5.0 AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

FROM mcr.microsoft.com/dotnet/sdk:5.0 AS build
WORKDIR /src
COPY ["src/ContosoUniversityWeb/ContosoUniversity.csproj", "src/ContosoUniversityWeb/"]
RUN dotnet restore "src/ContosoUniversityWeb/ContosoUniversity.csproj"
COPY . .
WORKDIR "/src/src/ContosoUniversityWeb"
RUN dotnet build "ContosoUniversity.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "ContosoUniversity.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "ContosoUniversity.dll"]