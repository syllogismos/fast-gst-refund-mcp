# Fast GST Refund

Generate Statement 3 and Annexure B Indian GST refund JSON, check records and get cited
preparation guidance without the GST offline Excel utilities. Version: **1.3.1**.

## Tools

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

Try: “Help me check my Statement 3 entries and create the JSON”, “Tell me which
records Annexure B needs”, or “Check these anonymous invoice-to-receipt allocations”.
The included skill explains the requirements → validate → generate workflow.

Guidance and checks are free. Downloads cost **₹499 + GST once per GSTIN and
refund period**, including both files and further downloads after corrections.
With OAuth and access for that GSTIN and period, the generator returns the file
directly. Otherwise it gives a 24-hour browser link for signing in and completing
the download. The user handles payment on the website. The assistant does not
charge a card, retrieve billing details or log into the GST portal. The taxpayer
reviews and uploads the files themselves.

## Connection and package contents

The endpoint is **https://fastgstrefund.com/mcp**, using Streamable HTTP.
The `.mcp.json` file declares it as `type: "http"`. The package includes manifests
for Claude Code, Grok Build and OpenClaw, together with one usage skill and an icon.
There are no hooks, local executable code, install scripts, runtime dependencies
or required secrets.

Install this directory through a compatible client's plugin installer, or use
its marketplace entry when available. For OpenClaw, run
`openclaw plugins install ./plugins/fast-gst-refund` from a checkout of this public
repository, then inspect with `openclaw plugins inspect fast-gst-refund`.
Use a client that supports the bundle's skill and remote MCP connection.
[Direct MCP setup](https://fastgstrefund.com/for-agents/) is also available.

OAuth uses automatic client registration and the `refund:generate` scope.
Granting it permits generator/file access; it does not grant access to account
or billing APIs. Never put passwords, email sign-in codes or tokens in tool arguments.

## Data and permissions

Only the validation and generation tools accept their documented taxpayer fields, with the
user's permission. Validation stores no records. Browser handoffs and generated
files expire after 24 hours. Keep identifiers and source documents out of the
five guidance/arithmetic tools; allocation checks use anonymous row references
and integer INR paise. Arithmetic validity does not determine tax eligibility.

The configured tool endpoint is `fastgstrefund.com`. Reading citations may also
involve the linked public sources. Operational analytics exclude tool arguments,
results and taxpayer identity; random request IDs are not persistent user IDs.
To disable analytics, add `"headers": {"X-GST-Analytics": "off"}` to the MCP server
entry. This bundle does not set a client-attribution header. See the
[privacy page](https://fastgstrefund.com/privacy/).

## Updates, ownership and support

Maintained by Fast GST Refund, through the owner's
GitHub account, `syllogismos`. The public distribution repository contains no
hosted implementation or taxpayer records.

Package updates receive a new version. Marketplace records that pin a commit or
package version need their own update. Clients discover remote tool changes at
the stable endpoint. See the [connection guide](https://fastgstrefund.com/for-agents/)
for the current tools, authentication and pricing.

The [connector distribution licence](https://github.com/syllogismos/fast-gst-refund-mcp/blob/main/plugins/fast-gst-refund/LICENSE) permits installation, use and
unmodified redistribution of this bundle. The hosted implementation remains
proprietary and is not included.

[Support](https://fastgstrefund.com/support/) ·
[Privacy](https://fastgstrefund.com/privacy/) ·
[Terms](https://fastgstrefund.com/terms/)

Contact: support@fastgstrefund.com.
