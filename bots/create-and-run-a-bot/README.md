# Create and run a Bot

This document outlines the steps required to create your first bot with Rocket.Chat.

## Prerequisites

* [Running Rocket.Chat server](../../installation/)
* User with admin privileges

## Steps

### 1. Create a bot user

In order to talk to your chatbot there must be a user account pre-configured on the Rocket.Chat server that the bot can log in to.

To create the account you need to have admin privileges:

1. In the topbar, click the three dots \(Options\) and then click **Administration**
2. Select **Users** from the left sidebar
3. Click `+` \(Add User\) button in the right sidebar
4. In the profile window that appears, fill in _Name_, _Username_, _Email_ and _Password_ fields
5. Enable _Verified_ toggle under the _Email_ field
6. Disable _Require password change_ toggle under the _Password_ field
7. Select `bot` from the `Add Role` dropdown menu and click _Add Role_ button to the right
8. Disable _Join default channels_ and _Send welcome email_ checkboxes
9. Click _Save_

Once saved, the bot will be configured with the username and password set on step 4. You can use `ROCKETCHAT_USER` and `ROCKETCHAT_PASSWORD` [environmental variables](../configure-bot-environment.md) to log in to Rocket.Chat server with this username and password pair.

NOTE: to avoid creating multiple accounts for bot emails, you can use Gmail `+address` alias. For example: `youremail+botnam@gmail.com`. [See this issue for more](https://github.com/RocketChat/Rocket.Chat/issues/7125).

### 2. Code your bot

To make the process of coding a bot easier and faster, you may want to check our existing guides below to quickly deploy a basic bot instance. As an advanced alternative, you can create your bot from the scratch using your favorite framework.

* [Running a Botkit Bot](botkit-bot.md)
* [Running a Hubot Bot](hubot-bot.md)
* [Running a Botpress Bot](botpress-bot.md)
* [Running a Rasa Bot](rasa-bot.md)
* [Running a bBot Bot](../running-a-bbot-bot.md)

Regardless of the option you choose, to make your bot work you will need credentials of the bot user you created in the previous step.

### 3. Talk to your bot

If the bot is configured to listen to direct messages \(`RESPOND_TO_DM=true`\), and messages are prepended with `BOT_NAME` or a preconfigured `BOT_ALIAS`, the bot will _usually_ respond to all messages addressed directly to the bot user \(depending on the particular bot framework\).

