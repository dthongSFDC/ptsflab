# Knowledge Folder Setup (Demo Orgfarm)

This project is pre-seeded for:
- Experience Cloud
- Sales Cloud (closest available shared doc is Sales Einstein guidance)
- Service Cloud

## What is already added
- `experience_cloud_4-2-2026.md`
- `sales_einstein_implementation_guide.md`
- `service_cloud_3-27-2026.md`
- `.toc.md` (index table of contents)
- `.search-index.json` (search index)

## What to add next for stronger Sales Cloud coverage
Add one or more core Sales Cloud guides to this folder, then re-index:
- Sales Cloud implementation guide
- Sales setup and administration guide
- Opportunity, lead, and forecasting process docs

## Re-index command
```bash
python3 "/Users/dthong/.claude/plugins/cache/scopezilla-dev/scopezilla-dev/1.18.1/scripts/index-knowledge.py" "/Users/dthong/Documents/Projects/PTSFLab"
```
