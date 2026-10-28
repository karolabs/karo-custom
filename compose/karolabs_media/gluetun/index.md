---
# SPDX-FileCopyrightText: © 2026 hazzuk
#
# SPDX-License-Identifier: AGPL-3.0-only

icon: custom/gluetun
weight: 0
---

# Gluetun

> Docker VPN client

``` yaml { title="Ansible vault" }
# gluetun

karolabs_media_gluetun_enabled: false

karolabs_media_gluetun_stack:
--8<-- "{{ page.url}}/stack.yml:docs"
```

??? abstract "Gluetun - Docker VPN client"

    <div class="grid cards" markdown>

    - :simple-github: [passteque/gluetun](https://github.com/passteque/gluetun)
    - :simple-docker: [docker.io/qmcgaw/gluetun](https://hub.docker.com/r/qmcgaw/gluetun)

    </div>

    !!! info "WireGuard config"

        Your VPN service should be able to provide you with a `wireguard.conf` file.

    !!! note "Links"

        - :lucide-bookmark: [Documentation](https://github.com/qdm12/gluetun-wiki)
        - :lucide-tag: [Releases](https://github.com/passteque/gluetun/releases)
