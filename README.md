# Kasm DeckCraft
DeckCraft (https://github.com/storytold/deckcraft) docker image for Kasm Workspaces (https://kasm.com)

Built for `linux/amd64` and `linux/arm64`. The latest DeckCraft release `.deb` is installed at build time.

Load this image into Kasm Workspaces by adding the Sully's Choice Kasm Workspace Registry: https://sullyschoice.github.io/kasm-registry/

## Manual Run

```bash
sudo docker run --rm -it --shm-size=512m -p 6901:6901 -e VNC_PW=password sccr.sullyschoice.net/sullyschoice/kasm-deckcraft:latest
```

Access via your browser: `https://<your ip>:6901` username: `kasm` , password: `password`

## Build
```bash
sudo docker build -t kasm-deckcraft:latest -f Dockerfile .
```

To pin a specific DeckCraft version:
```bash
sudo docker build --build-arg DECKCRAFT_VERSION=0.6.1 -t kasm-deckcraft:0.6.1 -f Dockerfile .
```
