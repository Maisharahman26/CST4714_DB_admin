# Lab: One Ticket, Two JSON Designs
# 1. Referenced Design

```json
{
  "users": [
    {
      "user_id": 103,
      "display_name": "Requester 103"
    },
    {
      "user_id": 201,
      "display_name": "Agent 201"
    }
  ],
  "tickets": [
    {
      "ticket_id": 1003,
      "subject": "Low water pressure",
      "status": "resolved",
      "requester_id": 103,
      "assignee_id": 201
    }
  ],
  "events": [
    {
      "event_id": 5005,
      "ticket_id": 1003,
      "event_type": "created",
      "event_at": "2026-02-03T12:05:00Z"
    },
    {
      "event_id": 5006,
      "ticket_id": 1003,
      "event_type": "status_changed",
      "event_at": "2026-02-03T14:25:00Z"
    },
    {
      "event_id": 5007,
      "ticket_id": 1003,
      "event_type": "status_changed",
      "event_at": "2026-02-03T19:40:00Z"
    }
  ]
}
```

## 2. Embedded / Hybrid Design
```json
{
  "ticket_id": 1003,
  "subject": "Low water pressure",
  "status": "resolved",
  "requester": {
    "requester_id": 103,
    "display_name": "Requester 103"
  },
  "assignee": {
    "assignee_id": 201,
    "display_name": "Agent 201"
  },
  "events": [
    {
      "event_id": 5005,
      "event_type": "created",
      "event_at": "2026-02-03T12:05:00Z"
    },
    {
      "event_id": 5006,
      "event_type": "status_changed",
      "event_at": "2026-02-03T14:25:00Z"
    },
    {
      "event_id": 5007,
      "event_type": "status_changed",
      "event_at": "2026-02-03T19:40:00Z"
    }
  ]
}
```
## 3. Tradeoff Explanation


The application opens ticket 1003 and shows its requester and events. Those facts in each design such has the requester's name and ticket's events are found using their IDs. In this design eveything is stored in a orgazied ticket so that it is much easier to find and can display eveything together and organized. If the requester changes their display name and the ticket accumulates years of events, the referenced design only needs to update the user's information. In the embedded design, multiple tickets may need to be updated, so it can grow too large.


