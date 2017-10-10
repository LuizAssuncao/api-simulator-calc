FROM microsoft/aspnetcore:2.0 AS build-env

COPY . /app
WORKDIR /app

EXPOSE 61201
# ENTRYPOINT ["dotnet", "run", "--project", "Easynvest.SimulatorCalc.Api", "--server.urls", "http://0.0.0.0:61201"]
CMD ASPNETCORE_URLS=http://*:$PORT dotnet Easynvest.SimulatorCalc.Api.dll

#ENTRYPOINT ["dotnet", "Easynvest.SimulatorCalc.Api.dll", "--server.urls", "http://0.0.0.0:61201"]