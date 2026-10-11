# vivutio/supplier-pack

**What a supplier installs.** A business that runs camps, lodges or hotels and sells their rooms: the properties it runs and their bookings.

## Contents

- [Install](#install)
- [What it holds](#what-it-holds)
- [How it is proven](#how-it-is-proven)
- [Licence](#licence)

## Install

In a vivutio installation:

```bash
composer require supplier
php bin/console doctrine:migrations:migrate
```

`supplier` is the pack's alias, given by the recipes endpoint the skeleton reads.
The pack is unpacked as it installs: the project's `composer.json` then
requires each module by its own name and version, and this package is not kept.
From then on each module is updated, or removed, on its own.

## What it holds

| Module | What it adds |
|---|---|
| [`vivutio/property-module`](https://github.com/utafitilabs/vivutio-property-module) | The camps, lodges and hotels you run: rooms, seasons, rates, availability and bookings |

Only the essentials are in a pack. Any other module is one more
`composer require`; the skeleton's README lists them all.

## How it is proven

The fleet gate installs the official modules through the packs, with the
commands above, and opens each module's first page. A version of this pack is
tagged only by its release workflow, after that gate.

## Licence

AGPL-3.0-or-later. See [LICENSE](LICENSE).
