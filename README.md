# adguard-filters

Personal ad/tracker blocklists for my home + VPS [AdGuard Home](https://adguard.com/en/adguard-home/overview.html) setup.

## Lists

| File | Scope |
|------|-------|
| [`filters/gnevashev-personal.txt`](filters/gnevashev-personal.txt) | Hand-maintained extras that slip past the stock lists (e.g. Yandex.Direct delivery). DNS-level. |

## Subscribe in AdGuard Home

Filters → DNS blocklists → **Add blocklist → Add a custom list**, then paste the raw URL:

```
https://raw.githubusercontent.com/gnevashev/adguard-filters/main/filters/gnevashev-personal.txt
```

AdGuard Home re-fetches per the `! Expires:` header (1 day).

## Notes

AdGuard Home is **DNS-level**: it blocks whole domains (`||domain^`), not URL paths,
and it can't hide empty ad containers (no cosmetic filtering). Path-based and
element-hiding rules live in the clearly marked *browser-only* section at the
bottom of the list — use them with uBlock Origin / the AdGuard browser extension.
