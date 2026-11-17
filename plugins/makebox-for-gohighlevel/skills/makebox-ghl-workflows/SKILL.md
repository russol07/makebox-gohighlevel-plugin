---
name: makebox-ghl-workflows
description: Inspect GoHighLevel workflows, check extended Workflow API eligibility and guide an owner to the provider's beta request when required.
---

Verify the selected location. Use `list_workflows` for the list and `get_workflow_api_status` to check extended Workflow API availability. A successful list does not establish permission to create or edit definitions. `WORKFLOW_API_NOT_ENABLED_FOR_LOCATION` means this location is not enabled for the private beta; adding scopes or changing a subscription alone does not enroll it. Other errors can mean something else: do not automatically label every error as lack of beta access.

HighLevel's current official guide links its application form at https://link.apisystem.tech/widget/form/qqPIi8Ue6zdqIaHb2cXE . The guide is https://help.leadconnectorhq.com/support/solutions/articles/155000009503-workflows-api-%E2%80%93-create-publish-and-monitor-workflows-by-api . If the form is inaccessible or changes, follow the current guide or contact HighLevel support. Do not submit an application or send a message on the user's behalf without explicit authorization. Do not ask for API secrets in chat or include them in an application.

For a permitted location, the token needs the relevant scopes: `workflows.readonly` to inspect, `workflows.write` to create or update, `workflows.publish` to change publication status, `workflows.delete` to delete, and `workflows.logs` for execution logs. Logs may contain personal data. API approval and token scopes do not override the MakeBox server's own write gate; current hosted CRM writes are disabled. Do not promise creation, editing or publishing until those operations are enabled and verified. For unavailable writes, prepare a draft of triggers, conditions and actions without claiming it was created. Review live automation changes with the user and verify provider status and readback.
