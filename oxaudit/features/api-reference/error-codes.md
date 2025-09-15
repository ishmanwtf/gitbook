# Error Codes

**Error Codes**

When using the API, you might encounter error codes if something goes wrong with your request. Understanding these error codes will help you troubleshoot issues more efficiently.

1. **400 Bad Request**
   * **Cause**: There may be missing or incorrect parameters in your request.
   * **Solution**: Double-check all required fields and ensure your data is correctly formatted.
2. **401 Unauthorized**
   * **Cause**: Your API key is missing or invalid.
   * **Solution**: Ensure the `Authorization` header includes a valid API key in the format `Bearer YOUR_API_KEY`.
3. **403 Forbidden**
   * **Cause**: Your API key lacks the necessary permissions for this action.
   * **Solution**: Verify the permissions associated with your API key. You may need to update permissions or use a key with higher access.
4. **404 Not Found**
   * **Cause**: The endpoint or resource you’re trying to access doesn’t exist.
   * **Solution**: Confirm the endpoint URL and ensure any IDs (like `audit_id`) are correct.
5. **429 Too Many Requests**
   * **Cause**: You have exceeded the rate limit for API requests.
   * **Solution**: Wait a moment and try again. Consider implementing request throttling in your integration.
6. **500 Internal Server Error**
   * **Cause**: There is an issue on OXAudit’s end, possibly due to server maintenance or an unexpected error.
   * **Solution**: Wait and try again. If the issue persists, contact OXAudit support.
