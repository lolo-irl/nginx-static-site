# Static Site with Nginx + Docker

Site estático servido com **Nginx** e containerizado com **Docker** e **Docker Compose**.

---

## Sobre o projeto

Projeto de site estático containerizado utilizando uma imagem customizada do Nginx, construída a partir do Debian. O objetivo é servir arquivos HTML e CSS de forma simples, reproduzível e independente de ambiente.

---

## Estrutura do projeto

```
.
├── Dockerfile        # Imagem customizada com Nginx (repositório oficial nginx.org)
├── compose.yaml      # Orquestração do container
├── index.html        # Página principal
└── style.css         # Estilos do site
```

---

## Como executar

### Pré-requisitos

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Subindo o container

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio

# Build e execução
docker compose up --build
```

Acesse o site em: [http://localhost:8080](http://localhost:8080)

### Parando o container

```bash
docker compose down
```

---

## Detalhes da imagem

- **Base:** `debian:latest`
- **Nginx:** instalado via repositório oficial [nginx.org](https://nginx.org/en/linux_packages.html) com verificação de chave GPG
- **Diretório de conteúdo:** `/usr/share/nginx/html`
- **Porta exposta:** `80` (mapeada para `8080` no host)

---

## Configuração das portas

| Host | Container |
|------|-----------|
| 8080 | 80        |

---
