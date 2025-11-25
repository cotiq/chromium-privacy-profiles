# Installing Profiles on macOS

This guide explains how to install the macOS versions of the privacy profiles (`*.mobileconfig`) included in this repository.  
These files apply system-level policies using the standard macOS configuration profile mechanism.

## 1. Choose the correct profile

Pick a file based on your browser family:

- **Brave**
    - `profiles/brave/macos-default.mobileconfig`

- **Generic Chromium**
    - `profiles/generic/macos-default.mobileconfig`

The `default` variant provides balanced privacy hardening without breaking common websites.

## 2. Review the file (recommended)

`.mobileconfig` profiles are XML.  
Open them in any editor (TextEdit, VS Code) and review the keys being applied.

Nothing in these profiles installs extensions, certificates, proxies, or payloads outside browser policies.

## 3. Install the profile

1. Double-click the `.mobileconfig` file.
2. Open **System Settings → General → Device Management**.
3. You will see the pending profile listed.
4. Select it, review the contents, and click **Install**.
5. Confirm when macOS prompts you.

## 4. Verify the policy

After installation:

1. Open your browser
2. Navigate to:
    - `brave://policy`
    - `chrome://policy`

3. Confirm that the expected keys appear under **Active Policies**.

## 5. Removing a profile

1. Open **System Settings → General → Device Management**.
2. Delete the profile from the list.
3. Confirm when macOS prompts you.
4. Restart the browser.

The browser will return to its unmanaged state.

## Notes

- Profiles apply system-wide for all users unless otherwise restricted.
- If your system is managed by an organization, macOS may prevent manual profile installation or removal.
- Safari does **not** support these policy keys; these profiles only affect Chromium-based browsers.