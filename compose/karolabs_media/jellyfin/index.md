---
# SPDX-FileCopyrightText: © 2026 hazzuk
#
# SPDX-License-Identifier: AGPL-3.0-only

icon: simple/jellyfin
weight: 20
---

# Jellyfin

> Media server

``` yaml { title="Ansible vault" }
# jellyfin

karolabs_media_jellyfin_enabled: false

karolabs_media_jellyfin_stack:
--8<-- "karo-compose/defaults/main/karolabs_media/jellyfin.yml:docs"
```

??? abstract "Jellyfin - Media server"

    <div class="grid cards" markdown>

    - :simple-github: [jellyfin/jellyfin](https://github.com/jellyfin/jellyfin)
    - :simple-docker: [docker.io/jellyfin/jellyfin](https://hub.docker.com/r/jellyfin/jellyfin)

    </div>

    ??? tip "Jellyfin initial setup"

        === "Server"

            - Server name: `example`
            - Username: `#!ini <jellyfin admin username>`
            - Password: `#!ini <jellyfin admin password>`

        === "Media"

            -   Movies
                - Folders: `#!ini <radarr root folder>` (e.g. `/data/media/movies`)
                - Preferred download language: `#!ini <your language>`
                - Country/region: `#!ini <your region>`

            -   TV
                - Display name: `Series`
                - Folders: `#!ini <sonarr root folder>` (e.g. `/data/media/series`)
                - Preferred download language `#!ini <your language>`
                - Country/region `#!ini <your region>`

        === "Metadata language"

            - Country/region: `#!ini <your region>`

        === "Remote access"

            - Allow remote connections to this server: `false`

    !!! note "Links"

        - :lucide-bookmark: [Documentation](https://jellyfin.org/docs/)
        - :lucide-tag: [Releases](https://github.com/jellyfin/jellyfin/releases)
