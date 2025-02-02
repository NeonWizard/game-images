# game-images

Game server docker images for the following games:

* [alt:V](altv/README.md)
* [ARK: Survival Evolved](ark/README.md)
* [ARMA III](arma3/README.md)
* [ARMA III for Windows Containers](arma3-win/README.md)
* [Counter Strike: Global Offensive](csgo/README.md)
* [Eco](eco/README.md)
* [Garry's Mod](gmod/README.md)
* [Project: Zomboid](pz/README.md)
* [Rust](rust/README.md)
* [Satisfactory](satisfactory/README.md)
* [SCP: Secret Laboratory](scpsl/README.md)
* [Valheim](valheim/README.md)
* [V Rising](vrising/README.md)

See the README of individual games for more information.

To run Minecraft servers, the following image is recommended: https://github.com/itzg/docker-minecraft-server.

These images are used for [IPS Hosting](https://www.ips-hosting.com/), a german game server hosting provider. However, feel free to use them for your own needs.

# Input sanitization
All the images, expect the given user input (e.g. command line arguments and environment variables) to be safe and already sanitized.
 

## Building and Versioning
On every push to the main branch, all images that were changed are automatically rebuilt and deployed to Docker Hub using the following tags:
* The image version (e.g. v1, v2, ...)
* latest

In addition, each image is rebuilt and deployed weekly at Sunday 00:00 to keep up with latest security patches.

The image version is configured as an env variable in the workflow file of the game in the `.github/workflows/` directory and should be raised whenever a breaking change is introduced to a game image.

PRs are welcome!
