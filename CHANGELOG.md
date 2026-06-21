# SPECTER Changelog

All notable changes to SPECTER will be documented in this file.
This changelog is client-facing and included in public releases.

## v1.0.0 -- Initial Release

### Forensic Acquisition Engine

SPECTER is a portable, cross-platform forensic disk and memory acquisition toolkit
built for incident response professionals, digital forensic examiners, and
managed security teams.

### Features

- **Interactive TUI** -- guided wizard interface with real-time progress, live
  log output, and intuitive keyboard navigation
- **E01 Disk Imaging** -- forensically sound Expert Witness Format acquisition
  with hardware-level integrity verification via ewfacquire/ewfverify
- **Memory Capture** -- volatile memory acquisition using platform-native tools
  (WinPmem on Windows, osxpmem on macOS)
- **Cloud Upload** -- direct evidence upload to AWS S3, Google Cloud Storage, or
  Azure Blob Storage with configurable credentials and bucket/container targeting
- **Cryptographic Sealing** -- HMAC-SHA256 integrity seal across all collected
  artifacts with tamper-evident manifest generation
- **Resume Support** -- interrupted acquisitions can be resumed from the last
  completed phase without re-imaging
- **Headless Mode** -- fully automated operation via YAML configuration for
  scripted or MDM-driven deployments
- **JSON Manifest** -- machine-readable `specter-manifest.json` with full chain
  of custody metadata, file hashes, and schema-validated structure
- **Schema Validation** -- JSON Schema contract for manifest files ensures
  interoperability and programmatic verification

### Platform Support

- Windows (amd64) -- fully self-contained with bundled ewfacquire, ewfverify,
  and WinPmem
- macOS (arm64, amd64) -- fully self-contained with bundled ewfacquire and
  ewfverify built from source
- Linux (amd64) -- fully self-contained with statically linked ewfacquire and
  ewfverify

### Portability

All platforms ship as a single zip archive containing the SPECTER binary and all
required forensic tools. No package installation is needed or permitted --
installing software on the target machine would modify the drive being imaged
and compromise forensic integrity.

### Deployment

- Extract to USB drive or network share
- Run as administrator/root
- Supports JumpCloud, Microsoft Intune, and Jamf Pro MDM deployment
- Cloud provider setup guides included for AWS, GCS, and Azure
