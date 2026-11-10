# Cleanplex templates for Unraid

Community Apps template for [Cleanplex](https://github.com/nazmolla/Cleanplex), which skips or mutes scenes you choose (nudity, violence, profanity and more) in Plex for every client, including Plex Web.

## Requirements

- Plex Media Server on this Unraid server with host networking (the Unraid default), claimed (signed in) so it has created its certificate.
- A kernel with nftables for the firewall redirect. Without it, run the container without `CLEANPLEX_REDIRECT` (scan and mark only) or see the Cleanplex README for the bridge-mode layout.

## Install

Apps tab, search *Cleanplex*, **Install**. Set:

- **Plex appdata (read only)**: Plex's appdata folder (the one containing `Library/Application Support/Plex Media Server`).
- **Media**: your media at the *same path Plex sees it at*, because Plex reports file paths and Cleanplex opens them to scan. Add one entry per Plex media mount.

On first start Cleanplex reads Plex's URL, token and certificate from Plex's appdata, starts its front door, turns enforcement on and switches Plex Relay and DLNA off. Nothing else needs configuring.

## Support

[github.com/nazmolla/Cleanplex/issues](https://github.com/nazmolla/Cleanplex/issues)
