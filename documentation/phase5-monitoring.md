# Phase 5 – Logging and Monitoring with AWS CloudTrail and CloudWatch

## Objective

Implement centralized logging and monitoring to provide visibility into AWS account activity and detect suspicious events.

---

## Services Used

| Service                   | Purpose                                              |
| ------------------------- | ---------------------------------------------------- |
| AWS CloudTrail            | Records AWS API activity and account events          |
| Amazon S3                 | Stores CloudTrail log files                          |
| Amazon CloudWatch Logs    | Centralized log collection                           |
| CloudWatch Metric Filters | Extract security-related events from logs            |
| CloudWatch Alarms         | Generate alerts when suspicious activity is detected |
| Amazon SNS                | Send email notifications when alarms are triggered   |

---

## Architecture

```text
AWS Resources
      ↓
CloudTrail
      ↓
S3 Log Storage
      ↓
CloudWatch Logs
      ↓
Metric Filters
      ↓
CloudWatch Alarms
      ↓
SNS Topic
      ↓
Email Notifications
```

---

## CloudTrail Configuration

| Setting                     | Value                      |
| --------------------------- | -------------------------- |
| Trail Name                  | Foody-Trail                |
| Multi-Region Trail          | Enabled                    |
| Log File Validation         | Enabled                    |
| Storage Location            | Amazon S3                  |
| CloudWatch Logs Integration | Enabled                    |
| IAM Role                    | CloudTrail_CloudWatch_Role |

---

## CloudWatch Log Configuration

| Setting          | Value          |
| ---------------- | -------------- |
| Log Group Name   | Foody_Logs     |
| Retention Period | 30 Days        |
| Log Source       | AWS CloudTrail |

---

## Metric Filters Implemented

| Filter Name                | Metric Name          | Purpose                                            |
| -------------------------- | -------------------- | -------------------------------------------------- |
| RootAccountUsageFilter     | RootAccountUsage     | Detect root account activity                       |
| UnauthorizedAPICallsFilter | UnauthorizedAPICalls | Detect access denied and unauthorized API requests |
| ConsoleLoginFailureFilter  | ConsoleLoginFailure  | Detect failed AWS console login attempts           |

---

## CloudWatch Alarms

| Alarm Name           | Threshold      | Purpose                                 |
| -------------------- | -------------- | --------------------------------------- |
| RootAccountUsage     | Greater than 0 | Alert when the root account is used     |
| UnauthorizedAPICalls | Greater than 0 | Detect unauthorized API activity        |
| ConsoleLoginFailure  | Greater than 3 | Detect repeated failed sign-in attempts |

---

## SNS Notification Configuration

| Setting             | Value                      |
| ------------------- | -------------------------- |
| Topic Name          | FoodyWoody-Security-Alerts |
| Topic Type          | Standard                   |
| Notification Method | Email                      |
| Subscription Status | Confirmed                  |

---

## Verification

The following components were successfully configured and verified:

* CloudTrail logging enabled.
* Multi-region trail created.
* CloudWatch Logs integration configured.
* Metric filters created for security events.
* CloudWatch alarms configured.
* SNS topic configured for email notifications.
* AWS account activity recorded and monitored.

---

## Security Benefits

| Security Control     | Benefit                                    |
| -------------------- | ------------------------------------------ |
| CloudTrail           | Provides an audit trail of AWS activity    |
| CloudWatch Logs      | Centralizes log collection                 |
| Metric Filters       | Detect suspicious behavior                 |
| CloudWatch Alarms    | Generate automated alerts                  |
| SNS Notifications    | Provide near real-time email notifications |
| Multi-Region Logging | Ensures visibility across all AWS regions  |

---

## Key Takeaways

This phase introduced centralized logging, monitoring, and alerting capabilities into the Foody Woody environment. These services provide visibility into AWS activity, improve incident detection, and establish the foundation for security operations and auditing.
