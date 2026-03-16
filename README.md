# Music Service Pi-Hole Lists

# Work in progress. Not currently working.

These lists are my attempt at creating workable pi-hole blocklists for s0uncloud, sp0tify and other music services. Current lists either don't exist or don't work well. Some of these issues are app level, some likely are DNS related. 

Currently only working on s0undcloud. Censoring service names to reduce SEO.

## How to add these lists to Pi-Hole

Navigate to the web UI, click "lists" in the sidebar, and add the follow as addresses (and, appropriately to which you're adding, click "add blocklist" or "add allowlist")

**S0undcloud Blacklist/Blocklist:**
```bash
https://raw.githubusercontent.com/kevin-mead/music-related-pihole-lists/refs/heads/main/s0undcloud-blacklist-kevin.txt
```

**S0undcloud Whitelist/Allowlist:**
```bash
https://raw.githubusercontent.com/kevin-mead/music-related-pihole-lists/refs/heads/main/s0undcloud-whitelist-kevin.txt
```
After adding, SSH into your server and use this command to update (or wait for your automatic updater to run):
```bash
pihole -g
```
## Known Issues

**Lots of issues are currently happening**

Signs that s0undcloud is mad at you:
- The player waits 3-10 seconds between songs
- The player is skipping songs

## Relevant Links

This [Reddit thread](https://www.reddit.com/r/pihole/comments/1h7s1nr/finally_got_soundcloud_mobile_desktop_working/).

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## Disclaimer

Using Pi-Hole/DNS blocklists is not illegal in my jurisdiction, or most for that matter. It may break terms of service for any given service/result in bad things happening (like account bans). Use these lists and Pi-Hole at your own risk, obviously.
