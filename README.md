# Mantis-BT-Microsoft-Teams

A [MantisBT](http://www.mantisbt.org/) plugin to communicate with [Microsoft Teams ](https://www.microsoft.com/en-us/microsoft-365/microsoft-teams/group-chat-software) projects and channels via a webhooks.


# Setup

* The `master` branch requires Mantis 2.0.x
* Extract this repo to your *Mantis folder/plugins/Teams*.
* On the Teams side, create a new Webhook (found in *Incomming Webhook*) and note the URL that Teams generates for you,see [Documentation](https://docs.microsoft.com/en-us/microsoftteams/platform/webhooks-and-connectors/how-to/add-incoming-webhook).
* On the MantisBT side, access the plugin's configuration page and fill in your Teams webhook URL.
* You can map your MantisBT projects to other Incoming webhooks by setting the *plugin_Teams_url_webhooks* option in Mantis.  Follow the instructions on the plugin's configuration page to get there. Make sure the *plugin_Teams_url_webhooks* configuration option is set to "All Users", with type "complex".
    Example value for this setting:

            array (
              'My First Mantis Project' => 'https://outlook.office.com/webhook/xx/IncomingWebhook/xx',
              'My Second Mantis Project' => 'https://outlook.office.com/webhook/xx/IncomingWebhook/xx'
            )
* You can specify which bug fields appear in the Teams notifications. Edit the *plugin_Teams_columns* configuration option for this purpose.  Follow the instructions on the plugin configuration page.
* You can map MantisBT usernames to Teams mentions. You can configure it the same way as the other "complex" configurations above.
    Example value for this setting:

            array (
              'My First Mantis Project' => 'https://outlook.office.com/webhook/xx/IncomingWebhook/xx',
              'My Second Mantis Project' => 'https://outlook.office.com/webhook/xx/IncomingWebhook/xx'
            )


# Forked

This is a modified version of the [Slack Plugin](https://github.com/infojunkie/MantisBT-Slack) made by [Karim Ratib](https://github.com/infojunkie) and adapted for Teams by [Hamdi Amine](https://github.com/Hamdi-Amine).
