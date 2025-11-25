# Installing Profiles on Linux

This guide explains how to install the Linux versions of the privacy profiles (`*.json`) included in this repository.  
These files use the standard **Chromium enterprise policy** mechanism and apply system-level policies to the browser.

## 1. Choose the correct profile

Select the file that matches your browser family:

- **Brave**  
  `profiles/brave/linux-default.json`

- **Generic Chromium**  
  `profiles/generic/linux-default.json`

The `default` variant applies balanced privacy hardening without breaking common websites.

## 2. Review the file (recommended)

Open the JSON file in any text editor to review the policy keys.

No scripts, no executable code, and no extension installation entries are included.

## 3. Install the profile

The location depends on your browser package.  
Create the **managed policy directory** if it doesn’t exist, then copy the file into it.

### Brave (APT / Debian / Ubuntu)

```shell
sudo mkdir -p /etc/brave/policies/managed
sudo cp linux-default.json /etc/brave/policies/managed/policies.json
```

### Chromium (Debian / Ubuntu)

```shell
sudo mkdir -p /etc/chromium/policies/managed
sudo cp linux-default.json /etc/chromium/policies/managed/policies.json
```

### Google Chrome (Deb / RPM)

```shell
sudo mkdir -p /etc/opt/chrome/policies/managed
sudo cp linux-default.json /etc/opt/chrome/policies/managed/policies.json
```

Rename the file to policies.json if needed.

## 4. Verify the policy

Open your browser and go to:

- `brave://policy`
- `chrome://policy`
- `chromium://policy`

The policies from the JSON file should appear under **Active Policies**.  
If nothing appears, restart the browser and check again.

## 5. Removing the policy

Delete the policy file from the appropriate directory:

```sh
sudo rm /etc/brave/policies/managed/policies.json
# or
sudo rm /etc/chromium/policies/managed/policies.json
# or
sudo rm /etc/opt/chrome/policies/managed/policies.json
```

Restart the browser.
Once the file is removed, the browser returns to an unmanaged configuration.

## Notes

- Policies installed this way apply system-wide.
- Snap and Flatpak browser packages generally do **not** support system policies.
- Ensure the policy file is named `policies.json`.  

