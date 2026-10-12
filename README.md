# 🎯 RuleHunt — YARA / Sigma / Nuclei Repository (MIT)

Aggregate open-source detection rules from GitHub in one searchable place.
UI in EN/TR/AR. Static single file + README.

## Tracked repos (all public & famous)

- YARA: `Yara-Rules/rules`, `Neo23x0/signature-base`,
  `advanced-threat-research/Yara-Rules`, `eset/malware-ioc`
- Sigma: `SigmaHQ/sigma`
- Nuclei: `projectdiscovery/nuclei-templates`
- Data: `OTRF/Security-Datasets`

## Features (all live via GitHub public API, no key)

- **Repo cards:** stars, forks, push date, description — straight from API.
- **Index:** per-repo recursive file tree → `.yar/.yara/.sigma/.yml/.yaml`
  file lists. Progress bar included.
- **Fast search:** substring over indexed paths (150 cap).
- **Viewer:** raw file fetch + structure **validator**
  (YARA: rule/strings:/condition: · Sigma: title/logsource/detection ·
  Nuclei: id/info) + copy + raw download link.
- **Updates board:** latest commits across repos, date-sorted.
- **Alerts:** keyword/CVE watch + browser Notification on matching commits.
  Auto-poll every 30 min (14 API calls/hr — safe under the 60/hr anon limit).
- **Quota meter:** live `X-RateLimit-Remaining` + optional personal token
  input (60 → 5000/hr), stored locally.
- **Pro $7/mo:** Telegram instant + Webhook/API + no ads (interest saved;
  backend worker required for delivery) + payment box (BTC/USDT/IBANs).

## Money & contact

- `CONFIG.ads` (AdSense/Carbon) footer slot.
- 📧 baranavisat@gmail.com · 📞 +90 531 326 37 22 · WhatsApp

## Run

```bash
cd rulehunt
python3 -m http.server 8080
```

## License

MIT. Rules belong to their authors — respect repo licenses.

## Telegram (@BaranScanBot)

- Footer'da herkese açık "Telegram" butonu (`t.me/BaranScanBot`) — ziyaretçi
  doğrudan bota yazar, ek ayar gerekmez.
- Sipariş/satış bildirimleri (`tgSend`) yalnızca `CONFIG`... `TG.chat`
  doluysa sahibine gider. Chat ID'yi @userinfobot'tan alıp `TG.chat`e yazın.
- ⚠️ **GÜVENLİK:** Bot tokeni herkese açık istemci kodundadır; kaynağı
  gören herkes bot adına mesaj gönderebilir. Kötüye kullanımda BotFather'dan
  tokeni yenileyin ve asla bu botla hassas işlem yapmayın. Gerçek çözüm:
  backend proxy.
