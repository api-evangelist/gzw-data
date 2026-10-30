# GZW Data API

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

GZW Data is a free, fan-made, read-only REST API for Gray Zone Warfare game data, published by independent maintainer ZoniBoy00 and hosted on Vercel at gzw-data.dev. It exposes 85+ datasets auto-discovered from a wiki-scraped data directory - weapons, ammo, armor, magazines, attachments, tasks and missions, keys and keycards, loot containers, medical, provisions, gear and vendors - behind one uniform JSON envelope with equality filters, full-text search, sorting and page-number pagination. Three smart routes union related datasets (armor, weapon_parts, helmet_mods). There is no authentication, no account and no API key; access is governed by a best-effort limit of 100 requests per minute per IP with X-RateLimit-* headers. An OpenAPI 3.0.3 contract, an llms.txt and a zero-dependency TypeScript client on npm are published. Data is scraped weekly from the community GZW Fandom Wiki; the project is unofficial and not affiliated with the game's publisher.

**Areas:** Gaming · Video Games · gray-zone-warfare · Game Data · Developer Tools · Open Data · OpenAPI · Weapons · Missions · loot · REST API · Public APIs

## GZW Data API on APIs.io

Everything profiled for GZW Data API is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/gzw-data/](https://apis.io/providers/gzw-data/)** — or go straight to one of the APIs or properties below.

### APIs (95)

- [GZW Data API Ammo API](https://apis.io/apis/gzw-data/gzw-data-ammo-api/) — The Ammo API from GZW Data API — 4 operation(s) for ammo.
- [GZW Data API Apparel Items API](https://apis.io/apis/gzw-data/gzw-data-apparel-items-api/) — The Apparel Items API from GZW Data API — 4 operation(s) for apparel items.
- [GZW Data API Armor API](https://apis.io/apis/gzw-data/gzw-data-armor-api/) — The Armor API from GZW Data API — 2 operation(s) for armor.
- [GZW Data API Auxiliary API](https://apis.io/apis/gzw-data/gzw-data-auxiliary-api/) — The Auxiliary API from GZW Data API — 4 operation(s) for auxiliary.
- [GZW Data API Backpacks API](https://apis.io/apis/gzw-data/gzw-data-backpacks-api/) — The Backpacks API from GZW Data API — 4 operation(s) for backpacks.
- [GZW Data API Barrels API](https://apis.io/apis/gzw-data/gzw-data-barrels-api/) — The Barrels API from GZW Data API — 4 operation(s) for barrels.
- [GZW Data API Belts API](https://apis.io/apis/gzw-data/gzw-data-belts-api/) — The Belts API from GZW Data API — 4 operation(s) for belts.
- [GZW Data API Binoculars API](https://apis.io/apis/gzw-data/gzw-data-binoculars-api/) — The Binoculars API from GZW Data API — 4 operation(s) for binoculars.
- [GZW Data API Boots API](https://apis.io/apis/gzw-data/gzw-data-boots-api/) — The Boots API from GZW Data API — 4 operation(s) for boots.
- [GZW Data API Buffer Tubes API](https://apis.io/apis/gzw-data/gzw-data-buffer-tubes-api/) — The Buffer Tubes API from GZW Data API — 4 operation(s) for buffer tubes.
- [GZW Data API Charging Handle API](https://apis.io/apis/gzw-data/gzw-data-charging-handle-api/) — The Charging Handle API from GZW Data API — 4 operation(s) for charging handle.
- [GZW Data API Cleanup API](https://apis.io/apis/gzw-data/gzw-data-cleanup-api/) — The Cleanup API from GZW Data API — 4 operation(s) for cleanup.
- [GZW Data API Collimators API](https://apis.io/apis/gzw-data/gzw-data-collimators-api/) — The Collimators API from GZW Data API — 4 operation(s) for collimators.
- [GZW Data API Containers API](https://apis.io/apis/gzw-data/gzw-data-containers-api/) — The Containers API from GZW Data API — 4 operation(s) for containers.
- [GZW Data API Contract API](https://apis.io/apis/gzw-data/gzw-data-contract-api/) — The Contract API from GZW Data API — 4 operation(s) for contract.
- [GZW Data API Contracts API](https://apis.io/apis/gzw-data/gzw-data-contracts-api/) — The Contracts API from GZW Data API — 4 operation(s) for contracts.
- [GZW Data API Drinks API](https://apis.io/apis/gzw-data/gzw-data-drinks-api/) — The Drinks API from GZW Data API — 4 operation(s) for drinks.
- [GZW Data API Electronics API](https://apis.io/apis/gzw-data/gzw-data-electronics-api/) — The Electronics API from GZW Data API — 4 operation(s) for electronics.
- [GZW Data API Face Cover API](https://apis.io/apis/gzw-data/gzw-data-face-cover-api/) — The Face Cover API from GZW Data API — 4 operation(s) for face cover.
- [GZW Data API Food API](https://apis.io/apis/gzw-data/gzw-data-food-api/) — The Food API from GZW Data API — 4 operation(s) for food.
- [GZW Data API Foregrips API](https://apis.io/apis/gzw-data/gzw-data-foregrips-api/) — The Foregrips API from GZW Data API — 4 operation(s) for foregrips.
- [GZW Data API Front Iron Sights API](https://apis.io/apis/gzw-data/gzw-data-front-iron-sights-api/) — The Front Iron Sights API from GZW Data API — 4 operation(s) for front iron sights.
- [GZW Data API Funds API](https://apis.io/apis/gzw-data/gzw-data-funds-api/) — The Funds API from GZW Data API — 4 operation(s) for funds.
- [GZW Data API Gas Blocks API](https://apis.io/apis/gzw-data/gzw-data-gas-blocks-api/) — The Gas Blocks API from GZW Data API — 4 operation(s) for gas blocks.
- [GZW Data API Gear API](https://apis.io/apis/gzw-data/gzw-data-gear-api/) — The Gear API from GZW Data API — 4 operation(s) for gear.
- [GZW Data API Glasses API](https://apis.io/apis/gzw-data/gzw-data-glasses-api/) — The Glasses API from GZW Data API — 4 operation(s) for glasses.
- [GZW Data API Gloves API](https://apis.io/apis/gzw-data/gzw-data-gloves-api/) — The Gloves API from GZW Data API — 4 operation(s) for gloves.
- [GZW Data API GZW Data API](https://apis.io/apis/gzw-data/gzw-data-gzw-data-api-api/) — The GZW Data API API from GZW Data API — 2 operation(s) for gzw data api.
- [GZW Data API Handguards API](https://apis.io/apis/gzw-data/gzw-data-handguards-api/) — The Handguards API from GZW Data API — 4 operation(s) for handguards.
- [GZW Data API Headsets API](https://apis.io/apis/gzw-data/gzw-data-headsets-api/) — The Headsets API from GZW Data API — 4 operation(s) for headsets.
- [GZW Data API Health API](https://apis.io/apis/gzw-data/gzw-data-health-api/) — The Health API from GZW Data API — 2 operation(s) for health.
- [GZW Data API Helmet Mods API](https://apis.io/apis/gzw-data/gzw-data-helmet-mods-api/) — The Helmet Mods API from GZW Data API — 2 operation(s) for helmet mods.
- [GZW Data API Helmet Mounts API](https://apis.io/apis/gzw-data/gzw-data-helmet-mounts-api/) — The Helmet Mounts API from GZW Data API — 4 operation(s) for helmet mounts.
- [GZW Data API Helmets API](https://apis.io/apis/gzw-data/gzw-data-helmets-api/) — The Helmets API from GZW Data API — 4 operation(s) for helmets.
- [GZW Data API Hidden Task API](https://apis.io/apis/gzw-data/gzw-data-hidden-task-api/) — The Hidden Task API from GZW Data API — 4 operation(s) for hidden task.
- [GZW Data API Household Item API](https://apis.io/apis/gzw-data/gzw-data-household-item-api/) — The Household Item API from GZW Data API — 4 operation(s) for household item.
- [GZW Data API Intels API](https://apis.io/apis/gzw-data/gzw-data-intels-api/) — The Intels API from GZW Data API — 4 operation(s) for intels.
- [GZW Data API Items API](https://apis.io/apis/gzw-data/gzw-data-items-api/) — The Items API from GZW Data API — 4 operation(s) for items.
- [GZW Data API Jewellery API](https://apis.io/apis/gzw-data/gzw-data-jewellery-api/) — The Jewellery API from GZW Data API — 4 operation(s) for jewellery.
- [GZW Data API Keycards API](https://apis.io/apis/gzw-data/gzw-data-keycards-api/) — The Keycards API from GZW Data API — 4 operation(s) for keycards.
- [GZW Data API Keys API](https://apis.io/apis/gzw-data/gzw-data-keys-api/) — The Keys API from GZW Data API — 4 operation(s) for keys.
- [GZW Data API Laboratory Supplies API](https://apis.io/apis/gzw-data/gzw-data-laboratory-supplies-api/) — The Laboratory Supplies API from GZW Data API — 4 operation(s) for laboratory supplies.
- [GZW Data API Lockboxes API](https://apis.io/apis/gzw-data/gzw-data-lockboxes-api/) — The Lockboxes API from GZW Data API — 4 operation(s) for lockboxes.
- [GZW Data API Loot Container API](https://apis.io/apis/gzw-data/gzw-data-loot-container-api/) — The Loot Container API from GZW Data API — 4 operation(s) for loot container.
- [GZW Data API Loot Containers API](https://apis.io/apis/gzw-data/gzw-data-loot-containers-api/) — The Loot Containers API from GZW Data API — 4 operation(s) for loot containers.
- [GZW Data API Loot Items API](https://apis.io/apis/gzw-data/gzw-data-loot-items-api/) — The Loot Items API from GZW Data API — 4 operation(s) for loot items.
- [GZW Data API Magazines API](https://apis.io/apis/gzw-data/gzw-data-magazines-api/) — The Magazines API from GZW Data API — 4 operation(s) for magazines.
- [GZW Data API Main Task API](https://apis.io/apis/gzw-data/gzw-data-main-task-api/) — The Main Task API from GZW Data API — 4 operation(s) for main task.
- [GZW Data API Medical API](https://apis.io/apis/gzw-data/gzw-data-medical-api/) — The Medical API from GZW Data API — 4 operation(s) for medical.
- [GZW Data API Metadata API](https://apis.io/apis/gzw-data/gzw-data-metadata-api/) — The Metadata API from GZW Data API — 4 operation(s) for metadata.
- [GZW Data API Military Equipment API](https://apis.io/apis/gzw-data/gzw-data-military-equipment-api/) — The Military Equipment API from GZW Data API — 4 operation(s) for military equipment.
- [GZW Data API Military Material API](https://apis.io/apis/gzw-data/gzw-data-military-material-api/) — The Military Material API from GZW Data API — 4 operation(s) for military material.
- [GZW Data API Mortar Rounds API](https://apis.io/apis/gzw-data/gzw-data-mortar-rounds-api/) — The Mortar Rounds API from GZW Data API — 4 operation(s) for mortar rounds.
- [GZW Data API Mounts API](https://apis.io/apis/gzw-data/gzw-data-mounts-api/) — The Mounts API from GZW Data API — 4 operation(s) for mounts.
- [GZW Data API Muzzle Devices API](https://apis.io/apis/gzw-data/gzw-data-muzzle-devices-api/) — The Muzzle Devices API from GZW Data API — 4 operation(s) for muzzle devices.
- [GZW Data API Night Vision API](https://apis.io/apis/gzw-data/gzw-data-night-vision-api/) — The Night Vision API from GZW Data API — 4 operation(s) for night vision.
- [GZW Data API Paper API](https://apis.io/apis/gzw-data/gzw-data-paper-api/) — The Paper API from GZW Data API — 4 operation(s) for paper.
- [GZW Data API Pistol Grips API](https://apis.io/apis/gzw-data/gzw-data-pistol-grips-api/) — The Pistol Grips API from GZW Data API — 4 operation(s) for pistol grips.
- [GZW Data API Plate Carrier API](https://apis.io/apis/gzw-data/gzw-data-plate-carrier-api/) — The Plate Carrier API from GZW Data API — 4 operation(s) for plate carrier.
- [GZW Data API Plate Carriers API](https://apis.io/apis/gzw-data/gzw-data-plate-carriers-api/) — The Plate Carriers API from GZW Data API — 4 operation(s) for plate carriers.
- [GZW Data API Provisions API](https://apis.io/apis/gzw-data/gzw-data-provisions-api/) — The Provisions API from GZW Data API — 4 operation(s) for provisions.
- [GZW Data API Reading Intel API](https://apis.io/apis/gzw-data/gzw-data-reading-intel-api/) — The Reading Intel API from GZW Data API — 4 operation(s) for reading intel.
- [GZW Data API Ready API](https://apis.io/apis/gzw-data/gzw-data-ready-api/) — The Ready API from GZW Data API — 2 operation(s) for ready.
- [GZW Data API Rear Iron Sights API](https://apis.io/apis/gzw-data/gzw-data-rear-iron-sights-api/) — The Rear Iron Sights API from GZW Data API — 4 operation(s) for rear iron sights.
- [GZW Data API Removed Content API](https://apis.io/apis/gzw-data/gzw-data-removed-content-api/) — The Removed Content API from GZW Data API — 4 operation(s) for removed content.
- [GZW Data API Repair Kits API](https://apis.io/apis/gzw-data/gzw-data-repair-kits-api/) — The Repair Kits API from GZW Data API — 4 operation(s) for repair kits.
- [GZW Data API Rigs API](https://apis.io/apis/gzw-data/gzw-data-rigs-api/) — The Rigs API from GZW Data API — 4 operation(s) for rigs.
- [GZW Data API Scopes API](https://apis.io/apis/gzw-data/gzw-data-scopes-api/) — The Scopes API from GZW Data API — 4 operation(s) for scopes.
- [GZW Data API Shirts API](https://apis.io/apis/gzw-data/gzw-data-shirts-api/) — The Shirts API from GZW Data API — 4 operation(s) for shirts.
- [GZW Data API Side Task API](https://apis.io/apis/gzw-data/gzw-data-side-task-api/) — The Side Task API from GZW Data API — 4 operation(s) for side task.
- [GZW Data API Slides API](https://apis.io/apis/gzw-data/gzw-data-slides-api/) — The Slides API from GZW Data API — 4 operation(s) for slides.
- [GZW Data API Squad Strike Missions API](https://apis.io/apis/gzw-data/gzw-data-squad-strike-missions-api/) — The Squad Strike Missions API from GZW Data API — 4 operation(s) for squad strike missions.
- [GZW Data API Squad Strike Missions Item API](https://apis.io/apis/gzw-data/gzw-data-squad-strike-missions-item-api/) — The Squad Strike Missions Item API from GZW Data API — 4 operation(s) for squad strike missions item.
- [GZW Data API Stock Adapters API](https://apis.io/apis/gzw-data/gzw-data-stock-adapters-api/) — The Stock Adapters API from GZW Data API — 4 operation(s) for stock adapters.
- [GZW Data API Stocks API](https://apis.io/apis/gzw-data/gzw-data-stocks-api/) — The Stocks API from GZW Data API — 4 operation(s) for stocks.
- [GZW Data API Suppressors API](https://apis.io/apis/gzw-data/gzw-data-suppressors-api/) — The Suppressors API from GZW Data API — 4 operation(s) for suppressors.
- [GZW Data API Tactical Devices API](https://apis.io/apis/gzw-data/gzw-data-tactical-devices-api/) — The Tactical Devices API from GZW Data API — 4 operation(s) for tactical devices.
- [GZW Data API Task Items API](https://apis.io/apis/gzw-data/gzw-data-task-items-api/) — The Task Items API from GZW Data API — 4 operation(s) for task items.
- [GZW Data API Tasks API](https://apis.io/apis/gzw-data/gzw-data-tasks-api/) — The Tasks API from GZW Data API — 4 operation(s) for tasks.
- [GZW Data API Throwables API](https://apis.io/apis/gzw-data/gzw-data-throwables-api/) — The Throwables API from GZW Data API — 4 operation(s) for throwables.
- [GZW Data API Tools API](https://apis.io/apis/gzw-data/gzw-data-tools-api/) — The Tools API from GZW Data API — 4 operation(s) for tools.
- [GZW Data API Trousers API](https://apis.io/apis/gzw-data/gzw-data-trousers-api/) — The Trousers API from GZW Data API — 4 operation(s) for trousers.
- [GZW Data API Upcoming Content API](https://apis.io/apis/gzw-data/gzw-data-upcoming-content-api/) — The Upcoming Content API from GZW Data API — 4 operation(s) for upcoming content.
- [GZW Data API Upper Receivers API](https://apis.io/apis/gzw-data/gzw-data-upper-receivers-api/) — The Upper Receivers API from GZW Data API — 4 operation(s) for upper receivers.
- [GZW Data API Valuables API](https://apis.io/apis/gzw-data/gzw-data-valuables-api/) — The Valuables API from GZW Data API — 4 operation(s) for valuables.
- [GZW Data API Vendors API](https://apis.io/apis/gzw-data/gzw-data-vendors-api/) — The Vendors API from GZW Data API — 4 operation(s) for vendors.
- [GZW Data API Vests API](https://apis.io/apis/gzw-data/gzw-data-vests-api/) — The Vests API from GZW Data API — 4 operation(s) for vests.
- [GZW Data API Vices API](https://apis.io/apis/gzw-data/gzw-data-vices-api/) — The Vices API from GZW Data API — 4 operation(s) for vices.
- [GZW Data API Weapon Parts API](https://apis.io/apis/gzw-data/gzw-data-weapon-parts-api/) — The Weapon Parts API from GZW Data API — 2 operation(s) for weapon parts.
- [GZW Data API Weapons API](https://apis.io/apis/gzw-data/gzw-data-weapons-api/) — The Weapons API from GZW Data API — 4 operation(s) for weapons.
- [GZW Data API Workshop Supplies API](https://apis.io/apis/gzw-data/gzw-data-workshop-supplies-api/) — The Workshop Supplies API from GZW Data API — 4 operation(s) for workshop supplies.
- [GZW Data API Changes API](https://apis.io/apis/gzw-data/gzw-data-changes-api/) — The Changes API from GZW Data API — 2 operation(s) for changes.
- [GZW Data API Schema API](https://apis.io/apis/gzw-data/gzw-data-schema-api/) — The Schema API from GZW Data API — 2 operation(s) for schema.
- [GZW Data API Search API](https://apis.io/apis/gzw-data/gzw-data-search-api/) — The Search API from GZW Data API — 2 operation(s) for search.
- [GZW Data API Version API](https://apis.io/apis/gzw-data/gzw-data-version-api/) — The Version API from GZW Data API — 2 operation(s) for version.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [gzw-data-mcp.yml](https://apis.io/servers/gzw-data/gzw-data-mcp-yml/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Gzw Data Agentic Access](https://apis.io/agentic-access/gzw-data/gzw-data-agentic-access/)

#### JSON Schema (92)

The data models the API reads and writes.

- [ApiError](https://apis.io/schemas/gzw-data/gzw-data-ApiError/)
- [ApiErrorResponse](https://apis.io/schemas/gzw-data/gzw-data-ApiErrorResponse/)
- [Capabilities](https://apis.io/schemas/gzw-data/gzw-data-Capabilities/)
- [MetadataResponse](https://apis.io/schemas/gzw-data/gzw-data-MetadataResponse/)
- [ObjectResponse](https://apis.io/schemas/gzw-data/gzw-data-ObjectResponse/)
- [PaginatedResponse](https://apis.io/schemas/gzw-data/gzw-data-PaginatedResponse/)
- [RecordResponse](https://apis.io/schemas/gzw-data/gzw-data-RecordResponse/)
- [ammo](https://apis.io/schemas/gzw-data/gzw-data-ammo/)
- [apparel_items](https://apis.io/schemas/gzw-data/gzw-data-apparel-items/)
- [auxiliary](https://apis.io/schemas/gzw-data/gzw-data-auxiliary/)
- [backpacks](https://apis.io/schemas/gzw-data/gzw-data-backpacks/)
- [barrels](https://apis.io/schemas/gzw-data/gzw-data-barrels/)
- [belts](https://apis.io/schemas/gzw-data/gzw-data-belts/)
- [binoculars](https://apis.io/schemas/gzw-data/gzw-data-binoculars/)
- [boots](https://apis.io/schemas/gzw-data/gzw-data-boots/)
- [buffer_tubes](https://apis.io/schemas/gzw-data/gzw-data-buffer-tubes/)
- [charging_handle](https://apis.io/schemas/gzw-data/gzw-data-charging-handle/)
- [cleanup](https://apis.io/schemas/gzw-data/gzw-data-cleanup/)
- [collimators](https://apis.io/schemas/gzw-data/gzw-data-collimators/)
- [containers](https://apis.io/schemas/gzw-data/gzw-data-containers/)
- [contract](https://apis.io/schemas/gzw-data/gzw-data-contract/)
- [contracts](https://apis.io/schemas/gzw-data/gzw-data-contracts/)
- [drinks](https://apis.io/schemas/gzw-data/gzw-data-drinks/)
- [electronics](https://apis.io/schemas/gzw-data/gzw-data-electronics/)
- [face_cover](https://apis.io/schemas/gzw-data/gzw-data-face-cover/)
- …and 67 more published on APIs.io

#### Examples (12)

Example requests and responses.

- [Gzw Data Changes Response](https://apis.io/examples/gzw-data/gzw-data-changes-response/)
- [Gzw Data Error Endpoint Not Found](https://apis.io/examples/gzw-data/gzw-data-error-endpoint-not-found/)
- [Gzw Data Error Record Not Found](https://apis.io/examples/gzw-data/gzw-data-error-record-not-found/)
- [Gzw Data Health Response](https://apis.io/examples/gzw-data/gzw-data-health-response/)
- [Gzw Data Item Context Response](https://apis.io/examples/gzw-data/gzw-data-item-context-response/)
- [Gzw Data Metadata Registry Response](https://apis.io/examples/gzw-data/gzw-data-metadata-registry-response/)
- [Gzw Data Paginated Response](https://apis.io/examples/gzw-data/gzw-data-paginated-response/)
- [Gzw Data Record Response](https://apis.io/examples/gzw-data/gzw-data-record-response/)
- [Gzw Data Schema Vendors Response](https://apis.io/examples/gzw-data/gzw-data-schema-vendors-response/)
- [Gzw Data Schema Weapons Response](https://apis.io/examples/gzw-data/gzw-data-schema-weapons-response/)
- [Gzw Data Search Response](https://apis.io/examples/gzw-data/gzw-data-search-response/)
- [Gzw Data Version Response](https://apis.io/examples/gzw-data/gzw-data-version-response/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Gzw Data Openapi Overlay](https://apis.io/overlays/gzw-data/gzw-data-openapi-overlay/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [GZW Data API — spectral rules](https://apis.io/rules/gzw-data/gzw-data-spectral/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Gzw Data Authentication](https://apis.io/security/gzw-data/gzw-data-authentication/)
- [Gzw Data Domain Security](https://apis.io/security/gzw-data/gzw-data-domain-security/)
- [Gzw Data Vulnerability Disclosure](https://apis.io/security/gzw-data/gzw-data-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Gzw Data Plans Pricing](https://apis.io/plans/gzw-data/gzw-data-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Gzw Data Rate Limits](https://apis.io/rate-limits/gzw-data/gzw-data-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://gzw-data.dev/)
- [Documentation](https://gzw-data.dev/docs/)
- [Getting started](https://gzw-data.dev/docs/#quickstart)
- [API reference](https://gzw-data.dev/docs/)
- [Pricing](https://gzw-data.dev/docs/)
- [Support](https://github.com/ZoniBoy00/gzw-data/issues)
- [Security](https://github.com/ZoniBoy00/gzw-data/blob/main/SECURITY.md)
- [Terms of service](https://gzw-data.dev/terms-of-service/)
- [Privacy policy](https://gzw-data.dev/privacy-policy/)
- [GitHub](https://github.com/ZoniBoy00)

## API Evangelist rating

**Kin Score 56.0** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 83.9 |
| Contract quality | 44.8 |
| Contract governance | 22.0 |
| Operational transparency | 55.3 |
| Developer ergonomics | 67.3 |
| Access clarity | 52.6 |

**Agent readiness 34.1** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | na |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | na |
| Error Semantics | verified |
| OpenAPI Examples | documented (partial credit) |
| Rate Limit Signal | verified |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | na |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | — |

**Regulatory alignment 30.4** — Government & Public Sector

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/gzw-data/](https://apis.io/providers/gzw-data/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for GZW Data API: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/gzw-data/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
