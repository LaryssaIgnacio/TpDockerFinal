# TP Final — Docker Compose

## Alunos
- Laryssa Flabio Ignacio
- Julliano Angelotti

## Objetivo
Criar um ambiente com dois containers Docker orquestrados com Docker Compose:
- **site**: site estático usando imagem customizada com nginx (porta 8080)
- **app**: servidor HTTP Apache (httpd) (porta 8081)

## Estrutura
```text
tp-docker/
├── docker-compose.yml
├── README.md
└── site/
    ├── Dockerfile
    └── index.html
```

## Como executar
```bash
docker build -t meu-site-nginx:1.0 ./site
docker compose up -d
```

Acessar no navegador:
- http://localhost:8080 → site estático (nginx)
- http://localhost:8081 → Apache (httpd)

## Comandos extras
```bash
docker compose ps
docker compose logs
docker compose exec site sh
```

## Finalizar
```bash
docker compose down
```
