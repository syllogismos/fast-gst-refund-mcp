# Fast GST Refund MCP

Generate **Statement 3 and Annexure B JSON** for Indian service-export GST refund
preparation, without the GST offline Excel utilities. Eleven MCP tools check records,
create the files and provide cited preparation guidance.

Connect to **https://fastgstrefund.com/mcp** using Streamable HTTP.

| Tool                          | What it does                                                               |
| ----------------------------- | -------------------------------------------------------------------------- |
| `get_refund_checklist`        | Build a preparation checklist.                                             |
| `search_refund_guides`        | Find public preparation guidance.                                          |
| `read_refund_guide`           | Read a guide with sources and source-check dates.                          |
| `explain_upload_error`        | Explain Statement 3 and Annexure B upload issues.                          |
| `check_receipt_allocation`    | Check anonymous invoice-to-receipt allocation arithmetic.                  |
| `get_statement3_requirements` | List Statement 3 fields and the source records they need.                  |
| `validate_statement3`         | Check export invoices and bank-realisation records before generation.      |
| `generate_statement3`         | Create Statement 3 JSON from checked records.                              |
| `get_annexure_b_requirements` | List Annexure B fields and the source records they need.                   |
| `validate_annexure_b`         | Check purchase entries and reviewed ITC/reversal totals before generation. |
| `generate_annexure_b`         | Create Annexure B JSON from checked records.                               |

## Access and downloads

Guidance, requirements and record checks are free and need no account. Downloads
cost **₹499 + GST once per GSTIN and refund period**, including both files and
further downloads after you correct your entries.

Connect your Fast GST Refund account through OAuth for direct downloads when you
have access for that GSTIN and period. Otherwise, the generator returns a browser
link: open it, sign in by email and complete the download on the website. Both
files can share one link, which lasts 24 hours. Payment is completed by the user
on the website; the assistant cannot charge a card or access billing details.

The taxpayer reviews the records and uploads the generated files to the GST
portal. The service does not log into the GST portal or file applications.
Use only the validation and generation tools' documented fields with the taxpayer's permission.
Keep identifiers and source documents out of the five guidance/arithmetic tools.

[Connection instructions](https://fastgstrefund.com/for-agents/) ·
[JSON generator](https://fastgstrefund.com/tools/statement-3-annexure-b-json/) ·
[Preparation guides](https://fastgstrefund.com/guides/) ·
[llms.txt](https://fastgstrefund.com/llms.txt)

## Registry and updates

Official MCP Registry identity: `com.fastgstrefund/fast-gst-refund`.
The registry manifest in `server.json`, hosted server and connector bundle are
version `1.3.1`. Registry metadata and marketplace packages have separate
publication steps. Clients discover the
current remote tools through MCP `tools/list` at the stable endpoint.

This repository contains connection documentation, registry metadata and a
[connector bundle](plugins/fast-gst-refund/) for compatible Claude Code, Grok Build
and OpenClaw clients. The hosted implementation is proprietary and is not
included. The bundle has its own limited distribution licence in its LICENSE file.

Check the changelog and connection guide when tools, authentication or pricing
change. Installing a bundle locally does not require a directory listing.

## Support

[Support](https://fastgstrefund.com/support/) ·
[Privacy](https://fastgstrefund.com/privacy/) ·
[Terms](https://fastgstrefund.com/terms/)

Public listing corrections: support@fastgstrefund.com.
