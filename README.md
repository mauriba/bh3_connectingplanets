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

## Network segmentation

### Spaces

| Space         | Description                                           | Address Space     |
| ------------- | ----------------------------------------------------- | ----------------- |
| `transport`   | Address space for transport networks on mars.         | `10.0.0.0/16`     |
| `main`        | The main network for SpaceOne's main colony.          | `10.1.0.0/16`     |
| `usa`         | A US settlement on mars.                              | `10.2.0.0/16`     |
| `russia`      | A Russian settlement on mars.                         | `10.3.0.0/16`     |
| `china`       | A Chinese settlement on mars.                         | `10.4.0.0/16`     |
| `earth`       | Address space of SpaceOne's lab on earth.             | `10.5.0.0/16`     |
