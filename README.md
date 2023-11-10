# Sprint-DevOps

O arquivo "EasyPlan" esta com o código fonte da API em java SpringBoot.


# Lista de Endpoints
## ***Empresas***
## GET 
https://api.example.com/api/empresas
### Descrição: Consulta a lista de empresas cadastradas.
### Exemplo de resposta:
          
       {
              "id": 19,
              "nome": "Silvio Hairs",
              "segmento": "Cabeleireiro",
              "endereco": "Av Imirim",
              "km": 4.0,
              "favorito": false
          }

## POST
https://api.example.com/api/empresas 
### Descrição: Cadastra uma nova empresa.
### Exemplo de solicitação:

      {
        "id": 21,
        "nome": "Transported Kolirio",
        "segmento": "Frete",
        "endereco": "AV Di Ines Silva",
        "km": 9.0,
        "favorito": false
      },


## PUT 
https://api.example.com/api/empresas/21
### Descrição: Atualiza informações sobre a empresa cadastrada.
### Exemplo de solicitação:

      {
        "id": 21,
        "nome": "Transported Kolirio",
        "segmento": "Frete",
        "endereco": "AV Di Ines Silva",
        "km": 9.0,
        "favorito": false
      },


## DELETE 
https://api.example.com/api/empresas/21
### Descrição: Deleta a empresa selecionada. No caso deletará a empresa com o id = 21.
## ***Usuarios***
## GET 
https://api.example.com/api/usuarios
### Descrição: Consulta a lista de usuarios cadastrados. 
### Exemplo de resposta:
          
             {
                  "id": 1,
                  "nome": "Renan Costa",
                  "telefone": "999999999",
                  "email": "renan@fiap.com.br",
                  "cpf": "123-456-789.00"
              }

## POST
https://api.example.com/api/usuarios
### Observação: Colocar id de um usuario ja cadastrad0!
### Descrição: Cadastra um novo usuario.
### Exemplo de solicitação:

           {
                "nome": "Renan Costa",
                "telefone": "999999999",
                "email": "renan@fiap.com.br",
                "cpf": "123-456-789.00"
          }


## PUT 
https://api.example.com/api/usuarios/1
### Descrição: Atualiza informações sobre o usuario cadastrado.
### Exemplo de solicitação:
      {
      "nome": "Renan Castilho",
      "telefone": "999999999",
      "email": "renan@fiap.com.br",
      "cpf": "123-456-789.00"
      }


## DELETE 
https://api.example.com/api/usuarios/1 
### Descrição: Deleta o usuario selecionado. No caso deletará o usuario com o id = 1.

## ***Agendamentos***
## GET 
https://api.example.com/api/agendamentos
### Descrição: Consulta a lista de agendamentos cadastrados. 
### Exemplo de resposta:
          
    {
        "id": 13,
        "empresa": {
            "id": 6,
            "nome": "Piratas",
            "segmento": "Barbeiro",
            "endereco": "Rua Dário Ribeiro",
            "km": 5.0,
            "favorito": false
        },
       "dataHora": "10-09-2023 16:00:00"
    },

## POST
https://api.example.com/api/agendamentos
### Observação: Colocar id de uma empresa ja cadastrada!
### Descrição: Cadastra um novo agendamento.
### Exemplo de solicitação:

    {
        "empresa":{ "id": 13
    },
        "dataHora": "10-09-2023 16:00:00"
    }


## PUT 
https://api.example.com/api/agendamentos/13
### Descrição: Atualiza informações sobre o agendamento cadastrado.
### Exemplo de solicitação:

    {
        "empresa":{ "id": 13
    },
        "dataHora": "20-10-2023 19:40:00"
    }


## DELETE 
https://api.example.com/api/agendamentos/13 
### Descrição: Deleta o agendamento selecionado. No caso deletará o agendamento com o id = 13.

