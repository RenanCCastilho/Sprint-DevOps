# Find It API — Entrega Sprint (DevOps)

![Java](https://img.shields.io/badge/Java-17-ED8B00?logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.1-6DB33F?logo=springboot&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?logo=microsoftazure&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle_DB-F80000?logo=oracle&logoColor=white)

Esta é a entrega da sprint de **DevOps Tools & Cloud Computing** do projeto **Find It**. Ela traz a API, o script do banco e a configuração do pipeline de CI/CD para a nuvem.

> Para a descrição completa do produto, veja **[FindIt-API](https://github.com/RenanCCastilho/FindIt-API)**.

## Conteúdo do repositório

| Arquivo | Descrição |
|---|---|
| `src/` | Código da API (Spring Boot) |
| [`DDL.txt`](DDL.txt) | Script de criação das tabelas no Oracle |
| [`YAML.txt`](YAML.txt) | Definição do pipeline de CI/CD |
| [`Config_ci_cd.pdf`](Config_ci_cd.pdf) | Passo a passo da configuração do CI/CD |
| [`EasyPlan.pdf`](EasyPlan.pdf) | Documentação do projeto |

## Endpoints

| Recurso | Rota base | Operações |
|---|---|---|
| Empresas | `/api/empresas` | `GET`, `POST`, `PUT /{id}`, `DELETE /{id}` |
| Usuários | `/api/usuarios` | `GET`, `POST`, `PUT /{id}`, `DELETE /{id}` |
| Agendamentos | `/api/agendamentos` | `GET`, `POST`, `PUT /{id}`, `DELETE /{id}` |

**Exemplo — cadastrar empresa**

```json
POST /api/empresas
{
  "nome": "Silvio Hairs",
  "segmento": "Cabeleireiro",
  "endereco": "Av. Imirim",
  "km": 4.0,
  "favorito": false
}
```

**Exemplo — criar agendamento** (use o id de uma empresa já cadastrada)

```json
POST /api/agendamentos
{
  "empresa": { "id": 6 },
  "dataHora": "10-09-2023 16:00:00"
}
```

## Como executar

1. Crie as tabelas executando o [`DDL.txt`](DDL.txt) no seu banco Oracle.
2. Rode a aplicação:

```bash
export DB_USERNAME=seu_usuario DB_PASSWORD=sua_senha
./mvnw spring-boot:run
```

---

Projeto acadêmico desenvolvido na **FIAP** (2023).
