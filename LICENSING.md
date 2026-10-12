# Licensing

Reraise uses two licence tiers.

Copyright: Reraise contributors.

## Which licence applies where

| Part | Licence | In this repository |
| --- | --- | --- |
| Card format specification and other documents | Apache-2.0 | yes |
| Schemas | Apache-2.0 | not yet |
| Libraries and adapters (storage, source, model) | Apache-2.0 | not yet |
| Examples | Apache-2.0 | not yet |
| The app: board, API service, MCP server | AGPL-3.0-or-later | not yet |

Everything in this repository today is under the Apache License 2.0. The full text is in
[LICENSE](LICENSE).

## Why two tiers

- **Open formats and libraries (Apache-2.0).** The card format, schemas, libraries and
  storage, source and model adapters should be adoptable by anyone, including people who run
  their own agent systems and note-taking vaults, without licence friction.
  Interoperability is the point of a card format.
- **The application (AGPL-3.0-or-later).** The board app, the API service and the MCP
  server keep improvements open even when the software is offered as a network service.

The exchange platform operated by Caprey SAS is a separate service, is not open source and
is not part of this repository.

## Contributions and DCO

By contributing you certify the [Developer Certificate of Origin](https://developercertificate.org/)
by signing off every commit (`git commit -s`, which adds a `Signed-off-by:` line). Your
contribution is licensed under the licence of the part it lands in. See
[CONTRIBUTING.md](CONTRIBUTING.md).

## SPDX header

Source files carry an SPDX header:

```ts
// SPDX-License-Identifier: Apache-2.0
// Copyright Reraise contributors
```

AGPL parts use `AGPL-3.0-or-later`.
