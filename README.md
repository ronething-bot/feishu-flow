# feishu-flow
feishu-flow test

we need send message to feishu group if action is review_requested and draft is false.


## create feishu flow.

1. create webhook trigger

input json data

```json
{
  "action": "review_requested",
  "pull_request": {
    "html_url": "https://github.com/ronething-bot/feishu-flow/pull/1",
    "state": "open",
    "title": "Update README.md",
    "draft": false,
    "body": ""
  },
  "sender": {
    "login": "ronething-bot"
  }
}
```


2. create filter condition

<img width="491" alt="image" src="https://github.com/ronething-bot/feishu-flow/assets/47621124/6b7398fe-e343-41a3-b380-b26b913712a9">

3. send message to feishu group

<img width="1098" alt="image" src="https://github.com/ronething-bot/feishu-flow/assets/47621124/a623efb4-4c07-4cfa-bd19-62dcf653a57f">

## config github repo webhook settings

<img width="1160" alt="image" src="https://github.com/ronething-bot/feishu-flow/assets/47621124/f4cf8ea1-62e6-4fb4-8e82-3e15ee8b7233">

Add webhook, choose content-type as application/json, and then select `Pull Requests` event.

## demo

<img width="539" alt="image" src="https://github.com/ronething-bot/feishu-flow/assets/47621124/494e4326-7370-4500-aa78-1bd431ff2653">


