# CS4 MintsLoader Infrastructure and IOC Provenance

This package contains a publication-ready case study on the relationship between the June 2026 Operation GhostWallet intrusion and known MintsLoader tradecraft, together with an IOC provenance review of the September 2026 CERT-AGID campaign.

## Main conclusion

The June chain is technically consistent with MintsLoader, but the public record does not preserve the remote stage needed for a family-level attribution. It is therefore classified as a moderate-confidence correlation. The strongest original result is the provenance analysis of `pesterbdd.com/images/Pester.png`: the URL is historical Pester package metadata and should be reviewed as likely environmental noise rather than treated as attacker infrastructure without additional evidence.

## Contents

- `report/CS4-MintsLoader-Infrastructure.docx` - editable paper
- `report/CS4-MintsLoader-Infrastructure.pdf` - publication copy
- `report/CS4-MintsLoader-Infrastructure.md` - GitHub version
- `iocs/confirmed.csv` - directly supported campaign indicators
- `iocs/correlations.csv` - analytical relationships and confidence
- `iocs/excluded-or-noisy.csv` - indicators requiring exclusion or review
- `methodology/methodology.md` - evidence and confidence model
- `evidence/public-source-references.md` - source register
- `disclosure/CERT-AGID-technical-note-it.md` - disclosure note ready for review
- `editorial/editorial-abstract-it.md` - Italian editorial abstract and safe headline

## Publication language

Use the following wording for the June finding:

> The June 2026 GhostWallet delivery chain is technically consistent with MintsLoader tradecraft. The available public evidence does not preserve the remote stage required for a definitive family attribution, so we assess the relationship with moderate confidence.

Use the following wording for the Pester finding:

> Historical package records and independent sandbox evidence show that `pesterbdd.com/images/Pester.png` was used as the icon URL in legitimate Pester module metadata. Its appearance in a malware IOC export is therefore insufficient to identify attacker-controlled infrastructure and warrants provenance review.

## Disclosure recommendation

Share the evidence matrix and the two bounded findings with CERT-AGID before broad publication. Do not characterize the Pester entry as an error. Request confirmation of how the URL was collected and whether it came from a runtime connection, a memory string, or an automated extraction stage.
