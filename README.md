# go-ssb-room

Scuttlebutt room server, implemented in Go

<!-- metadata -->
* **Category**: Utilities
* **Status**: ❹💣
* **Image**: [`3wordchant/go-ssb-room`](https://hub.docker.com/r/3wordchant/go-ssb-room), ❹💣, own
* **Healthcheck**: ❌
* **Backups**: ❌
* **Email**: N/A
* **Tests**: ❌
* **SSO**: ❌
<!-- endmetadata -->

## Basic usage

1. Set up Docker Swarm and [`abra`]
2. Deploy [`coop-cloud/traefik`]
3. `abra app new go-ssb-room`
4. `abra app YOURAPPDOMAIN config` - be sure to change `$DOMAIN` to something that resolves to
   your Docker swarm box
5. `abra app YOURAPPDOMAIN deploy`
6. To set someone (yourself?) as an initial user, run 
   ```
   abra app YOURAPPDOMAIN run app "/app/cmd/insert-user/insert-user -repo /app/data @your-ssb-cryptkey.edXXX" 
   ```

[`abra`]: https://git.autonomic.zone/autonomic-cooperative/abra
[`coop-cloud/traefik`]: https://git.autonomic.zone/coop-cloud/traefik
