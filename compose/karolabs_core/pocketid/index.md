---
# SPDX-FileCopyrightText: © 2026 hazzuk
#
# SPDX-License-Identifier: AGPL-3.0-only

icon: custom/pocket-id
---

# Pocket ID

> OIDC provider

``` yaml { title="Ansible vault" }
# oidc

# karo_compose_oidc_subdomain: auth
# karo_compose_oidc_provider_name: PocketID
# karo_compose_oidc_admin_group: admin

# pocketid

karolabs_core_pocketid_enabled: false

karolabs_core_pocketid_stack:
--8<-- "{{ page.url}}/stack.yml:docs"
```

??? abstract "Pocket ID - OIDC provider"

    <div class="grid cards" markdown>

    - :simple-github: [pocket-id/pocket-id](https://github.com/pocket-id/pocket-id)
    - :simple-docker: [docker.io/pocketid/pocket-id](https://hub.docker.com/r/pocketid/pocket-id)

    </div>

    !!! note "Links"

        - :lucide-bookmark: [Documentation](https://pocket-id.org/docs/introduction)
        - :lucide-tag: [Releases](https://github.com/pocket-id/pocket-id/releases)
