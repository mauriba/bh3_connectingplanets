# Connecting Planets

Let's simulate a network infrastructure for the fictitous company
Spaceone. The simulation resides in the Packet Tracer file
`network.pkt`. Any switch or router configuration should be placed
inside `/configs`. This way, we can make use of git versioning and
collaboration while also documenting our work.

## A pull request arrived! How do I combine the configs?

1. Open the packet tracer file.
2. Reboot the active network component (router, switch) whose config has changed.
3. Copy the newly committed config from the git repo.
4. Paste or import the config into the network component.

## Naming conventions

|           | Naming Conventions                                |
| --------- | ------------------------------------------------- |
| Space     | a lowercase string                                |
| Layer     | `A/D/C` for Access, Distribution or Core Layer    |
| Number    | two-digit increment starting from `01`            |

Use these conventions to name active network components as follows:
`[Layer]-[Space]-[Number]`. Store its configuration in `config/[Layer]-[Space]-[Number].cisco`.
