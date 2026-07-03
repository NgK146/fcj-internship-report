---
title: "Week 10 Worklog"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Develop the Frontend user interface for the Document Management System (DMS).
* Integrate Amazon Cognito for user authentication.
* Build the foundational Serverless Backend (API Gateway & Lambda).

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Set up Frontend project folder structure <br> - Create base HTML/CSS/JS for login, home, and file manager pages <br> - Pick a lightweight UI library | 22/06/2026 | 22/06/2026 | <https://docs.aws.amazon.com/amplify/latest/userguide/getting-started.html> |
| Tue | - Build login and registration pages <br> - Integrate Cognito Hosted UI / AWS Amplify for auth flow <br> - Test login and store JWT token in localStorage | 23/06/2026 | 23/06/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools-app-integration.html> |
| Wed | - Build main file list view with folder grouping <br> - Add upload button with progress bar <br> - Add download, version view, and activity history UI features | 24/06/2026 | 24/06/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-presigned-url.html> |
| Thu | - Polish UI: responsive layout, error handling, loading states <br> - Write first Lambda function (login handler, return token) <br> - Create API Gateway to route Frontend requests to Lambda | 25/06/2026 | 25/06/2026 | <https://docs.aws.amazon.com/lambda/latest/dg/getting-started.html> |
| Fri | - Write Lambda for file upload (generate S3 Presigned URL) <br> - Write Lambda for file download (time-limited Presigned URL) <br> - Write Lambda to fetch file list from DynamoDB | 26/06/2026 | 26/06/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-presigned-url.html> |
| Sat | - Connect Frontend to API Gateway, fix CORS settings <br> - Test end-to-end: login → list files → upload → download <br> - Log all bugs found for fixing next week | 27/06/2026 | 27/06/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-cors.html> |
| Sun | - Design DynamoDB table schema (metadata and audit log) <br> - Configure IAM Role for Lambda to access S3 and DynamoDB <br> - Plan next week: connect Lambda to DynamoDB, finish remaining features | 28/06/2026 | 28/06/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.html> |

### Week 10 Achievements:

* Completed the Frontend UI (login, registration, and file manager pages).
* Built core Lambda functions (auth, upload/download Presigned URL generation, file listing).
* Successfully connected the Frontend to the Backend via API Gateway.
* Designed the DynamoDB schema for document metadata and audit logs.
