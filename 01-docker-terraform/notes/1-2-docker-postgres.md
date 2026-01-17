# 1.2 — Docker + Postgres Notes

## Goal

## Prerequisites
1. GitHub account to use CodeSpaces
2. Python installed
3. Docker installed

## Key concepts
### Docker fundamentals
- **Isolation:** A container is isolated from your host machine, so actions inside the container don’t affect your system.
- **Image vs Container:** An image is a snapshot/template; a container is a running instance created from that image.
- **Stateless by default:** Containers don’t preserve changes by default; when you rerun from the same image, you typically start “fresh” again.
### Volumes
- **Volume (-v):** Map a host folder into a container so files can be accessed from both sides (and to preserve data).
### Postgres with Docker
- **Environment variables (-e):** Used to configure containers (e.g., Postgres user/password/database).
- **Port mapping (-p HOST:CONTAINER):** Expose a container port to your machine (so localhost:<port> forwards into the container).
### Networking
- **Localhost confusion:** When multiple containers need to talk, they must be on the same Docker network and connect using the container/service name (not localhost).
### Docker Compose
- **Compose = multiple services in one file:** A docker-compose.yml defines everything needed to run Postgres + pgAdmin together.
- **Same network by default:** Services in the same compose file run on the same default network and can reach each other by service name (e.g., pgdatabase).

## Practice with instructor

## Commands
> [!NOTE]
>Bash is case senstive.

| Command | Description |
| --- | --- |
| `python -V` & `python --version` | Check Python version |
| `echo 'PS1="> "' > ~/.bashrc` | Overwrites your entire bash configuration and simplifies your terminal prompt |
| `docker` | Prints the help/usage text for docker (proves the Docker CLI is installed and runnable) |
| `dcoker run  hello-world` | Does an end-to-end Docker test |
| `dcoker run -it ubuntu` | Interact with docker image |

## Gotchas / Warnings

## New terms

## References
-  What is Docker? [Link](https://docs.docker.com/get-started/docker-overview/)
