# Proposed AWS architecture

| Service | Role |
|---|---|
| S3 and KMS | Documents and preference records stored per organisation, encrypted with its own key |
| Textract | Text read from scanned agreements and PDF policies |
| Bedrock | Document classification and policy comparison drafts |
| DynamoDB | Register, preference records, reminders and the review log |

One AWS account per customer, encrypted at rest and in transit. The public demo calls none of these services.
