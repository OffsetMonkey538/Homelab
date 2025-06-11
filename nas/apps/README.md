# Apps on NAS

My nas is what runs almost everything.

## List of apps
- todo


## Using compose files on TrueNas Scale
TrueNas Scale has it's own apps stuff, but I want to touch this stuff myself so I'm using compose files.

To use compose files in TrueNas Scale, I first go to `Apps`, then `Discover Apps`, then click on the three dots *next to* `Custom App` and select `Install via YAML`.
Then I add the name for the service and the following under `Custom Config`:
```yml
include:
  - /mnt/apps-ssd/apps/service-name/docker-compose.yml
```
This way I can make changes to the file on disk (via SMB) and just restart the service from the TrueNas web ui.
