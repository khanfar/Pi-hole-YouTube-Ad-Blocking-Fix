# Pi-hole YouTube Ad Blocking Fix

This repository contains a list of domains that should be whitelisted in Pi-hole to ensure proper YouTube functionality while maintaining ad-blocking capabilities.

## Problem
Pi-hole's aggressive ad blocking can sometimes interfere with YouTube's core functionality, causing issues with video playback, recommendations, and other features.

## Solution
Add the following domains to your Pi-hole whitelist to restore YouTube functionality while maintaining ad blocking effectiveness:

### Required Domains
```
s.ytimg.com
www.youtube.com
youtube.com
googlevideo.com
beacons.gvt2.com
beacons.gcp.gvt2.com
i.ytimg.com
www.youtube-nocookie.com
youtube-ui.l.google.com
youtubei.googleapis.com
doubleclick.net
googleads.g.doubleclick.net
static.doubleclick.net
jnn-pa.googleapis.com
```

## How to Whitelist

### Method 1: Using Pi-hole Web Interface
1. Access your Pi-hole admin interface
2. Navigate to "Whitelist" under "Domains"
3. Add each domain individually

### Method 2: Using Terminal
Run the following commands:

```bash
pihole -w s.ytimg.com
pihole -w www.youtube.com
pihole -w youtube.com
pihole -w googlevideo.com
pihole -w beacons.gvt2.com
pihole -w beacons.gcp.gvt2.com
pihole -w i.ytimg.com
pihole -w www.youtube-nocookie.com
pihole -w youtube-ui.l.google.com
pihole -w youtubei.googleapis.com
pihole -w doubleclick.net
pihole -w googleads.g.doubleclick.net
pihole -w static.doubleclick.net
pihole -w jnn-pa.googleapis.com
```

## Important Notes
- After adding these domains to the whitelist, you may need to:
  1. Update gravity: `pihole -g`
  2. Clear your browser cache
  3. Restart your browser
- Some YouTube ads might still appear as this is designed to fix functionality while maintaining reasonable ad blocking

## Contributing
Feel free to submit issues and pull requests if you find other domains that should be added or removed from the whitelist.

## Author
Maintained by Khanfar Systems

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
