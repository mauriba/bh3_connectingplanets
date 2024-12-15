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

|               | Naming Conventions                                                    |
| ------------- | --------------------------------------------------------------------- |
| Space         | a lowercase string                                                    |
| Layer         | `A/D/C` for Access, Distribution or Core Layer                        |
| Redundancy    | either `common` or a two-digit increment starting from `01`           |

Note: a config file with the suffix `common` means that it should be used for all redundant
devices of that particular space and layer.

Use these conventions to name active network components as follows:
`[Layer]-[Space]-[Redundancy]`. Store its configuration in `config/[Layer]-[Space]-[Redundancy].cisco`.
