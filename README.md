![image](https://user-images.githubusercontent.com/51267656/146583554-2f06208a-ad2a-41df-80da-d06bfb38c3e3.png)
# Datadog and GO - simple use List all User

## Utilizzo su instanza linux :

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

## Utilizzo con docker container
1. Creiamo una cartella di lavoro
2. Eseguire il comando per creare il file go.mod
```
go mod init <nomecartella>
```

3. Eseguire comando per installazione go-client-datadog
```
go get github.com/DataDog/datadog-api-client-go/api/v2/datadog
```
N.B. noteremo che nel file go.mod è stato aggiunto un require

4. Creaiamo il nostro Dockerfile (presente nella cartella dedicata)
5. Facciamo build dell'immagine
```
docker build . -t go-dd-docker
```
6. Eseguiamo il nostro container
```
docker run go-dd-docker
```
