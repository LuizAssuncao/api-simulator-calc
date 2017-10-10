# cd Easynvest.SimulatorCalc.Api
# dotnet publish -c Release
# docker build -t api-simulator-calc-publish ./bin/Release/netcoreapp2.0/publish/
# docker run -it --rm -p 61201:61201 --name simulator-publish api-simulator-calc-publish
# docker tag api-simulator-calc-publish registry.heroku.com/api-simulator-calc/web
# docker push registry.heroku.com/api-simulator-calc/web

FROM microsoft/aspnetcore:2.0 AS build-env

COPY . /app
WORKDIR /app

EXPOSE 61201
# ENTRYPOINT ["dotnet", "run", "--project", "Easynvest.SimulatorCalc.Api", "--server.urls", "http://0.0.0.0:61201"]
CMD ASPNETCORE_URLS=http://*:$PORT dotnet Easynvest.SimulatorCalc.Api.dll

#ENTRYPOINT ["dotnet", "Easynvest.SimulatorCalc.Api.dll", "--server.urls", "http://0.0.0.0:61201"]