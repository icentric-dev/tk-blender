# FPTR(ShotGrid) Toolkit Engine for Blender 4.2

This repository is a fork of [tk-blender](https://github.com/diegogarciahuerta/tk-blender). For detailed installation instructions, please refer to the original repository. This toolkit supports Blender 4.2 and is designed for easy deployment. Implementation details are based on [Shotgrid with tk-blender - #11 by zavinator](https://community.shotgridsoftware.com/t/shotgrid-with-tk-blender/17217/11).

## Engine Installation
Add the following changes to `../config/env/includes/engine_locations.yml`
```shell
engines.tk-blender.location:
  type: git
  branch: master
  path: https://github.com/icentric-dev/tk-blender.git
  version: v2.0.0
```

## Configuring Blender Engine Requirements

### PySide6 Installation

To run toolkit applications, PySide6 must be installed where Blender’s Python can access it.

For Windows, install PySide6 in Blender’s bundled Python environment with the following command:

```shell
"C:\Program Files\Blender Foundation\Blender 4.2\4.2\python\bin\python.exe" -m pip install PySide6 --target="C:\Program Files\Blender Foundation\Blender 4.2\4.2\python\lib"
```

Ensure you run this command in an Administrator console, as Blender’s installation directory may require elevated permissions.

### tk-core v0.21.6+

Ensure you use tk-core version v0.21.6 or later to support PySide6.

Modify the version in the configuration file located at: ``/config/core/core_api.yml``

It should look like this:

```yaml
location:
  type: app_store
  name: tk-core
  version: v0.21.6
```
