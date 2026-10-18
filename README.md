
# slack-php

This [SDK](https://github.com/sdk-fabric/slack-php) is managed by the [SDK Fabric](https://sdk-fabric.org/) project, a global infrastructure to
automatically generate SDKs for every API.

You can find more information about this SDK at [TypeHub](https://typehub.cloud/):
https://app.typehub.cloud/d/sdkfabric/slack

## Usage

```php
<?php

require __DIR__ . '/vendor/autoload.php';

$client = new \SdkFabric\Slack\Client::build('[access_token]');

// Deletes a message from a channel.
$response = $client->chat()->delete(new Delete_Message_Request());

// Retrieves a permalink URL for a specific existing message.
$response = $client->chat()->getPermalink('channel', 'message_ts');

// Sends an ephemeral message to a user in a channel.
$response = $client->chat()->postEphemeral(new Post_Ephemeral_Request());

// Sends a message to a channel.
$response = $client->chat()->postMessage(new Post_Message_Request());

// Schedules a message to be sent to a channel at a future time.
$response = $client->chat()->scheduleMessage(new Schedule_Message_Request());

// Updates a message in a channel.
$response = $client->chat()->update(new Update_Message_Request());
```
