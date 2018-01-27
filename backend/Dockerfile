FROM microsoft/aspnetcore-build AS builder
WORKDIR /app

RUN git clone https://github.com/kajakdc/infotv-backend.git .

RUN dotnet restore
RUN dotnet publish -c Release -o out

FROM microsoft/aspnetcore
WORKDIR /app
COPY --from=builder /app/out  .
ENTRYPOINT ["dotnet", "infotv-backend.dll"]
