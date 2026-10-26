Resource UUIDs are now available in the client backend API and `clustat --json`
output through `nodes[].gres[].uuid`. Devices without a UUID return `null`.
You can also use `-json`; the normal terminal view stays the same.

Only the client package needs updating, including both `clustat-backend` and
`clustat`. Restart `clustat-client.service` after upgrading. No server update or
configuration changes are needed.

UUID checks are now part of the E2E inventory comparisons, with regression tests
covering missing UUIDs, filtering, device reordering, and inventory changes.

Changes: [#13](https://github.com/TING-HiuYu/clustat/pull/13).
