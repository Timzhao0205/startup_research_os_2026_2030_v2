# Search Query Bank

Use these patterns when Claude needs domain-targeted searches.

## General patterns

```text
site:ieeexplore.ieee.org [topic] [application] 2024 OR 2025 OR 2026
site:spectrum.ieee.org [topic] startup industrial application
site:nature.com [topic] review 2024 2025
site:science.org [topic] energy electronics robotics biomedical
site:energy.gov [topic] funding roadmap program
site:arpa-e.energy.gov [topic] OPEN SCALEUP program
site:iea.org [topic] technology roadmap market report
site:nist.gov [topic] semiconductor AI standards measurement
site:bis.gov [topic] export controls China semiconductor AI rule
site:fda.gov [device type] guidance medical device AI software
site:nmpa.gov.cn [device type] regulation guidance China
site:miit.gov.cn [technology] policy industrial plan
site:ndrc.gov.cn [energy technology] policy China
site:semi.org [semiconductor topic] market report supply chain
site:semiconductors.org [topic] policy industry report
site:ferc.gov [grid topic] rule interconnection reliability
site:nerc.com [grid reliability topic]
```

## Gap-fill query template

```text
Find 10 Tier 1 or Tier 2 sources from whitelist domains for [topic]. Exclude company marketing and low-quality aggregator sites. For each source, provide source title, URL, source type, source tier, publication date, claim supported, and limitations.
```
