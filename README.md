# FitVictory

## Sobre o projeto  

O FitVictory é um aplicativo de saúde e bem-estar que ajuda os usuários a alcançar seus objetivos por meio de uma combinação de informações claras e personalizadas, uma comunidade vibrante e desafios estimulantes.  
O aplicativo oferece um chatbot especializado que responde a perguntas sobre saúde, fornece orientações personalizadas e informações atualizadas. Também oferece desafios diários e checklists que ajudam os usuários a desenvolver hábitos saudáveis e alcançar suas metas.  
Os desafios são projetados para serem alcançáveis, mas desafiadores, proporcionando uma sensação de conquista ao serem concluídos. As listas de verificação são adaptáveis, levando em consideração as preferências e metas individuais dos usuários.  
A pontuação de bem-estar do usuário aumenta à medida que os desafios são concluídos. Essa pontuação reflete não apenas as realizações, mas também o equilíbrio entre os diferentes aspectos do bem-estar.  
O FitVictory é uma ferramenta poderosa que pode ajudar os usuários a alcançar seus objetivos de saúde e bem-estar. É um guia completo que oferece informações, comunidade e desafios para tornar a jornada para uma vida saudável mais envolvente e sustentável.  

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
