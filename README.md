# Slack ⇄ ClickUp Request Sync (case study)

Keeping a Slack List request tracker in step with the ClickUp tasks behind it.

## The problem

Operations requests come in through a Slack form. Each one becomes a ClickUp task and a card in a Slack List tracker. As soon as the work moved in ClickUp, the Slack tracker went stale.

Slack Lists and ClickUp have no native sync, and Zapier has no ready-made actions for Slack Lists.

## The first version

A status change in ClickUp moves the matching card in Slack.

- The form workflow stores the ClickUp task URL on the Slack item, so each card can be matched to its task exactly.
- A Zap triggers on task changes and calls the Slack Lists API through a small private Slack app, since Zapier's own Slack connection can't edit Lists.
- Status names are identical on both sides, so no mapping table is needed.
