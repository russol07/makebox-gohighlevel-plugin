---
name: makebox-ghl-setup
description: Help an owner connect a GoHighLevel or LeadConnector white-label sub-account to MakeBox MCP using its own Private Integration Token and location ID.
---

Use when a user wants to connect a location or asks where to obtain the token. Do not request or receive a token, password or OAuth code in chat. A workspace owner or admin should:

1. Sign in at https://mcp.makebox.ai/account/; create or select the correct workspace. An existing team member should accept the organization's invitation and sign in individually. The owner chooses whether the organization pays for the team seat or the member pays for that seat; a separate workspace requires its own subscription. Server-side entitlement and location limits control access.
2. In the target GoHighLevel sub-account (which may have an agency's white-label brand), locate the Location ID under Settings > Business Profile. In that same sub-account open Settings > Private Integrations > Create New Integration. If missing, an agency administrator may need to enable the feature for that sub-account and grant permission to manage it. Do not change unrelated settings.
3. Name the integration, select only scopes needed for the intended work, generate and securely copy its **sub-account** Private Integration Token (PIT). A legacy API key, agency token or another location's token is not interchangeable with the location PIT. Official guide: https://help.gohighlevel.com/support/solutions/articles/155000003054-private-integrations-everything-you-need-to-know . Tokens can be shown once; never post them in chat, files or public URLs.
4. In MakeBox select that workspace, find Locations, enter the Location ID and paste the PIT into Private integration token, then choose Connect location. The server verifies that the token matches the location. Once connected, team members do not need separate copies of the token. Use https://mcp.makebox.ai/ghl/mcp as the MCP URL, authenticate with the individual's MakeBox account and select the intended location. Verify with the actual `get_location_summary` tool.

HighLevel, LeadConnector and compatible agency white-label instances share the underlying platform, but compatibility depends on agency feature settings, token scopes, the location's product plan and endpoint eligibility. Do not claim every agency, token, endpoint or feature was tested. Agency-wide tokens and location plans have distinct restrictions. Users of white-label accounts who cannot see Private Integrations should contact their agency administrator.

For Workflow API beta access, read the makebox-ghl-workflows skill. Hosted CRM writes may be disabled even if the provider grants workflow scopes or beta access.

For current plan prices and billing, use https://mcp.makebox.ai/account/about.html#pricing. Paid plans are $19/month for one location or $29/month for one agency, plus $9/month per additional team member; applicable tax is added. Friends grants can be free. The owner may pay for a seat or the invited member may pay for their own seat. Do not suggest that a team seat creates a separate organization.
