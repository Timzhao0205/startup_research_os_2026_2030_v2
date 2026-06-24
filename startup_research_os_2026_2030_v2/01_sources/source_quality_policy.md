# Source Quality Policy

## Tier 1 — highest priority

Use for technical facts, regulations, standards, public policy, government programs, national-lab results, public data, and mature market structure.

Acceptable Tier 1 source types:

- peer-reviewed papers and conferences;
- official standards bodies;
- official government and regulator pages;
- national labs;
- international agencies;
- industry associations with transparent methodology;
- public filings;
- procurement documents;
- official statistical databases.

Examples:
IEEE Xplore, IEEE Spectrum, ACM Digital Library, Nature, Science, Cell, AIP, APS, IOP, SPIE, Optica, ACS, RSC, NIST, DOE, ARPA-E, EIA, IEA, IRENA, BIS, FDA, NIH, NMPA, MIIT, NDRC, SAMR, SAC, SEMI, SIA, WSTS, IEC, ISO, UL, ASTM, SAE, JEDEC, IPC, FERC, NERC.

## Tier 2 — strong analysis and triangulation

Use for policy interpretation, strategy, geopolitics, industry structure, technology strategy, and synthesis.

Examples:
CSET, RAND, CSIS, Brookings, MERICS, Rhodium Group, ITIF, CNAS, CFR, Belfer Center, Stanford HAI, Columbia Center on Global Energy Policy, National Academies, OECD, WEF.

## Tier 3 — market and journalism triangulation

Use for market timing, company movement, funding, acquisitions, industry narratives, technical media, and weak demand signals.

Examples:
Reuters, AP, Financial Times, Wall Street Journal, Bloomberg, MIT Technology Review, The Information, Wired, Ars Technica, Nikkei, SCMP, Caixin, SemiEngineering, EE Times, DigiTimes, TechInsights, Yole Group, IDTechEx, Omdia, PitchBook, CB Insights, Crunchbase, Dealroom.

## Tier 4 — weak signal only

Use for startup discovery, local Chinese market signals, customer anecdotes, and hypothesis generation only.

Examples:
36Kr, EqualOcean, ITjuzi, Qichacha, Tianyancha, Cyzone, Pedaily, Leiphone, Jiqizhixin, OFweek, forums, social media, blogs.

## Hard rules

- Tier 4 sources do not count toward the 300-source strategy corpus.
- No top-ranked idea may rely only on Tier 3 sources.
- No major factual claim should rely only on a company marketing page.
- Company pages must be labeled as company claims.
- Market reports are triangulation, not proof.
- If source quality is weak, explicitly lower confidence.
- Always distinguish facts, inference, and speculation.
- Always log useful sources into `source_evidence_ledger.csv`.

## Source qualification checklist

A source counts toward the 300-source strategy corpus only if:

1. It is unique by URL/DOI/title.
2. It is Tier 1, Tier 2, or approved Tier 3.
3. It directly supports at least one claim.
4. Claude can extract enough substance to summarize the claim.
5. The evidence ledger row includes domain, tier, source type, claim supported, confidence, and limitations.
6. It is not merely a search-result snippet.
7. It is not a duplicate, press-release mirror, scraper page, or SEO content.
