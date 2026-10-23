# accountancy-app-admin-electron

## Impersonation script path

The impersonation script location is read from `runtime-config.json` in Electron's
user data directory. On first launch, the app creates this file using the current
default path. The app logs the exact config file location at startup.

To change the script location without rebuilding, update
`impersonationScriptPath` to the new absolute path, for example:

```json
{
  "impersonationScriptPath": "E:\\Apps\\AccountancyApp\\accountancy-app-firestore\\accountancy-app-production\\create-Impersonation-token.js"
}
```

The new path is read when impersonation is started, so saving the config file is
enough; the app does not need to be rebuilt or restarted.
