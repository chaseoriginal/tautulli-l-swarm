# tautulli-l-swarm

Plex statistics and monitoring (L = Linux Plex host).

## Stack

- **Host**: ore-dock-110-1
- **Stack**: `tautulli-l-swarm`
- **Image**: lscr.io/linuxserver/tautulli:latest
- **Config**: named volume `tautulli-l-swarm.config`

## Ports

| Port | Published | Protocol |
|------|----------|----------|
| 8181 | 81 | TCP |

## Deploy

```bash
ssh ore-dock-110-1
cd /data/compose/tautulli-l-swarm
set -a && source .env && docker stack deploy -c docker-compose.yml --with-registry-auth tautulli-l-swarm && set +a
```
