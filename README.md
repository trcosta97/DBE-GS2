# FitVictory API

## Endpoints
Login com permissões de ADMIN:  
```console
{
  "email": "admin@fitvictory.com",
  "senha": "fVic0"
}
```

### Swagger
https://dbe-gs2-production.up.railway.app/swagger-ui/index.html  

### Register
POST  
https://dbe-gs2-production.up.railway.app/auth/register   
```console
{
  "nome": "string",
  "email": "string",
  "senha": "string",
  "cpf": "string",
  "role": "USER",
  "enderecoUsuario": {
    "numero": "string",
    "rua": "string",
    "cidade": "string",
    "estado": "string",
    "pais": "string",
    "cep": "stringst"
  }
}
```

### Login
POST  
https://dbe-gs2-production.up.railway.app/auth/login     
```console
{
  "email": "string",
  "senha": "string"
}
```

### Update User
PUT  
https://dbe-gs2-production.up.railway.app/user/<IdUsuario>    
```console
{
  "nome": "string",
  "senha": "string",
  "email": "string"
}
```

### Get User
GET  
https://dbe-gs2-production.up.railway.app/user/<IdUsuario>  
Requisição sem corpo. Retorna usuário especificado pelo ID na url.  

### Get Users
GET  
https://dbe-gs2-production.up.railway.app/user?page=0&size=10    
Requisição sem corpo. Retorna lista de usuários paginados com 10 por página, ordenados por ID (ordem de cadastro).

### Check In
PUT  
https://dbe-gs2-production.up.railway.app/user/checkIn/<IdUsuario>    
```console
  {
  "tipo": "ACADEMIA",
  "descricao": "string",
  "pontos": 0,
  "enderecoAtividade": {
    "numero": "string",
    "rua": "string",
    "cidade": "string",
    "estado": "string",
    "pais": "string",
    "cep": "string"
  }
}
```

### Get Atividades por User
GET  
https://dbe-gs2-production.up.railway.app/user/atividades/<IdUsuario>?page=0&size=10    
Requisição sem corpo. Inserir o ID do usuário no local indicado no link. Retorna lista de atividades por usuário. Requisição paginada com 10 por página, ordenados por ID (ordem de cadastro).
