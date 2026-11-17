# MakeBox for GoHighLevel

Connect an authorized GoHighLevel or compatible LeadConnector white-label workspace to Codex or Claude Code through the shared MakeBox MCP server: https://mcp.makebox.ai/ghl/mcp. Sign in and manage workspaces at https://mcp.makebox.ai/account/. The owner connects the CRM credentials; each member uses their own MakeBox identity and selected workspace. Do not put private tokens, passwords or OAuth codes in chat.

## Current availability

The hosted connector exposes registered read and write operations according to subscription access, member permissions and provider scopes. Not every documented operation has been individually verified; some provider features require separate approval. The catalog is not proof that every provider operation works. Access depends on the selected organization, location, subscription, member permissions, scopes and account features.

## Plans

Location: $19/month for one location and owner. Agency: $29/month for one agency and its locations. Additional team member: $9/month per workspace, paid by the organization or that member. Applicable tax is added. Pricing and terms: https://mcp.makebox.ai/account/about.html#pricing and https://mcp.makebox.ai/account/terms-ghl.html.

## Connect a location

In the target location, copy the Location ID from Settings > Business Profile. Create a location-level Private Integration Token in Settings > Private Integrations; ask your agency administrator if that menu is unavailable. Enter the ID and token in the MakeBox account. A team member accepts an invitation and does not need a copy of the token. HighLevel guide: https://help.gohighlevel.com/support/solutions/articles/155000003054-private-integrations-everything-you-need-to-know.

For an agency, first connect its agency ID and agency-level token, then connect each location with its own location-level token. Authenticated members select the organization and authorized location during MCP authorization.

## Workflow API

Extended Workflow API access is approved by HighLevel per location. See https://help.leadconnectorhq.com/support/solutions/articles/155000009503-workflows-api-%E2%80%93-create-publish-and-monitor-workflows-by-api and its application form https://link.apisystem.tech/widget/form/qqPIi8Ue6zdqIaHb2cXE. Approval, token scopes, subscription access and the relevant user permissions are all required.

## Install and connect

For Claude Code, load this directory for a session with `claude --plugin-dir /absolute/path/to/makebox-ghl-plugin-0.3.2`, then use `/mcp` to authenticate. For Codex, use a supported plugin source or import and authenticate the remote MCP connection. The MakeBox account displays current setup commands. Each client user signs in individually.

Product: https://mcp.makebox.ai/account/about.html
Support: https://mcp.makebox.ai/account/support-ghl.html
Privacy: https://mcp.makebox.ai/account/privacy-ghl.html
Terms: https://mcp.makebox.ai/account/terms-ghl.html

MakeBox is independent and is not endorsed by HighLevel. Compatibility and feature availability depend on the underlying agency and provider settings.

## Claude Code marketplace

Add the MakeBox marketplace with `claude plugin marketplace add russol07/makebox-gohighlevel-plugin`, then install with `claude plugin install makebox-for-gohighlevel@makebox-crm-plugins`. Restart Claude Code and authenticate the MCP connection. A public directory submission is separate from this repository-based installation.

## Codex marketplace

Add `russol07/makebox-gohighlevel-plugin` as a plugin marketplace in Codex, then install `makebox-for-gohighlevel@makebox-crm-plugins`. Authenticate to the shared MCP endpoint when prompted. This repository-based install is separate from public directory review.
