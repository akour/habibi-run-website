# Google Play Data Safety Draft

## Status
Provisional working draft only. Do not submit. No APK/AAB, Android manifest, Godot export configuration, plugin list, SDK inventory, or network capture was available for inspection.

## Confirmed from project brief
- App name: Juha’s Bad Day: Habibi, Run!
- Developer: One Apps
- Package ID: `com.oneapps.habibirun`
- Platform: Android
- Engine: Godot 4
- Release status: In development

## Planned / assumed behavior
- No accounts or login
- No advertising
- No analytics
- No location collection
- No contacts access
- No camera access
- No microphone access
- No personal information intentionally collected
- No personal data sold or shared
- Save data stored locally on the device

These are requirements, not verified binary facts.

## Likely draft answers if binary verification confirms the plan
- Does the app collect or share any required user data types? Likely **No**.
- Is all user data encrypted in transit? Likely **Not applicable** if no data leaves the device.
- Can users request deletion? Likely **Not applicable** for server-side data; users can clear local app data or uninstall.
- Is data processing optional? Likely **Not applicable** if no collection occurs.

## Binary verification required
1. Inspect the exported Android manifest and merged manifest.
2. Confirm whether `INTERNET` or any sensitive permission is present.
3. Review Godot Android export settings.
4. Inventory every plugin, module, library, and SDK.
5. Run network traffic inspection on a release-candidate build.
6. Confirm no crash reporting, analytics, ads, payments, authentication, push notifications, cloud save, leaderboards, or social SDKs.
7. Confirm no device identifiers or diagnostic data leave the device.
8. Confirm local save format and deletion behavior.
9. Verify Play Billing is absent.
10. Verify no background services or telemetry endpoints are present.

## Review triggers
Re-open this draft immediately if the project adds ads, analytics, crash reporting, cloud saving, accounts, authentication, payments, leaderboards, social features, push notifications, external SDKs, device identifiers, or network logging.
