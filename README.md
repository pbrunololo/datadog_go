# Datadog_GO

1. Installare go sul proprio pc
2. Creare una cartella dedicata al progetto
3. Eseguire questo comando
```
go get github.com/DataDog/datadog-api-client-go/api/v2/datadog
```

4. Export dei dati
```   
export DD_SITE="datadoghq.???" DD_API_KEY="xxxx" DD_APP_KEY="xxxx"
```

5. Lanciare il comando
```
go run main_alluser_list.go
```
