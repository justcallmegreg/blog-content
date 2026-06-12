---
title: "Reactor Diagnostics Routine"
description: "Running the daily containment check."
---
# Reactor Diagnostics

Run the following on the maintenance terminal:

```bash
sudo vaultctl reactor --status --verbose
```

Expected output:

```
core temp .... 451 K
coolant ...... OK
containment .. 99.7%
```

Containment schematic:

![reactor schematic](./assets/reactor.svg)

All systems within acceptable parameters. Resume normal operations.
