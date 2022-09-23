FROM mcr.microsoft.com/dotnet/aspnet:6.0 AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build
WORKDIR /src

COPY ["WebApp/WebApp.csproj", "WebApp/"]
RUN dotnet restore "WebApp/WebApp.csproj"
COPY . .
WORKDIR /src/WebApp
RUN dotnet build -c Release -o /app/build

WORKDIR ../
RUN echo $(ls -1)
RUN dotnet test TestWebApp.sln -v q
  #-r . --logger "trx;logfilename=testResults.trx"
#RUN echo $(ls -1)
#RUN echo $(cat testResults.trx)

FROM build AS publish
RUN dotnet publish "WebApp.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "WebApp.dll"]
