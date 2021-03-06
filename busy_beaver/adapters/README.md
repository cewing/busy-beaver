# Adapter Information

<!-- TOC -->

- [GitHub Integration](#github-integration)
- [Youtube Adapter](#youtube-adapter)
  - [Where to get your channel id?](#where-to-get-your-channel-id)
  - [How to create an api key?](#how-to-create-an-api-key)
  - [Example](#example)

<!-- /TOC -->

## GitHub Integration

Create a [GitHub OAuth App](https://github.com/settings/developers). The sole function of this app is to provide a means for the Slack user to validate their GitHub account.

You will also need need to create a [Personal Access Token](https://github.com/settings/tokens) that can be used to access the GitHub API.

## Youtube Adapter

### Where to get your channel id?

Login to youtube and go to https://www.youtube.com/account_advanced, your
channel id will be displayed.

### How to create an api key?

Go to https://console.developers.google.com and create a project. After you can
visit https://developers.google.com/youtube/registering_an_application#Create_API_Keys
for instructions to generate the api key. After you have both, you can move to
the examples.

### Example

```python
api_key = "..."
channel_id = "..."
youtube = YoutubeAdapter(api_key=api_key)
data = youtube.get_latest_videos_from_channel(channel_id)
videos = data["items"]
```
