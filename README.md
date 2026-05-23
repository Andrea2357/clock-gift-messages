# Clock Gift Messages

Public remote message file for the Clock Gift desktop companion app.

The app reads `messages.json` from a fixed raw GitHub URL. Keep this repository public so the desktop app can sync without a private token.

Raw URL:

```text
https://raw.githubusercontent.com/Andrea2357/clock-gift-messages/main/messages.json
```

Edit flow:

1. Open the local editor from the main project: `remote_messages/editor.html`.
2. Download the generated `messages.json`.
3. Replace `messages.json` in this repository.
4. In the desktop app, use the raw URL above in remote message sync settings.
## Boyfriend editor

Open the editor through this preview URL:

`	ext
https://htmlpreview.github.io/?https://github.com/Andrea2357/clock-gift-messages/blob/main/editor.html
`

The editor runs in the browser, lets you edit every message category, downloads a new messages.json, or saves directly to GitHub when you provide a fine-grained token limited to this repository. Upload that downloaded file to this repository to update the remote messages used by the desktop app.
Token guidance:

- Create a fine-grained personal access token.
- Repository access: only Andrea2357/clock-gift-messages.
- Repository permissions: Contents as Read and write.
- Do not grant access to the private app repository.

