
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
