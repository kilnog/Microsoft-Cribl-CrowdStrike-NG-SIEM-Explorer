# Microsoft -> Cribl -> CrowdStrike NG SIEM Explorer

**An interactive reference tool for planning and operationalising Microsoft security log ingestion into CrowdStrike Falcon Next-Gen SIEM via Cribl Stream.**

---

## What It Does

This single-file HTML tool helps security engineers and architects understand, plan, and document the end-to-end data pipeline for getting Microsoft security logs from their origin into CrowdStrike Falcon NG SIEM using Cribl Stream as the data pipeline layer.

It covers the full stack:

```
Microsoft Source → Azure Transport → Cribl Stream → CrowdStrike NG SIEM
```

---

## Features

### 🔷 Pipeline Explorer
Select any Microsoft data source from the sidebar to see:
- A description of the log source and what it captures
- An animated end-to-end flow diagram showing each entity in the pipeline
- CrowdStrike NG SIEM parser name and ingestion status
- Numbered configuration steps for Microsoft, Cribl, and CrowdStrike — each with reference links

### 📊 Pipeline Matrix
A sortable, filterable table of all supported Microsoft sources showing:
- Log collection method (Azure Event Hub, API Pull, WEF/File Monitor)
- Cribl ingest/collect method
- CrowdStrike NG SIEM connector type (Cribl: HEC)
- NG SIEM parser name
- Supported parser status

### 📋 Build Run Sheet
Select the sources you want to onboard and generate a step-by-step operational run sheet with numbered actions and reference links for each source. Exportable as a standalone HTML file for team distribution or printing.

### 📚 Resources & Best Practices
Curated best practice guidance and direct documentation links covering:
- Azure Event Hub design principles
- Cribl Stream pipeline configuration
- CrowdStrike NG SIEM connector and parser setup
- O365 API pull source considerations

---

## Data Sources Covered

| Group | Sources |
|---|---|
| M365 / Office 365 | Defender for Office 365, Defender XDR Events, M365 Unified Audit Log, MessageTrace |
| Azure Identity | Azure Entra ID, Defender for Identity |
| Azure Platform | Azure Key Vault, Azure Activity Log, Azure Firewall |
| Windows Endpoint | Microsoft IIS, Microsoft SQL Audit |

More sources can be added by extending the `SOURCES` array in the JavaScript data block.

---

## The .html Explorer Tool

- Pure single file HTML/CSS/JavaScript — zero dependencies, zero build tooling
- Fonts loaded from Google Fonts (Inter + JetBrains Mono) — requires internet access for full rendering; falls back to system fonts offline
- All data is embedded in the file — no API calls, no telemetry, no tracking

---

## Disclaimer

> This tool was developed AI-assisted (Claud) and provided for informational reference only.
> Content is derived from publicly available documentation from Microsoft, Cribl, and CrowdStrike.
> It may be incomplete, inaccurate, or out of date.
> This is not official guidance from any of the named vendors.
> Always verify configurations against current official documentation before implementation.
> No liability is accepted for decisions made based on this content.

**Official documentation sources:**
- Cribl Stream docs: [docs.cribl.io/stream](https://docs.cribl.io/stream/)
- Microsoft Learn: [learn.microsoft.com](https://learn.microsoft.com)
- CrowdStrike Tech Hub: [crowdstrike.com/tech-hub](https://www.crowdstrike.com/tech-hub/)

---

## License

MIT License — applies to the tool's original source code, UI structure, and curation logic.

Embedded documentation content (configuration steps, parser names, product descriptions) is derived from publicly available documentation from Microsoft, Cribl, and CrowdStrike. That content remains the property of the respective owners and is subject to their own terms of use. See [LICENSE](./LICENSE) for the full notice.
