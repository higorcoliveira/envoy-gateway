## To create certificates

- Create the certificates
```
dotnet dev-certs https -ep ~/.dotnet/corefx/cryptography/x509stores/my/CoffeeAPI.pfx -p 123456
dotnet dev-certs https -ep ~/.dotnet/corefx/cryptography/x509stores/my/TeaAPI.pfx -p 123456
```

- Inside each API, run:

```
dotnet user-secrets set "Kestrel:Certificates:Development:Password" "123456"
```

## To start

```
docker-compose up -d
```