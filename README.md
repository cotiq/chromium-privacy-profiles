# Chromium privacy profiles

A collection of minimal, privacy-focused policy profiles for Chromium-based browsers.

All profiles avoid forced extensions, external URLs, proxy changes, certificate injections, or any high-risk configuration.

Supported browsers:

- **Brave**
- **Generic Chromium implementations** (Chrome, Chromium, Edge, Vivaldi, Opera, etc.)

## Installation guides

- macOS: [docs/installing-macos.md](docs/installing-macos.md)
- Linux: [docs/installing-linux.md](docs/installing-linux.md)
- Windows: [docs/installing-windows.md](docs/installing-windows.md)

## What these profiles do

- Reduce background network activity
- Minimize passive telemetry
- Apply stricter default permission settings
- Reduce WebRTC IP leakage
- Disable autofill components
- Block third-party cookies
- Disable Sync
- Keep configurations small and auditable
- Maintain normal browsing usability

### Brave profiles additionally disable

- AI features
- Rewards
- VPN UI
- News
- Web Discovery
- Talk
- Speedreader
- Tor window integration
- Stats ping system

### Generic profiles

Generic profiles include only standard Chromium policy keys.

## License
MIT License.