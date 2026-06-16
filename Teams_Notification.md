# Teams Notification Playbook

## Goal

Send a Microsoft Teams notification when a high-severity Sentinel incident is created.

## Workflow

1. Sentinel incident trigger starts Logic App.
2. Logic App extracts incident details.
3. Message is posted to SOC Teams channel.
4. Analyst reviews incident link.
