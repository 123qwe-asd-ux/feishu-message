# Feishu-Notification-Robot

`This is a GitHub Action workflow to send pull request notifications to Feishu group via Feishu bot.`

If you want to use the Feishu notification robot in your GitHub repository, you need to read this README carefully.

## To make a new robot in Feishu

1. Go to the Feishu group where you want to receive notifications.
2. Click on the group name at the top, then select "Manage Bots" (管理机器人).
3. Click on "Add Bot" (添加机器人) and choose "Custom Bot" (自定义).
4. Fill in the bot name and select an avatar if desired.
5. Under "Bot Settings" (机器人设置), enable "Receive Messages" (接收消息) and "Send Messages" (发送消息).
6. Copy the "Webhook URL" (Webhook 地址) provided for the bot. You will need this URL in the next steps.
7. Save the bot settings.

## To configure the GitHub Action workflow

In your GitHub repository, you need to set up the workflow file and secrets.
you can copy the workflow file from this repository and modify it as needed.

1. Create a new file in your repository at `.github/workflows/feishu-notification.yml`.
2. Copy the content of the `feishu-notification.yml` file from this repository into your new file.
3. In your GitHub repository, go to "Settings" > "Secrets and variables" > "Actions".
4. Click on "New repository secret" and add a new secret with the name `FEISHU_BOT_WEBHOOK_URL` and paste the Webhook URL you copied from Feishu as the value.
5. Save the secret.  
6. Commit and push the changes to your repository.
7. The workflow will now run on pull request events and send notifications to your Feishu group via the bot.
8. You can customize the notification message in the workflow file as needed.

## Note

- Make sure the bot has the necessary permissions to send messages in the Feishu group.
- Test the setup by creating a pull request in your repository to see if the notification is sent successfully.
- You can modify the workflow file to change the notification format or add more information as needed.
- If you encounter any issues, check the GitHub Actions logs for debugging information.
