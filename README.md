# Project Ordinance: Black Mesa Roleplay

![Project Ordinance logo](logo.png)

**Project Ordinance: Black Mesa Roleplay** is a Garry's Mod roleplay schema built on the **Parallax** framework and set in the **Black Mesa** universe.

This repository contains the gameplay code, schema definitions, modules, custom entities, bundled content, audio/visual assets, and developer tooling from a project that lived privately for a long time and is now being released as open source.

## Status

- **Current open-source repository version:** `0.3.04`
- **Gamemode ID:** `bmrp`
- **Base framework:** `parallax`
- **Author:** Riggs
- **Repository state:** formerly private, now open source

Because this was a long-running private codebase, you should expect a mix of production code, project-specific assumptions, and historical conventions that were originally written for a live server environment rather than for public distribution.

## What this project includes

The repository contains:

- a Parallax-based Black Mesa roleplay schema
- faction and class definitions for multiple departments and progression paths
- client/server gameplay modules
- custom content under `content/` such as materials, models, particles, fonts, localization, and sounds
- custom weapons/entities under `entities/`
- helper tooling under `tools/` for asset and mapping workflows

## Notable systems

From the current repository layout, the project includes work around systems such as:

- custom chatbox
- emote wheel
- talking animations
- footsteps and viewbob
- ambients / scapes / weapon reverb
- bodygroup management
- moods
- NVGs and ultravision
- plants
- security cameras
- vending machines
- maintenance and funding systems
- ARC9 support hooks

## Factions and progression

The schema currently includes faction and class data for groups such as:

- Administrative Department
- Research & Development
- Security Division
- Service Personnel
- Hazardous Environments Combat Unit
- Black Ops
- Creatures

It also contains class files for administrative, research, security, and service-side role progression.

## Repository layout

```text
.
├─ content/      # bundled assets: materials, models, particles, sounds, fonts, localization, etc.
├─ entities/     # custom scripted entities / weapons
├─ gamemode/     # core gamemode, modules, schema boot/config/hooks/factions/classes/items/libraries
├─ tools/        # Python utilities for scapes, material cleanup, and mapping workflows
├─ LICENSE       # GNU AGPL v3
├─ bmrp.txt      # Garry's Mod gamemode metadata
└─ version.json  # repository version metadata
```

## Developer tools

The `tools/` directory contains a small set of Python utilities used during development, including:

- `generate_scapes_from_soundscapes.py` - converts Source 1 soundscape KeyValues into Parallax scape registrations
- `adjust_labcrete_vmf.py` - adjusts LABCRETE texture axes in VMF files
- `strip_vmt_bump_env_phong.py` - strips selected material keys from VMT files
- `python -m tools` - launches the bundled GUI wrapper for these tools (requires `PySide6`)

## Getting started

This is best treated as an **open-source developer release** rather than a one-click public package.

At a high level, running or developing against it looks like this:

1. Install or prepare a Garry's Mod server/development environment.
2. Install the **[Parallax](https://github.com/Parallax-Framework/parallax)** framework this schema derives from.
3. Place this repository in your `garrysmod/gamemodes/bmrp` directory.
4. Configure your own database/backend and environment-specific settings locally.
5. Ensure required client content is mounted, packed, or distributed for your deployment.
6. Launch Garry's Mod using the `bmrp` gamemode.

### Important setup note

This repository may still assume local dependencies, plugins, or private server-side infrastructure that were present during its private lifespan. If you are trying to run it outside its original environment, expect some integration work.

Also, do **not** reuse any old/private credentials or deployment secrets. Configure your own environment from scratch.

## Open-source release note

This project is being published to preserve the work, make the code available for study, and allow the community to run, improve, and extend it in the open.

If you are reading older comments or source headers that reflect the project's former private status, treat them as historical leftovers from the pre-release period. The open-source release is governed by the repository's root license file.

## License

This repository is licensed under the **GNU Affero General Public License v3.0**.

See [`LICENSE`](LICENSE) for the full legal text.

### AGPL in plain English

Anyone can:

- use this code
- study this code
- modify this code
- run this code privately
- run this code commercially

But if they do, they must follow the AGPL rules.

In practice, that means they must:

- release the source code for modifications they distribute or publish
- keep modified versions under the same AGPL license terms when conveying them
- preserve the license and copyright notices
- **also release the corresponding source for server-side changes when users interact with a modified version over a network**

That last point is the important AGPL difference: **if you run a modified version on a server, the users interacting with that server must be able to get the source code for the version you are running**.

So, to be completely clear:

- You **can** use it.
- You **can** modify it.
- You **can** run it commercially.
- You **cannot** keep your modifications private if you distribute them.
- You **also cannot** keep server-side modifications private if users are interacting with that modified version over a network.

This section is only a plain-English summary. The actual license text in [`LICENSE`](LICENSE) is what governs.

## Contributing

Bug fixes, cleanup, documentation improvements, compatibility work, and feature contributions are welcome.

By contributing to this repository, you agree that your contributions are submitted under the same AGPL-3.0 license as the rest of the project unless explicitly stated otherwise.

## Credits

- **Project Ordinance: Black Mesa Roleplay**
- **Riggs**
- Built on **Parallax**

## Disclaimer

This is a fan project release. Any franchise, universe, brand, or trademark references related to **Black Mesa**, **Half-Life**, or associated properties belong to their respective owners.
