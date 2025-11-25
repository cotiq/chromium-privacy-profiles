# Installing Profiles on Windows

This guide explains how to install the Windows versions of the privacy profiles (`*.reg` files) included in this repository.  
These files apply system-wide browser policies through the Windows Registry.

## 1. Choose the correct profile

Select a file matching your browser family:

- **Brave**
    - `profiles/brave/windows-default.reg`

- **Generic Chromium**
    - `profiles/generic/windows-default.reg`

The `default` variant is designed for balanced privacy without breaking common websites.

## 2. Review the file (recommended)

`.reg` files are plain text.  
Open them in any editor (Notepad, VS Code) to confirm the keys being applied.

No scripts, no executables, no forced extensions are included.

## 3. Apply the profile

Double-click the `.reg` file and confirm:

- Allow Registry Editor to make changes.
- Confirm import.

The profile is applied immediately.

Policies are written to:`HKEY_LOCAL_MACHINE\Software\Policies\BraveSoftware\Brave` or `HKEY_LOCAL_MACHINE\Software\Policies\Google\Chrome` depending on the file.

## 4. Verify the policy

Open your browser and navigate to:

- `brave://policy`
- `chrome://policy`
- `edge://policy`

Check the **Active Policies** section.  
You should see the keys included in your imported `.reg` file.

If you don’t see them, restart the browser.

## 5. Removing a profile

To remove a previously applied policy:

1. Open Registry Editor (`regedit`).
2. Delete the relevant key: 
   - For Brave: `HKEY_LOCAL_MACHINE\Software\Policies\BraveSoftware`
   - For generic Chromium: `HKEY_LOCAL_MACHINE\Software\Policies\Google\Chrome`

3. Restart the browser.

The browser will return to its normal, unmanaged configuration.

## Notes

- Policies imported at the machine level apply to all users.
- User-level policies (`HKEY_CURRENT_USER`) are not used in these profiles.
- If your organization already enforces policies, Windows will display them in the policy page with status “managed”.



