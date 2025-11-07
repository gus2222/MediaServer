# 🗄️ Servidor MediaServer (Configurações YAML)

Este repositório armazena os arquivos de configuração YAML utilizados para gerenciar o ambiente de mídia Docker.

## 🚀 Visão Geral dos Serviços (Container Functions)

O ecossistema de mídia é composto por vários serviços que trabalham juntos para gerenciar, baixar e reproduzir seu conteúdo.

| Arquivo YAML | Serviço | Função Principal | Categoria |
| :--- | :--- | :--- | :--- |
| \`docker-compose.yml\` | Docker Compose | Orquestração principal dos serviços. | Orquestração |
| \`bazarr.yml\` | **Bazarr** | **Gerenciador de Legendas:** Baixa e sincroniza legendas para seus filmes e séries. | Suporte |
| \`flaresolverr.yml\` | **FlareSolverr** | **Proxy:** Usado para contornar bloqueios/restrições de busca em sites específicos. | Suporte |
| \`jackett.yml\` | **Jackett** | **Indexador de Torrents:** Fornece uma API unificada para trackers privados/públicos. | Indexação |
| \`jellyfin.yml\` | **Jellyfin** | **Reprodutor/Streamer de Mídia:** Servidor de mídia para assistir seus filmes e séries em vários dispositivos. | Reprodução |
| \`lidarr.yml\` | **Lidarr** | **Gerenciador de Música:** Monitora e gerencia a adição automática de músicas/álbuns. | Gerenciamento |
| \`prowlarr.yml\` | **Prowlarr** | **Gerenciador de Indexadores:** Centraliza a configuração de todos os seus indexadores. | Indexação |
| \`qbittorrent.yml\` | **qBittorrent** | **Cliente de Download:** Responsável por realizar o download dos arquivos (torrents). | Download |
| \`radarr.yml\` | **Radarr** | **Gerenciador de Filmes:** Monitora e gerencia a adição automática de filmes. | Gerenciamento |
| \`sonarr.yml\` | **Sonarr** | **Gerenciador de Séries:** Monitora e gerencia a adição automática de séries de TV. | Gerenciamento |

---

## 🛠️ Próximos Passos

1.  **Configurar Volumes:** Verifique se os caminhos definidos nos volumes (`volumes:`) em cada arquivo YAML apontam corretamente para os diretórios de *Downloads*, *Filmes*, *Séries* e *Música* no seu sistema hospedeiro.
2.  **Ajustar Portas:** Revise as portas mapeadas para garantir que não haja conflitos com outros serviços no seu host.
