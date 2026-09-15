# Synthtraffic

Synthtraffic generates realistic, repeatable event traffic from YAML or JSON scenarios.

## Install

1. Open [Releases](https://github.com/SynthTraffic/synthtraffic-releases/releases) and download the archive for your operating system and CPU.
2. Extract `synthtraffic` (macOS/Linux) or `synthtraffic.exe` (Windows).
3. Add the folder containing that file to your `PATH` — not the file itself. For example, if the Windows binary is `C:\Tools\synthtraffic\synthtraffic.exe`, add `C:\Tools\synthtraffic` to `PATH`.
4. Open a new terminal and confirm the installation:

```bash
synthtraffic --help
```

## Get a license

Choose a Free Trial or Developer license on [Pricing](https://www.synthtraffic.io/pricing/). Contact us through the website for Enterprise pricing and custom terms. After checkout or signup, you receive a signed `license.env` by email.

## Set your license

Set `SYNTHTRAFFIC_LICENSE_FILE` to the path of the `license.env` you received.

**macOS/Linux shell**

```bash
export SYNTHTRAFFIC_LICENSE_FILE=/path/to/license.env
```

**PowerShell**

```powershell
$env:SYNTHTRAFFIC_LICENSE_FILE = "C:/path/to/license.env"
```

## Run a sample

Save this as `hello-world.yaml`:

```yaml
generators:
  - name: events
    value:
      eventId: =uuid()
      source: =oneOf(web, mobile, api)
      createdAt: =now(format=RFC3339Milli)
```

Then preview three events:

```bash
synthtraffic sample hello-world.yaml --events 3 --seed 42
```
