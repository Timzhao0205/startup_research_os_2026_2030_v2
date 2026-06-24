<task>
Audit the sources and citations in the previous scoring answer.
</task>

<audit_rules>
For each cited source, classify:
- domain;
- source tier;
- source type;
- claim supported;
- whether it directly supports the claim;
- whether it is primary or secondary;
- whether it is a company claim;
- whether it is outdated;
- whether it should be replaced by a better source.
</audit_rules>

<deliverable>
Produce:
1. Source audit table.
2. Ideas whose score depends on weak sources.
3. Ideas whose score should be reduced.
4. Ideas needing better technical evidence.
5. Ideas needing better customer-pain evidence.
6. Ideas needing better China/US policy evidence.
7. CSV-ready rows for `source_evidence_ledger.csv`.
8. Revised confidence ratings.
</deliverable>

<rules>
Be strict. Do not defend weak citations. Do not preserve unsupported claims.
</rules>
