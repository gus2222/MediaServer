# 🗄️ Servidor MediaServer (Configurações YAML)

## ⚠️ AVISO IMPORTANTE: ARQUITETURA ARM
As imagens de container referenciadas nestes arquivos YAML (ex: `jellyfin.yml`, `radarr.yml`, etc.) são configuradas para a **Arquitetura ARM** (como Raspberry Pi ou outros dispositivos ARM).

Se você estiver rodando este ambiente em um PC com arquitetura **x86/AMD64**, será necessário alterar o nome das imagens para as versões compatíveis com seu sistema, se aplicável.

---

## 🚀 Visão Geral dos Serviços (Container Functions)

O ecossistema de mídia é composto por vários serviços que trabalham juntos para gerenciar, baixar e reproduzir seu conteúdo.

| Arquivo YAML | Serviço | Função Principal | Categoria |
| :--- | :--- | :--- | :--- |
| `docker-compose.yml` | Docker Compose | Orquestra e define as redes e volumes para todos os containers. | Orquestração |
| `radarr.yml` | **Radarr** | **Gerenciador de Filmes:** Monitora e gerencia a adição automática de filmes. | Gerenciamento |
| `sonarr.yml` | **Sonarr** | **Gerenciador de Séries:** Monitora e gerencia a adição automática de séries de TV. | Gerenciamento |
| `lidarr.yml` | **Lidarr** | **Gerenciador de Música:** Monitora e gerencia a adição automática de músicas/álbuns. | Gerenciamento |
| `bazarr.yml` | **Bazarr** | **Gerenciador de Legendas:** Baixa e sincroniza legendas para seus filmes e séries. | Suporte |
| `prowlarr.yml` | **Prowlarr** | **Gerenciador de Indexadores:** Centraliza a configuração de todos os seus indexadores. | Indexação |
| `jackett.yml` | **Jackett** | **Indexador de Torrents:** Fornece uma API unificada para trackers privados/públicos. | Indexação |
| `qbittorrent.yml` | **qBittorrent** | **Cliente de Download:** Responsável por realizar o download dos arquivos (torrents). | Download |
| `jellyfin.yml` | **Jellyfin** | **Reprodutor/Streamer de Mídia:** Servidor de mídia para assistir seus filmes e séries em vários dispositivos. | Reprodução |
| `flaresolverr.yml` | **FlareSolverr** | **Proxy:** Usado para contornar bloqueios/restrições de busca em sites específicos. | Suporte |

---

## 🛠️ Como Executar

Estes arquivos de configuração são compatíveis com os principais *runtime* de contêineres e podem ser executados usando:

### Opção 1: Docker Compose

Certifique-se de ter o Docker e o Docker Compose instalados. Na pasta raiz do repositório, execute:
```bash
docker-compose up -d
````
### Opção 2: Podman Compose

Certifique-se de ter o Podman e o Podman-Compose instalados. Na pasta raiz do repositório, execute:
```bash
podman-compose up -d
````
