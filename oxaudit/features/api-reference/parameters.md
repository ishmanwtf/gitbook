# Parameters

Here’s a sample request for starting an audit in your project. This example shows how to submit your API key and required data to initiate an audit process.

### **Request**:

```
http
POST https://api.oxaudit.com/v1/audits
Authorization: Bearer YOUR_API_KEY
Content-Type: multipart/form-data

Form Data:
- project_name: "MyDeFiProject"
- contracts: [File Uploads]
```

### **Description**:

* **Authorization Header**: Your API key is required to authenticate and authorize the request.
* **Form Data**: The `project_name` identifies the project in your OXAudit account, and `contracts` allows you to upload the specific smart contract files to be audited.
