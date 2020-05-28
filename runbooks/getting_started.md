# Set up Transposit

## Learn the basics

Welcome! Let's step through some Transposit basics.

## Runbooks

Runbooks in Transposit are documents written in [Markdown](https://www.markdownguide.org/getting-started/), sectioned into steps. You can find the runbook you are viewing now [here](https://console.transposit.com/mc/t/yoko-test-mc-team/runbooks/getting_started).

## Actions

You can automate common tasks in your runbooks by using actions. For example, you can add an action and configure it to restart a specific EC2 instance in AWS.

## Try some actions

You can navigate to the [Actions Page](https://console.transposit.com/mc/t/yoko-test-mc-team/actions/) to create your first Action.

Note that most actions require users to add authentication in the [integrations page](https://console.transposit.com/mc/t/yoko-test-mc-team/settings/integrations) to run; you'll see an error in the Slack channel if the integration is not configured. You only need to add authentication once for different actions using the same underlying conncector.

For example, try the **Get Jira Issues** action below, and if the Jira integration is not configured, you'll see the error that this action **requires authorization for: Jira(User)**

_This action will list 10 Jira issues assigned to the current user_

[Get Jira Issues](https://console.transposit.com/mc/t/yoko-test-mc-team/actions/display_jira_users)

In the next step, we'll fix that.

_Note: you can close this runbook and return to it from the Slack channel by using the `/transposit` slash command._

## Integrations

Integrations connect Transposit with your infrastructure and any third-party services you use, allowing you to run actions.

Go to [Transposit Settings > Integrations](https://console.transposit.com/mc/t/yoko-test-mc-team/settings/integrations), search for "_Jira_" integration, enter auth configurations(if any), and then click on "Connect" option with "Authorization for workflows that are performed as you" text.
Jira integration.

There are two kinds of authentication:

- _Authorization for workflows that don’t require a specific user_ -- If you are an admin and want to add authentication for everyone on the team to use, choose this option.
- _Authorization for workflows that are performed as you_ -- Any member of the team can use this option to add authentication using their own account. This is a good option for restricting access to certain actions.

Now you can go ahead creating your own actions from the [actions page](https://console.transposit.com/mc/t/yoko-test-mc-team/actions/), add authentications in the integrations page if needed.

## Add an Action to a Runbook

Navigate to [Test Runbook](https://console.transposit.com/mc/t/yoko-test-mc-team/runbooks/test_runbook), click on "Add Action" on the top, and select the action you created in the previous step.

To test out this new action, bring out transposit on Slack by typing `/transposit`, choose **Home** from the dropdown on top left, and search for **Test Runbook**.

## Triggers

You can add triggers to Transposit, and invoke them with alerting systems such as PagerDuty or OpsGenie, or with monitoring systems such as New Relic or Datadog.

When triggers are fired, they send a message to a Slack channel, along with a prompt to create an incident.

Try to invoke your first trigger by navigating to [Triggers Page](https://console.transposit.com/mc/t/yoko-test-mc-team/settings/triggers), Click on _Add Trigger_, choose _A Hello World Integrator to get started_ from the integrator list,
,enter an _existing_ channel name, and click _Add_.

To manually invoke this trigger, open your local terminal, and run `curl ENDPOINT_URL` -- replace ENDPOINT_URL with the **Endpoint URL** on the trigger you created. You should get an alert Slack from Transposit.

When you need to integrate with your Pagerduty or Opsgenie account, simply copy a trigger's endpoint url, and add it as a "webhook" on Pagerduty, Opsgenie or any other monitoring systems.

## Activity Timeline

If you have created an incident from a trigger, you can view each incident's timeline at [Transposit > Activities](https://console.transposit.com/mc/t/yoko-test-mc-team/activities)

Over in the new channel created for the incident from the previous step, you can open runbooks, and jump to the web view of the incident.

When you're ready, close the incident from [incident timeline web UI](https://console.transposit.com/mc/t/yoko-test-mc-team/activities)

## Ask Your Team to Join Transposit!

Now you know how Transposit works, it's time to ask the rest of your team to join!

Ask your team to [sign in to transposit](https://console.transposit.com) using the same **Slack workspace** you signed in with. They should be automatically added to your team.

Also invite them to `#transposit-welcome` channel on Slack so they can test out Transposit by themselves.
