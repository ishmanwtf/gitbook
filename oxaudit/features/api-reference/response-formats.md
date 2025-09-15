# Response Formats

All responses from OXAudit’s API are in JSON format. Each response typically includes essential details about the action performed and any relevant IDs or status messages. Here’s an example response for a successful audit request.

**Example JSON Response**:

```
json

{
  "audit_id": "abc123",
  "status": "pending"
}
```

**Description**:

* `audit_id`: The unique identifier for this audit request. Use this ID to check the audit’s status or retrieve results later.
* `status`: Shows the current status of the audit (e.g., "pending," "in\_progress," or "completed").

The `audit_id` is essential for tracking the audit process, especially when making follow-up requests to check the status or fetch results.
