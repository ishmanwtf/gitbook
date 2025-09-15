# Endpoints

## **Start an Audit**

* **Endpoint**: `POST /v1/audits`
* **Purpose**: Initiates a new audit for the specified project or contract.
* **Parameters**:
  * `project_name` (string): The name of your project.
  * `contracts` (file): The smart contract files to audit, provided as file uploads.
*   **Example Request**:

    ```
    http
    POST https://api.oxaudit.com/v1/audits
    Authorization: Bearer YOUR_API_KEY
    Content-Type: multipart/form-data
    ```
* **Form Data**:
  * `project_name`: "MyDeFiProject"
  * `contracts`: \[File Uploads]
* **Retrieve Audit Results**
  * **Endpoint**: `GET /v1/audits/{audit_id}`
  * **Purpose**: Fetches the results of a specific audit.
  * **Parameters**:
    * `audit_id` (string): The unique ID of the audit you want to retrieve.
  * **Example Request**:

```
http
GET  https://api.oxaudit.com/v1/audits/abc123
Authorization: Bearer YOUR_API_KEY

```

## **List All Projects**

* **Endpoint**: `GET /v1/projects`
* **Purpose**: Lists all projects associated with your account.
* **Parameters**: None
* **Example Request**:

```
http
GET https://api.oxaudit.com/v1/projects
Authorization: Bearer YOUR_API_KEY
```
