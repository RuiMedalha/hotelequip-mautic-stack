
# Mautic Stack (Docker Compose)

Mautic 6 + MySQL 8 + sidecar de cron, pronto para Nginx Proxy Manager (NPM) / Cloudflare.  
**Importante:** não montamos `/var/www/html/config` para evitar que o `local.php` seja sobrescrito pelo template do entrypoint.

---

## 1) Pré‑requisitos

- Docker e Docker Compose instalados no servidor.
- Rede Docker `proxy_default` já criada (é a rede do Nginx Proxy Manager).  
  Se precisares de criar: `docker network create proxy_default`
- DNS do domínio apontado para o teu NPM (ex.: `mautic.hotelequip.pt`).

---

## 2) Configuração

### 2.1 Criar o `.env`

Cria a partir do exemplo:

```bash
cp .env.example .env
nano .env
