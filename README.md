# aws-cost-automation
Event-driven AWS cost monitoring using Lambda, EventBridge, and SNS
# AWS Cost Automation – v1

This project is a simple, event-driven AWS cost monitoring automation.

## What it does
- Runs on a scheduled interval using EventBridge
- Uses AWS Lambda to scan EC2 resources
- Detects stopped EC2 instances (potential cost waste)
- Sends email notifications via SNS
- Uses least-privilege IAM (read-only detection)

## Architecture
EventBridge → Lambda → EC2 (Read-Only) → SNS → Email

## Why this matters
Manual cost checks don’t scale. This automation provides
repeatable, low-risk visibility into potential cloud waste.

## Current scope
- Detection only (no automated actions)
- Read-only by design
- Alert-based (human decision required)

## Next version (v2)
- Reduce alert noise
- Add state/change detection
- Prepare for approval-based actions
