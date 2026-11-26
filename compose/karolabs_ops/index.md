---
# SPDX-FileCopyrightText: © 2026 hazzuk
#
# SPDX-License-Identifier: AGPL-3.0-only

icon: lucide/layers-2
weight: 3
---

# karolabs_ops

Operations and monitoring services.

``` yaml { .no-copy hl_lines="5" }
karo_compose_stack_groups:
  - karolabs_core # setup first
  - karolabs_extra
  - karolabs_media
  - karolabs_ops # order last in list
```
