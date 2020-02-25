# node-red-tweakers.

This is a Node-RED flow.

This flow is monitoring the [buy&sell RSS feed](https://tweakers.net/feeds/va.xml) of the dutch site [tweakers.net](https://tweakers.net/).  It is checking for articles matching a specific criteria and if so posts a message on the slack channel with ID=`$slack_channel_tweakers`

## Prerequisites

The following 2 environments variables must be set for this flow:

1. **slack_token** : the API token of your slack Bot (customs integrations)
2. **slack_channel_tweakers** : The ID of the slack channel where the flow will post a message when an article has been put on tweakers matching the criteria.  Don't forget to assure that the slack Bot is mem ber of this channel.

## Testing

You can test if slack configuration is properly setup by triggering the `[test slack output]` inject node: This should post a message on the slack channel with id `$slack_channel_tweakers`.