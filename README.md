# Datadog_GO

1. Installare go sul proprio pc
2. Creare una cartella dedicata al progetto
3. Eseguire questo comando
```
go get github.com/DataDog/datadog-api-client-go/api/v2/datadog
```

4. Creare il proprio codice go (esempio di file presente)
5. Export dei dati necessari alla connessione verso Datadog
```   
export DD_SITE="datadoghq.???" DD_API_KEY="xxxx" DD_APP_KEY="xxxx"
```

6. Lanciare il comando e vedere il result
```
go run main_alluser_list.go
```
