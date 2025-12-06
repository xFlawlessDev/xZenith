# Discord Webhook Setup Guide

This guide will help you set up Discord webhook integration for automatic release notifications.

## Prerequisites

- Admin access to your Discord server
- Admin access to this GitHub repository

---

## Step 1: Create Discord Webhook

1. **Open Discord Server Settings**

   - Go to your Discord server
   - Right-click on the channel where you want release notifications (e.g., `#announcements` or `#releases`)
   - Select `Edit Channel`

2. **Create Webhook**

   - Navigate to `Integrations` tab
   - Click `Webhooks` → `New Webhook`
   - Give it a name like "xZenith Releases"
   - (Optional) Upload the xZenith logo as the webhook avatar
   - Click `Copy Webhook URL` - **Save this URL securely!**

3. **Save Changes**
   - Click `Save Changes`

---

## Step 2: Add Webhook to GitHub Secrets

1. **Navigate to Repository Settings**

   - Go to: https://github.com/xFlawlessDev/xZenith/settings/secrets/actions

2. **Create New Secret**
   - Click `New repository secret`
   - **Name**: `DISCORD_WEBHOOK_URL`
   - **Value**: Paste the Discord webhook URL you copied earlier
   - Click `Add secret`

---

## Step 3: Test the Integration

### Option A: Create a Test Release (Recommended)

1. Go to: https://github.com/xFlawlessDev/xZenith/releases/new
2. Create a test release:

   - **Tag**: `v1.1.1-test` (or any version)
   - **Title**: `Test Release - Discord Integration`
   - **Description**: Add some release notes
   - Check `This is a pre-release` (so it doesn't confuse users)
   - Click `Publish release`

3. Check your Discord channel - you should see a notification within seconds!

4. If successful, you can delete the test release

### Option B: Wait for Next Real Release

Simply publish your next release as normal, and the Discord notification will be sent automatically.

---

## Customization Options

### Change Embed Color

Edit `.github/workflows/discord-release-notification.yml` and modify the `color` value:

```yaml
"color": 3447003, # Blue (default)
```

Color values (in decimal):

- 🔵 Blue: `3447003`
- 🟢 Green: `5763719`
- 🟡 Gold: `16766720`
- 🔴 Red: `15548997`
- 🟣 Purple: `10181046`

### Modify Notification Content

You can customize the embed by editing the `payload.json` section in the workflow file:

- **Title**: Change the emoji or text format
- **Fields**: Add/remove information fields
- **Buttons**: Modify button labels or add more links
- **Avatar**: Change the webhook avatar URL

---

## Notification Preview

When you publish a release, Discord will receive a rich embed notification with:

- 🚀 **Version number** and release title
- 📅 **Release date** (relative timestamp)
- 📝 **Full release notes** (automatically formatted)
- 🖼️ **xZenith logo** thumbnail
- 🔘 **Download button** (direct link to release)
- 💬 **Discord invite button** (join your community)

---

## Troubleshooting

### Webhook not sending?

1. **Check GitHub Actions**

   - Go to: https://github.com/xFlawlessDev/xZenith/actions
   - Click on the latest workflow run
   - Check for errors in the logs

2. **Verify Secret**

   - Ensure `DISCORD_WEBHOOK_URL` secret exists
   - Make sure the URL starts with `https://discord.com/api/webhooks/`

3. **Test Webhook Manually**
   ```bash
   curl -H "Content-Type: application/json" \
        -d '{"content": "Test message"}' \
        YOUR_WEBHOOK_URL
   ```

### Release notes too long?

The workflow automatically truncates release notes to 3800 characters and adds a "Read full release notes" link.

---

## Security Notes

⚠️ **Never commit the webhook URL directly to the repository!**  
Always use GitHub Secrets to store sensitive information.

If you accidentally expose your webhook URL:

1. Delete the exposed webhook in Discord
2. Create a new webhook
3. Update the GitHub secret with the new URL

---

## Additional Resources

- [Discord Webhook Documentation](https://discord.com/developers/docs/resources/webhook)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [GitHub Encrypted Secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets)

---

**Questions?** Join our Discord: https://discord.gg/HKG9GNTesb
