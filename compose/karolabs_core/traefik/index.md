---
# SPDX-FileCopyrightText: © 2026 hazzuk
#
# SPDX-License-Identifier: AGPL-3.0-only

icon: custom/traefik
weight: -2
---

# Traefik

> Reverse proxy

``` yaml { title="Ansible vault" }
# traefik

karolabs_core_traefik_enabled: false

karolabs_core_traefik_stack:
--8<-- "{{ page.url}}/stack.yml:docs"
```

??? abstract "Traefik - Reverse proxy"

    <div class="grid cards" markdown>

    - :simple-github: [traefik/traefik](https://github.com/traefik/traefik)
    - :lucide-bookmark: [Documentation](https://doc.traefik.io/traefik/)

    </div>

    ??? info "Traefik notes"

        - The first time you run Traefik, you should keep ACME staging enabled. Once you've verified that your setup is correct, disable it to request valid TLS certificates. This is to avoid [Let's Encrypt rate limits](https://letsencrypt.org/docs/rate-limits/).

        - It's recommended to disable the Traefik dashboard when your server is exposed publicly.

        - Traefik is set to use TLS 1.3. Cipher suites are not configurable, supported ciphers are [safe](https://golang.org/doc/go1.12#tls_1_3).

        - The Traefik dashboard can be useful when setting up other stacks. As you can check 'HTTP Routers' to ensure the availability of other services.

    ??? tip "Traefik Cloudflare API tokens"

        > Based on the [Lego library docs](https://go-acme.github.io/lego/dns/cloudflare/index.html#api-tokens).

        --8<-- "docs/snippets.md:cloudflare_token"

        === "`traefik_acme_zone_api_token`"

            - Token name

                ``` txt
                Traefik (example.com) - Resolve domain names to Zone IDs
                ```

            - Permissions: Zone, Zone, Read

            - Zone Resources: Include, Specific zone, example.com

        === "`traefik_acme_dns_api_token`"

            - Token name

                ``` txt
                Traefik (example.com) - Edit DNS for DNS-01 challenges
                ```

            - Permissions: Zone, DNS, Edit

            - Zone Resources: Include, Specific zone, example.com

??? abstract "Tinyauth - Authentication middleware (forward auth)"

    <div class="grid cards" markdown>

    - :simple-github: [tinyauthapp/tinyauth](https://github.com/tinyauthapp/tinyauth)
    - :lucide-bookmark: [Documentation](https://tinyauth.app/docs/getting-started/)

    </div>

??? abstract "CetusGuard - Docker socket proxy"

    <div class="grid cards" markdown>

    - :simple-github: [hectorm/cetusguard](https://github.com/hectorm/cetusguard)

    </div>
