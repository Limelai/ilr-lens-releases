# ILR Lens releases

Official Windows releases of **ILR Lens**, a free ILR assurance and comparison tool from [FEFunding.co.uk](https://fefunding.co.uk/tools/ilr-lens).

ILR Lens helps further education colleges compare ILR returns, investigate the changes behind their learner numbers, and review assurance findings. It runs locally on Windows. Your ILR data stays on your computer.

This repository holds approved release files only: the signed installer, the complete package, the guides and the checksums. It contains no source code.

## Download

The recommended place to download ILR Lens is its page on FEFunding.co.uk, which also explains what it does, how to install it and how to check the download:

**https://fefunding.co.uk/tools/ilr-lens**

Each version is also listed under [Releases](https://github.com/Limelai/ilr-lens-releases/releases). Every release holds the same files:

| File | What it is |
|---|---|
| `ILR-Lens-Setup-<version>.exe` | The installer, signed by LIMELAI LIMITED |
| `ILR-Lens-<version>-Windows.zip` | The complete package: the installer, the three guides, `README.txt` and `SHA256SUMS.txt` |
| `ILR-Lens-Quick-Start.pdf` | From installing to a first result |
| `ILR-Lens-User-Guide.pdf` | The full guide |
| `ILR-Lens-Release-Notes.pdf` | What this version does, and what it cannot do |
| `SHA256SUMS.txt` | SHA-256 checksums for the installer and the guides |
| `README.txt` | Orientation, upgrade note and attribution |

## Requirements

- Windows 10 version 1809 or later, or Windows 11, on a 64-bit (x64) PC.
- No administrator rights. The installer installs ILR Lens for your Windows account only.
- No account, licence key or registration. ILR Lens is free.

## Checking your download

**Publisher.** The installer is signed by **LIMELAI LIMITED**, the company behind FEFunding.co.uk. To check it, right-click the downloaded file, choose **Properties**, open the **Digital Signatures** tab, and confirm the signer is LIMELAI LIMITED.

**Checksum.** In PowerShell, in the folder you downloaded to, run:

```powershell
Get-FileHash .\ILR-Lens-Setup-1.1.0.exe -Algorithm SHA256
```

Compare the result with the value on the FEFunding.co.uk download page and in that release's `SHA256SUMS.txt`. A matching checksum shows the file is byte for byte the approved release. The digital signature shows who signed it.

**Microsoft Defender SmartScreen.** The signature is valid and publicly trusted. SmartScreen builds reputation for a new signing certificate as downloads accumulate, so early downloads may still show a warning. If you see one, check the publisher and the checksum as above, then follow your organisation's IT policy. If you are not sure, ask your IT team before going further. Never turn off SmartScreen or your antivirus to install ILR Lens.

## Privacy

ILR Lens processes your ILR on your computer. It does not upload learner data to FEFunding or anyone else. It has no account, no server and no cloud service.

## About

- **Created by** Ben Sonoiki.
- **Published free by** [FEFunding.co.uk](https://fefunding.co.uk).
- **Software publisher:** LIMELAI LIMITED, the company behind FEFunding.co.uk, and the name Windows shows for the installer.
- **Contact:** ben@fefunding.co.uk

ILR Lens is an independent assurance and investigation tool. It is not affiliated with, endorsed by, or a product of the Department for Education.

ILR Lens includes LARS reference data published by the Department for Education under the [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/). The exact dataset and version are named in each release's `README.txt` and in the application under Settings and help.

## For maintainers

Only approved releases are published here. A release is never edited after it is published: a correction is a new version.

1. Assemble the files on Windows with the FEFunding packaging script, which checks the installer's checksum and signature, regenerates `SHA256SUMS.txt` and builds the ZIP.
2. Create a **draft** release tagged `v<version>` and attach the seven files.
3. Run **Actions › Check draft release** with the tag and the approved installer SHA-256. It checks every attached file, the checksums, the ZIP's contents and the installer's signature.
4. Publish the release only when that check passes and the owner has approved it.

No source code, secrets, credentials or development history belong in this repository.
