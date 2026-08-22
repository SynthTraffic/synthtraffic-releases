# Synthtraffic releases

This repository publishes **binary releases only** for [Synthtraffic](https://github.com/SynthTraffic/synthtraffic) (proprietary source).

## Download

Open [Releases](https://github.com/SynthTraffic/synthtraffic-releases/releases) and pick the archive for your OS and CPU architecture.

## Verify checksums

Each release includes `checksums.txt`. After downloading:

```bash
sha256sum -c checksums.txt
```

PowerShell:

```powershell
Get-FileHash .\synthtraffic_1.0.0_windows_amd64.zip
# compare with the line in checksums.txt
```

## License

Synthtraffic requires a signed `license.env`. After signup you receive a license file; activate once:

```bash
synthtraffic license activate license.env
synthtraffic license status
```

Get a trial or purchase a license from the Synthtraffic website.
