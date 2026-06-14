# config-generated

A dump of generated DDM and .mobileconfig profiles - for exploration purposes

## Structure

### DDM (Declarative Device Management)

Apple's modern device management framework (macOS 13+, iOS 16+). Declarations are JSON-formatted.

```
ddm/
├── activations/       # Activation declarations – link configurations to predicates
│   ├── com.apple.activation.simple.json
│   └── com.apple.activation.simple.macos.json
├── assets/            # Asset declarations – referenced data and credentials
│   ├── com.apple.asset.data.json
│   └── com.apple.asset.userpassword.json
├── configurations/    # Configuration declarations – settings applied to devices
│   ├── com.apple.configuration.account.caldav.json
│   ├── com.apple.configuration.account.carddav.json
│   ├── com.apple.configuration.account.exchange.json
│   ├── com.apple.configuration.app.managed.json
│   ├── com.apple.configuration.diskmanagement.settings.json
│   ├── com.apple.configuration.passcode.settings.json
│   ├── com.apple.configuration.restrictions.explicit.json
│   ├── com.apple.configuration.screensaver.json
│   ├── com.apple.configuration.security.certificate.json
│   ├── com.apple.configuration.services.configuration-files.json
│   └── com.apple.configuration.softwareupdate.enforcement.specific.json
└── management/        # Management declarations – MDM metadata
    ├── com.apple.management.organization.json
    └── com.apple.management.properties.json
```

### .mobileconfig Profiles

Legacy XML-based (property list) configuration profiles supported across all Apple platforms.

```
mobileconfig/
├── certificate.mobileconfig      # Root CA certificate trust
├── email.mobileconfig            # IMAP email account
├── filevault.mobileconfig        # FileVault full-disk encryption (macOS)
├── passcode.mobileconfig         # Passcode policy
├── restrictions.mobileconfig     # Device restrictions
├── softwareupdate.mobileconfig   # Software update deferral (macOS)
├── vpn.mobileconfig              # IKEv2 VPN
└── wifi.mobileconfig             # 802.1X Wi-Fi (WPA2 Enterprise)
```

## References

- [Apple Declarative Device Management](https://developer.apple.com/documentation/devicemanagement/declarativedevicemanagement)
- [Apple Configuration Profile Reference](https://developer.apple.com/documentation/devicemanagement/configuration_profiles)
- [MDM Protocol Reference](https://developer.apple.com/documentation/devicemanagement)
