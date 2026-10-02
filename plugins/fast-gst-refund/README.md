# Fast GST Refund

Five free MCP tools for Indian service-export GST refund preparation, with a
usage skill for choosing the right preparation step. Version: **1.0.0**.

## Tools

| Tool                       | Purpose                                                   |
| -------------------------- | --------------------------------------------------------- |
| `get_refund_checklist`     | Prepare a checklist for the current filing stage.         |
| `search_refund_guides`     | Find public preparation guides.                           |
| `read_refund_guide`        | Read a guide with source links and source-check dates.    |
| `explain_upload_error`     | Understand Statement 3 and Annexure B upload issues.      |
| `check_receipt_allocation` | Check anonymous invoice-to-receipt allocation arithmetic. |

Try: “Build my Statement 3 preparation checklist”, “Explain an Annexure B
duplicate-document issue”, or “Check these anonymous invoice-to-receipt
allocations”. The skill explains the supported inputs and how to cite guidance.

These tools do not generate the complete Statement 3 or Annexure B upload JSONs,
retrieve taxpayer accounts, file government applications, collect payments or
promise refund eligibility. No account, API key or subscription is needed for
the current five tools.

## Connection and package contents

The only tool endpoint is **https://fastgstrefund.com/mcp**, using Streamable HTTP.
The `.mcp.json` file declares it as `type: "http"` for compatible bundle clients.
The `.grok-plugin/plugin.json` manifest is for Grok Build. The
`.claude-plugin/plugin.json` compatibility marker allows OpenClaw to recognize
the skill/MCP bundle; it is a file format, not a Claude directory listing.
`openclaw.plugin.json` and `package.json` supply ClawHub catalog metadata.

Install this directory through a compatible client's local plugin installer,
or use the marketplace entry when approved. For OpenClaw, run
`openclaw plugins install ./plugins/fast-gst-refund` from a checkout of this
public repository, then inspect with `openclaw plugins inspect fast-gst-refund`.
The package provides one skill and one remote MCP connection. It has no hooks,
local executable code, install scripts, runtime dependencies or required secrets.
Use a client version that reports both skill and MCP capabilities for the bundle.
[Direct MCP setup](https://fastgstrefund.com/for-agents/) is also available.

## Data and permissions

The client sends a request to `fastgstrefund.com` only to perform the requested
tool operation. Reading returned source links may involve the cited public
websites. No other service endpoint is configured in this package.

Keep GSTINs, PANs, names, invoice numbers, bank details, credentials and document
contents local. Allocation tools accept only anonymous row references and
integer INR paise. A passed arithmetic check is not a tax-eligibility decision.

The hosted service records limited operational events, including tool names,
outcomes and timing, but excludes arguments and results. It uses random request
IDs, not persistent user identities. To disable these events, add
`"headers": {"X-GST-Analytics": "off"}` to the server entry. This package does not
set a client-attribution header. See the [privacy page](https://fastgstrefund.com/privacy/).

## Updates, ownership and support

The package is maintained by Fast GST Refund (Xeloni Zarakas Private Limited)
through the owner's GitHub account, `syllogismos`. The public distribution
repository contains no hosted implementation or taxpayer records.

Package updates use a new version. Grok catalog updates pin a new commit SHA;
ClawHub releases are published separately. The stable remote endpoint can serve
updated tools independently of the installed package. Check the
[connection guide](https://fastgstrefund.com/for-agents/) for changes to tools,
authentication or pricing.

The [connector distribution licence](LICENSE) permits installation, use and
unmodified redistribution of this package. The hosted implementation remains
proprietary; it is not included or open-sourced by this package.

[Support](https://fastgstrefund.com/support/) ·
[Privacy](https://fastgstrefund.com/privacy/) ·
[Terms](https://fastgstrefund.com/terms/)

Contact: support@fastgstrefund.com.
