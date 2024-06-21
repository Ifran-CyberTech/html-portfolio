## Architecture

- ifran.ajtech.au domain is managed by Anthony with DNS in cloudflare
- Cloudflare is pointing ifran.ajtech.au to a server which is using Nginx proxy manager
- Nginx proxy manager points ifran.ajtech.au towards an internal docker container via ip + port
- The internal container is synced to github on branch **feature/dockerfile** and checks for changes every 5 minutes
- Cloudflare is being used to proxy & cache the site, this means that if a change is made it may not reflect instantly
