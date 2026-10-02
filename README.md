# Fast GST Refund MCP

Five free, read-only MCP tools for Indian service-export GST refund preparation.

Connect to **https://fastgstrefund.com/mcp** using Streamable HTTP. No account,
API key or payment is required for the current tools.

| Tool                       | What it does                                               |
| -------------------------- | ---------------------------------------------------------- |
| `get_refund_checklist`     | Builds a preparation checklist.                            |
| `search_refund_guides`     | Finds relevant public preparation guides.                  |
| `read_refund_guide`        | Retrieves a public guide with its source links.            |
| `explain_upload_error`     | Explains common Statement 3 and Annexure B upload issues.  |
| `check_receipt_allocation` | Checks anonymous invoice-to-receipt allocation arithmetic. |

[Connection instructions and scope](https://fastgstrefund.com/for-agents/) ·
[Preparation guides](https://fastgstrefund.com/guides/) ·
[llms.txt](https://fastgstrefund.com/llms.txt)

The current tools provide guidance and bounded arithmetic. They do not retrieve
taxpayer accounts, file government applications, or generate complete Statement 3
and Annexure B upload JSON files. Keep taxpayer identifiers, credentials and source
documents local. Allocation checks accept anonymous row references and integer INR
paise amounts.

## Registry and updates

Official MCP Registry identity: `com.fastgstrefund/fast-gst-refund`.
The published initial version is `1.0.0`. The remote endpoint remains the connection
address; clients discover available tools through MCP `tools/list`.

This repository contains public connection documentation and registry metadata for
the hosted service. The server implementation is proprietary and is not distributed
here. No open-source license is granted for the server implementation.

New capabilities are documented after release. Check this repository's changelog and
the connection guide when a release changes tools, authentication or pricing.

## Support

[Support](https://fastgstrefund.com/support/) ·
[Privacy](https://fastgstrefund.com/privacy/) ·
[Terms](https://fastgstrefund.com/terms/)

Public listing corrections: support@fastgstrefund.com.
