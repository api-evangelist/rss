# RSS (rss)

RSS (Really Simple Syndication) is the canonical XML feed format family for publishing and subscribing to streams of frequently updated content — blogs, news, podcasts, and other periodic resources. This API Evangelist index profiles the RSS family as a content syndication standard, covering RSS 2.0 (stewarded by the RSS Advisory Board), Atom 1.0 (IETF RFC 4287), JSON Feed 1.1, the RSS Best Practices Profile, OPML 2.0 for feed subscription lists, and the HTML autodiscovery conventions used by feed readers to locate feeds.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/rss/refs/heads/main/apis.yml)

## Scope

- **Type:** Index (Standard)
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Syndication, RSS, Atom, JSON Feed, OPML, Content, XML, Specification, Standard

## Timestamps

- **Created:** 2025-01-01
- **Modified:** 2026-05-23

## APIs (Specifications)

### RSS 2.0

The dominant XML-based syndication format, stewarded by the RSS Advisory Board. A feed has a root `<rss version="2.0">` wrapping a single `<channel>` with required `title`, `link`, and `description`, plus a sequence of `<item>` elements. The spec is intentionally frozen; extensions happen through XML namespaces. The Advisory Board states: *"The RSS spec is, for all practical purposes, frozen at version 2.0.1."*

