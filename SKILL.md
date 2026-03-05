# DashTask Agent API Documentation

## Overview
The DashTask Agent API allows developers to interact with the DashTask platform, enabling automation of tasks through a programmable interface.

## Authentication
To use the DashTask API, you must authenticate using an API key that can be generated in your account settings.

### Generating an API Key
1. Log in to your DashTask account.
2. Navigate to the **API Keys** section.
3. Click on **Generate New Key**.
4. Store the key securely, as it will only be displayed once.

## Endpoints
### 1. Create a Task
- **POST /tasks**
- Creates a new task.

**Request Body:**
```json
{
  "title": "Task Title",
  "description": "Task Description",
  "due_date": "2026-03-05T04:00:00Z"
}
```

### 2. Get Task Details
- **GET /tasks/{task_id}**
- Retrieves details about a specific task.

### 3. Update a Task
- **PUT /tasks/{task_id}**
- Updates the specified task.

### 4. Delete a Task
- **DELETE /tasks/{task_id}**
- Deletes the specified task.

## Examples
### Creating a Task
```bash
curl -X POST https://api dashtask.com/tasks \
-H "Authorization: Bearer YOUR_API_KEY" \
-H "Content-Type: application/json" \
-d '{"title":"Task Title","description":"Task Description"}'
```

### Getting a Task Details
```bash
curl -X GET https://api.dashtask.com/tasks/{task_id} \
-H "Authorization: Bearer YOUR_API_KEY"
```

## Conclusion
This documentation serves as a quick reference for using the DashTask Agent API. For more detailed information, refer to the [official documentation](https://docs.dashtask.com).