# actions-webhook

A little sample on how to trigger a GitHub Action via webhook.

We can trigger GitHub Actions workflow runs via webhook using creating a [`repository_dispatch` event](https://developer.github.com/v3/repos/#create-a-repository-dispatch-event) via GitHub API:

```bash
curl -H "Authorization: token <YOUR_GITHUB_TOKEN>" \
    --request POST \
    --data '{"event_type": "<YOUR_EVENT_TYPE>"}' \
    https://api.github.com/repos/<YOUR_GITHUB_USER>/<YOUR_GITHUB_REPO>/dispatches
```