**Human URL:** [https://www.rssboard.org/rss-specification](https://www.rssboard.org/rss-specification)

#### Tags

- RSS, Syndication, XML, Specification

#### Properties

- [Specification](https://www.rssboard.org/rss-specification)
- [Best Practices Profile](https://www.rssboard.org/rss-profile)
- [Validator](https://www.rssboard.org/rss-validator/)
- [Autodiscovery](https://www.rssboard.org/rss-autodiscovery)
- [JSON Schema — Channel](json-schema/rss-channel-schema.json)
- [JSON Schema — Item](json-schema/rss-item-schema.json)
- [JSON Structure — Channel](json-structure/rss-channel-structure.json)
- [Example — Channel](examples/rss-channel-example.json)
- [Example — Item](examples/rss-item-example.json)

### Atom 1.0

Defined by IETF RFC 4287, Atom 1.0 is the more rigorously specified XML alternative to RSS 2.0. An `atom:feed` contains required `atom:id`, `atom:title`, `atom:updated`, and `atom:author` plus a sequence of `atom:entry` items each with their own `id`, `title`, `updated`, and `content` or `summary`. Uses the namespace `http://www.w3.org/2005/Atom` and media type `application/atom+xml`.

**Human URL:** [https://datatracker.ietf.org/doc/html/rfc4287](https://datatracker.ietf.org/doc/html/rfc4287)

#### Tags

- Atom, Syndication, IETF, XML, Specification

#### Properties

- [Specification (RFC 4287)](https://datatracker.ietf.org/doc/html/rfc4287)
- [JSON Schema — Feed](json-schema/atom-feed-schema.json)
- [JSON Schema — Entry](json-schema/atom-entry-schema.json)
- [Example — Feed](examples/atom-feed-example.json)

### JSON Feed 1.1

Brent Simmons and Manton Reece's JSON-based syndication format, intended as a developer-friendly alternative to RSS and Atom. A feed has top-level `version`, `title`, and `items`; each item has a required `id` and at least one of `content_html` or `content_text`. Served with `application/feed+json`. The spec captures its motivation plainly: *"For most developers, JSON is far easier to read and write than XML."*

**Human URL:** [https://www.jsonfeed.org/version/1.1/](https://www.jsonfeed.org/version/1.1/)

#### Tags

- JSON Feed, Syndication, JSON, Specification

#### Properties

- [Specification](https://www.jsonfeed.org/version/1.1/)
- [JSON Schema — Feed](json-schema/json-feed-schema.json)
- [JSON Schema — Item](json-schema/json-feed-item-schema.json)
- [Example — Feed](examples/json-feed-example.json)

### RSS Best Practices Profile

The RSS Advisory Board's normative guidance on producing RSS feeds that interoperate cleanly across the diverse population of feed readers. Covers character data, date formats, email addresses, URLs, element-by-element recommendations, and common namespace extensions. From the profile itself: *"This profile is a set of recommendations for how to create RSS documents that work best in the wide and diverse audience of client software that supports the format."*

**Human URL:** [https://www.rssboard.org/rss-profile](https://www.rssboard.org/rss-profile)

#### Tags

- RSS, Best Practices, Profile, Interoperability

#### Properties

- [Documentation](https://www.rssboard.org/rss-profile)
- [Vocabulary](vocabulary/rss-vocabulary.yml)

### OPML 2.0

Outline Processor Markup Language — an XML format whose most common application is exchanging lists of RSS/Atom/JSON Feed subscriptions between feed readers. A subscription-list OPML has a `body` of `outline` elements with `type="rss"`, `text`, `xmlUrl` (the feed URL), and `htmlUrl` (the human-readable site URL). OPML is the de facto portable format for feed-reader import/export.

**Human URL:** [http://opml.org/spec2.opml](http://opml.org/spec2.opml)

#### Tags

- OPML, Outline, Subscription, Syndication, XML

#### Properties

- [Specification](http://opml.org/spec2.opml)
- [JSON Schema — Subscription List](json-schema/opml-subscription-list-schema.json)
- [Example — Subscription List](examples/opml-subscription-list-example.json)

### Feed Autodiscovery

The HTML convention by which a web page advertises the location of its RSS, Atom, or JSON Feed via a `<link rel="alternate" type="application/rss+xml" href="...">` element in the document head. Feed readers, browsers, and crawlers look for this element to discover feeds from a homepage URL alone. The RSS Advisory Board spec notes: *"The rel attribute must have a value of 'alternate', a keyword that indicates the link is an alternate version of the site's main content."*

**Human URL:** [https://www.rssboard.org/rss-autodiscovery](https://www.rssboard.org/rss-autodiscovery)

#### Tags

- Autodiscovery, HTML, Syndication, Discovery

#### Properties

- [Documentation](https://www.rssboard.org/rss-autodiscovery)
- [Example](examples/feed-autodiscovery-example.json)

## Artifacts

| Type | Location | Count |
|------|----------|-------|
| JSON Schema | `json-schema/` | 6 |
| JSON Structure | `json-structure/` | 1 |
| JSON-LD Context | `json-ld/rss-context.jsonld` | 1 |
| Examples | `examples/` | 6 |
| Vocabulary | `vocabulary/rss-vocabulary.yml` | 1 |

## Common Properties

| Property | URL |
|----------|-----|
| Website | https://www.rssboard.org/ |
| Documentation | https://www.rssboard.org/rss-specification |
| Best Practices | https://www.rssboard.org/rss-profile |
| Validator | https://www.rssboard.org/rss-validator/ |
| Blog | https://www.rssboard.org/news |
| Atom Specification | https://datatracker.ietf.org/doc/html/rfc4287 |
| JSON Feed Specification | https://www.jsonfeed.org/version/1.1/ |
| OPML Specification | http://opml.org/spec2.opml |
| JSON-LD Context | [json-ld/rss-context.jsonld](json-ld/rss-context.jsonld) |
| Vocabulary | [vocabulary/rss-vocabulary.yml](vocabulary/rss-vocabulary.yml) |

## Notes

- **Stewardship.** RSS 2.0 is stewarded by the [RSS Advisory Board](https://www.rssboard.org/), a non-profit working group. Atom is an IETF standard (RFC 4287). JSON Feed is maintained by its co-authors. OPML 2.0 is published at opml.org.
- **Frozen but extensible.** RSS 2.0 is intentionally frozen at 2.0.1/2.0.11; all evolution happens through XML namespace extensions (Media RSS, iTunes podcast namespace, Dublin Core, the Atom namespace embedded in RSS, the WebSub Hub link relation).
- **No upstream GitHub org.** There is no `github.com/rssboard` organization; the spec, profile, and validator are hosted directly at rssboard.org. The Atom spec lives in the IETF datatracker. JSON Feed lives at jsonfeed.org.
- **No commercial surface.** As a standards family there is no pricing, rate-limits, or FinOps profile — those pipeline steps are intentionally skipped for `x-type: standard` repos.

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
