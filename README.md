 установки SSL сертификата поставить его на автообновление через cron:
```bash
0 */12 * * * /usr/bin/certbot -a \! -d /run/systemd/system && perl -e 'sleep int(rand(3600))' && certbot -q renew --renew-hook "systemctl reload nginx"

```
