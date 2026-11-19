# www redirect for mcskimmingshearing.biz

A temporary stopgap. It sends visitors who arrive on `www.mcskimmingshearing.biz` to `https://mcskimmingshearing.biz`, keeping the page path.

It exists because Wix still holds a stale Cloudflare for SaaS custom hostname for `www`, which stops Cloudflare serving that address from our own zone (Wix ticket 3000443782). `www` is pointed here with a DNS-only CNAME to `willy363.github.io`, which bypasses the Cloudflare proxy.

Once Wix removes the hostname: delete the `www` CNAME in Cloudflare, add `www.mcskimmingshearing.biz` back as a custom domain on the `mcskimming-website` Worker, and delete this repo.
