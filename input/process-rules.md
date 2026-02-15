# Process Rules

## User Registration Process
1. User submits registration form with username, email, and password
2. System validates input data:
   - Username must be unique and 3-20 characters
   - Email must be valid format and unique
   - Password must be at least 8 characters
3. System creates user profile with default preferences
4. System sends verification email
5. User must verify email within 24 hours
6. Upon verification, account is activated

## Project Creation Workflow
1. User must be authenticated
2. User provides project name and description
3. System validates:
   - Project name is unique for the user
   - Description is not empty
4. System creates project with owner set to current user
5. System creates default task categories
6. System logs activity
7. User is redirected to project dashboard

## Idea Submission Process
1. User must be authenticated
2. User selects project or submits as standalone idea
3. User fills in idea form:
   - Title (required, max 100 chars)
   - Description (required, max 5000 chars)
   - Category (optional)
   - Related documents (optional)
4. System validates input
5. System creates idea record
6. System notifies project collaborators (if applicable)
7. System logs activity
8. System returns idea ID to user

## Review and Approval Process
1. Submitted ideas go to "pending" status
2. Project owner or designated reviewers can:
   - Approve: Move to "approved" status
   - Reject: Move to "rejected" status with reason
   - Request changes: Add comments and keep in "pending"
3. Approved ideas are visible to all collaborators
4. Rejected ideas are only visible to author and reviewers
5. All status changes are logged

## Collaboration Rules
1. Project owner can:
   - Add/remove collaborators
   - Change project status
   - Delete project
   - Approve/reject ideas
2. Collaborators can:
   - View project details
   - Submit ideas
   - Comment on ideas
   - Vote on ideas
3. Public users can:
   - View public projects
   - View approved ideas

## Data Retention Policy
1. Active projects: Retained indefinitely
2. Archived projects: Retained for 2 years
3. Completed projects: Retained for 5 years
4. Deleted projects: Soft delete with 30-day recovery period
5. Activity logs: Retained for 1 year
6. User accounts: Deleted after 3 years of inactivity (with 30-day notice)
