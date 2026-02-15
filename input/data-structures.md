# Data Structures

## User Profile
```json
{
  "userId": "string",
  "username": "string",
  "email": "string",
  "createdAt": "timestamp",
  "preferences": {
    "theme": "string",
    "notifications": "boolean",
    "language": "string"
  },
  "metadata": {
    "lastLogin": "timestamp",
    "loginCount": "number"
  }
}
```

## Project Structure
```json
{
  "projectId": "string",
  "name": "string",
  "description": "string",
  "owner": "userId",
  "collaborators": ["userId"],
  "status": "enum(active, archived, completed)",
  "createdAt": "timestamp",
  "updatedAt": "timestamp",
  "tags": ["string"],
  "tasks": [
    {
      "taskId": "string",
      "title": "string",
      "description": "string",
      "status": "enum(todo, in_progress, done)",
      "assignee": "userId",
      "dueDate": "timestamp",
      "priority": "enum(low, medium, high)"
    }
  ]
}
```

## Idea Structure
```json
{
  "ideaId": "string",
  "title": "string",
  "description": "string",
  "category": "string",
  "author": "userId",
  "createdAt": "timestamp",
  "votes": "number",
  "comments": [
    {
      "commentId": "string",
      "author": "userId",
      "content": "string",
      "createdAt": "timestamp"
    }
  ],
  "relatedDocs": ["documentId"]
}
```

## Activity Log
```json
{
  "logId": "string",
  "userId": "string",
  "action": "string",
  "entityType": "string",
  "entityId": "string",
  "timestamp": "timestamp",
  "metadata": "object"
}
```
