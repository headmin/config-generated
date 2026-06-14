# config-generated

A dump of generated DDM and `.mobileconfig` profiles - for exploration purposes.

- Explore the repo with [Pique](https://github.com/macadmins/pique)
- Process everything related to DDM and .mobileconfig with [contour](https://github.com/macadmins/contour)  

## Structure

### DDM Beta (Declarative Device Management)

Apple's modern device management framework. Declarations are JSON-formatted. This folder reflects the beta schema and type identifiers.

```
ddm-beta/
├── activation/                                    # Activation declarations – link configurations to predicates
│   └── activation-simple.json
├── asset/                                         # Asset declarations – credentials and referenced data
│   ├── asset-credential-acme.json                 # ACME protocol certificate credential
│   ├── asset-credential-certificate.json          # Certificate credential
│   ├── asset-credential-identity.json             # Identity credential
│   ├── asset-credential-scep.json                 # SCEP certificate credential
│   ├── asset-credential-userpassword.json         # Username and password credential
│   ├── asset-data.json                            # Generic data asset
│   └── asset-useridentity.json                    # User identity asset
├── configuration/                                 # Configuration declarations – settings applied to devices
│   ├── account-caldav.json                        # CalDAV calendar account
│   ├── account-carddav.json                       # CardDAV contacts account
│   ├── account-exchange.json                      # Exchange account
│   ├── account-google.json                        # Google account
│   ├── account-ldap.json                          # LDAP directory account
│   ├── account-mail.json                          # Mail (IMAP/SMTP) account
│   ├── account-subscribed-calendar.json           # Subscribed calendar account
│   ├── app-managed.json                           # Managed app installation
│   ├── app-settings.json                          # Managed app settings
│   ├── audio-accessory-settings.json              # Audio accessory settings
│   ├── content-cache-settings.json                # Content caching settings
│   ├── diskmanagement-settings.json               # Disk management settings
│   ├── extensible-sso.json                        # Extensible SSO
│   ├── external-intelligence-settings.json        # External intelligence (AI) settings
│   ├── intelligence-settings.json                 # Apple Intelligence settings
│   ├── keyboard-settings.json                     # Keyboard settings
│   ├── legacy-interactive.json                    # Legacy interactive configuration
│   ├── legacy.json                                # Legacy (MDM profile) configuration
│   ├── management-status-subscriptions.json       # Management status subscriptions
│   ├── management-test.json                       # Management test declaration
│   ├── math-settings.json                         # Math settings
│   ├── migration-assistant-settings.json          # Migration Assistant settings
│   ├── network-dns-proxy.json                     # DNS proxy
│   ├── network-dns-settings.json                  # DNS settings
│   ├── network-relay.json                         # Network relay
│   ├── network-vpn-always-on.json                 # Always-on VPN
│   ├── network-vpn-ikev2.json                     # IKEv2 VPN
│   ├── network-vpn-ipsec.json                     # IPsec VPN
│   ├── network-vpn-vpn-plugin.json                # VPN plugin
│   ├── package.json                               # Package installation
│   ├── passcode-settings.json                     # Passcode policy settings
│   ├── safari-bookmarks.json                      # Safari managed bookmarks
│   ├── safari-extensions-settings.json            # Safari extensions settings
│   ├── safari-settings.json                       # Safari settings
│   ├── screensharing-connection-group.json        # Screen sharing connection group
│   ├── screensharing-connection.json              # Screen sharing connection
│   ├── screensharing-host-settings.json           # Screen sharing host settings
│   ├── security-certificate.json                  # Certificate trust
│   ├── security-identity.json                     # Identity certificate
│   ├── security-passkey-attestation.json          # Passkey attestation
│   ├── services-background-tasks.json             # Background task management
│   ├── services-configuration-files.json          # Configuration file deployment
│   ├── siri-settings.json                         # Siri settings
│   ├── softwareupdate-enforcement-specific.json   # Software update enforcement
│   ├── softwareupdate-settings.json               # Software update settings
│   ├── watch-enrollment.json                      # Apple Watch enrollment
│   └── webcontent-filter-plugin.json              # Web content filter plugin
└── management/                                    # Management declarations – MDM metadata
    ├── management-organization-info.json          # Organization information
    ├── management-properties.json                 # MDM properties
    └── management-server-capabilities.json        # Server capabilities
```

### `.mobileconfig` Profiles

XML property list configuration profiles supported across Apple platforms. Split into three folders by purpose.

#### `profiles/apple/` — Apple payload types and MDM commands

Generated from Apple's published payload and command schemas.

```
profiles/apple/
├── -globalpreferences.mobileconfig            # Global macOS preference domain
├── accountconfiguration.mobileconfig          # Account configuration command
├── activensextensions.mobileconfig            # Active notification/share extensions
├── adcertificate-managed.mobileconfig         # AD certificate
├── airplay-security.mobileconfig              # AirPlay security
├── airprint.mobileconfig                      # AirPrint printers
├── app-lock.mobileconfig                      # Single app / app lock mode
├── applyredemptioncode.mobileconfig           # App Store redemption code command
├── asam.mobileconfig                          # Autonomous Single App Mode
├── assetcache-managed.mobileconfig            # Content caching (managed)
├── associated-domains.mobileconfig            # Associated domains
├── authenticate.mobileconfig                  # Authenticate MDM command
├── cellular.mobileconfig                      # Cellular settings
├── cellularprivatenetwork-managed.mobileconfig # Private cellular network
├── certificatelist.mobileconfig               # Certificate list command
├── checkout.mobileconfig                      # Shared iPad checkout command
├── clearpasscode.mobileconfig                 # Clear passcode command
├── commonpayloadkeys.mobileconfig             # Common payload keys reference
├── conferenceroomdisplay.mobileconfig         # Conference room display mode
├── declarations.mobileconfig                  # Declarative management declarations command
├── declarativemanagement.mobileconfig         # Declarative management payload
├── deleteuser.mobileconfig                    # Delete user command
├── deviceinformation.mobileconfig             # Device information query command
├── devicelock.mobileconfig                    # Device lock command
├── dictionary.mobileconfig                    # Dictionary settings
├── directoryservice-managed.mobileconfig      # Directory service (Active Directory)
├── discrecording.mobileconfig                 # Disc recording settings
├── dnsproxy-managed.mobileconfig              # DNS proxy (managed)
├── dnssettings-managed.mobileconfig           # DNS settings (managed)
├── dock.mobileconfig                          # Dock settings
├── domains.mobileconfig                       # Email/web domains
├── education.mobileconfig                     # Education configuration
├── enablelostmode.mobileconfig                # Enable lost mode command
├── erasedevice.mobileconfig                   # Erase device command
├── esso.mobileconfig                          # Extensible SSO
├── ews-account.mobileconfig                   # Exchange Web Services account
├── familycontrols-timelimits-v2.mobileconfig  # Screen Time / Family Controls
├── fileproviderd.mobileconfig                 # File provider settings
├── finder.mobileconfig                        # Finder settings
├── firstactiveethernet-managed.mobileconfig   # First active Ethernet interface
├── firstethernet-managed.mobileconfig         # First Ethernet interface
├── font.mobileconfig                          # Custom font installation
├── getbootstraptoken.mobileconfig             # Get bootstrap token command
├── gettoken.mobileconfig                      # Get token command
├── globalethernet-managed.mobileconfig        # Global Ethernet settings
├── google-oauth.mobileconfig                  # Google OAuth account
├── homescreenlayout.mobileconfig              # Home screen layout
├── installapplication.mobileconfig            # Install application command
├── installedapplicationlist.mobileconfig      # Installed application list command
├── installenterpriseapplication.mobileconfig  # Install enterprise application command
├── installprofile.mobileconfig                # Install profile command
├── installprovisioningprofile.mobileconfig    # Install provisioning profile command
├── invitetoprogram.mobileconfig               # Invite to program command
├── loginitems-managed.mobileconfig            # Login items (managed)
├── loginwindow.mobileconfig                   # Login window settings
├── lom.mobileconfig                           # Lights-Out Management
├── lomdevicerequest.mobileconfig              # LOM device request command
├── machineinfo.mobileconfig                   # Machine info command
├── managedapplicationattributes.mobileconfig  # Managed app attributes command
├── managedapplicationconfiguration.mobileconfig # Managed app configuration command
├── managedapplicationfeedback.mobileconfig    # Managed app feedback command
├── managedapplicationlist.mobileconfig        # Managed app list command
├── managedclient-preferences.mobileconfig     # Managed client preferences
├── manifesturl.mobileconfig                   # Manifest URL command
├── mcx-filevault2.mobileconfig                # FileVault 2 (MCX)
├── mcx-timemachine.mobileconfig               # Time Machine (MCX)
├── mcx.mobileconfig                           # MCX managed preferences payload
├── mcxloginscripts.mobileconfig               # Login/logout scripts (MCX)
├── mcxmenuextras.mobileconfig                 # Menu bar extras (MCX)
├── mcxprinting.mobileconfig                   # Printing (MCX)
├── networkusagerules.mobileconfig             # Network usage rules
├── notificationsettings.mobileconfig          # Notification settings
├── nsextension.mobileconfig                   # Extension policy
├── passwordhash.mobileconfig                  # Password hash payload
├── preference-security.mobileconfig           # Security preference pane
├── preference-users.mobileconfig              # Users & Groups preference pane
├── profilelist.mobileconfig                   # Profile list command
├── profileremovalpassword.mobileconfig        # Profile removal password
├── provisioningprofilelist.mobileconfig       # Provisioning profile list command
├── proxy-http-global.mobileconfig             # Global HTTP proxy
├── refreshcellularplans.mobileconfig          # Refresh cellular plans command
├── relay-managed.mobileconfig                 # Network relay (managed)
├── removeapplication.mobileconfig             # Remove application command
├── removemedia.mobileconfig                   # Remove media command
├── removeprofile.mobileconfig                 # Remove profile command
├── removeprovisioningprofile.mobileconfig     # Remove provisioning profile command
├── requestmirroring.mobileconfig              # Request mirroring command
├── restartdevice.mobileconfig                 # Restart device command
├── restrictions.mobileconfig                  # Device restrictions
├── returntoservice.mobileconfig               # Return to service command
├── rotatefilevaultkey.mobileconfig            # Rotate FileVault recovery key command
├── screensaver-user.mobileconfig              # Screen saver (user-level)
├── screensaver.mobileconfig                   # Screen saver settings
├── secondactiveethernet-managed.mobileconfig  # Second active Ethernet interface
├── secondethernet-managed.mobileconfig        # Second Ethernet interface
├── security-certificatepreference.mobileconfig     # Certificate trust preference
├── security-certificaterevocation.mobileconfig     # Certificate revocation
├── security-certificatetransparency.mobileconfig   # Certificate transparency
├── security-fderecoverykeyescrow.mobileconfig      # FileVault recovery key escrow
├── security-identitypreference.mobileconfig        # Identity preference
├── security-pem.mobileconfig                       # PEM certificate
├── security-pkcs1.mobileconfig                     # PKCS#1 certificate
├── security-root.mobileconfig                      # Root certificate trust
├── security-smartcard.mobileconfig                 # Smart card settings
├── servicemanagement.mobileconfig             # Service management (launchd items)
├── setautoadminpassword.mobileconfig          # Set auto admin password command
├── setbootstraptoken.mobileconfig             # Set bootstrap token command
├── setfirmwarepassword.mobileconfig           # Set firmware password command
├── setrecoverylock.mobileconfig               # Set recovery lock command
├── settings.mobileconfig                      # Settings command
├── submitdiaginfo.mobileconfig                # Submit diagnostic info command
├── syspolicy-kernel-extension-policy.mobileconfig # Kernel extension policy (KEXT)
├── system-extension-policy.mobileconfig       # System extension policy
├── system-logging.mobileconfig                # System logging settings
├── systemconfiguration.mobileconfig           # System configuration
├── systemmigration.mobileconfig               # System migration settings
├── systempolicy-control.mobileconfig          # Gatekeeper / system policy control
├── systempolicy-managed.mobileconfig          # System policy managed exceptions
├── tcc-configuration-profile-policy.mobileconfig  # Privacy / TCC policy (PPPC)
├── thirdactiveethernet-managed.mobileconfig   # Third active Ethernet interface
├── thirdethernet-managed.mobileconfig         # Third Ethernet interface
├── tokenupdate.mobileconfig                   # Token update command
├── tvremote.mobileconfig                      # TV remote settings
├── unlockuseraccount.mobileconfig             # Unlock user account command
├── userauthenticate.mobileconfig              # User authenticate command
├── validateapplications.mobileconfig          # Validate applications command
├── verifyfirmwarepassword.mobileconfig        # Verify firmware password command
├── verifyrecoverylock.mobileconfig            # Verify recovery lock command
├── vpn-managed-appmapping.mobileconfig        # Per-app VPN mapping (managed)
├── vpn-managed.mobileconfig                   # VPN (managed)
├── webclip-managed.mobileconfig               # Web clip (managed)
├── wifi-managed.mobileconfig                  # Wi-Fi (managed)
├── xsan-preferences.mobileconfig              # Xsan preferences
└── xsan.mobileconfig                          # Xsan settings
```

#### `profiles/apps/` — Third-party app managed preferences

Managed configuration profiles scoped to individual third-party application preference domains.

```
profiles/apps/
├── com-1password-1password.mobileconfig              # 1Password
├── com-alectrona-patch-agent.mobileconfig            # Alectrona Patch Agent
├── com-alectrona-patch-notifier.mobileconfig         # Alectrona Patch Notifier
├── com-alectrona-patch.mobileconfig                  # Alectrona Patch
├── com-anthropic-claudefordesktop.mobileconfig       # Claude for Desktop
├── com-barebones-bbedit.mobileconfig                 # BBEdit
├── com-brave-browser.mobileconfig                    # Brave Browser
├── com-citrix-receiver-nomas.mobileconfig            # Citrix Receiver
├── com-cloudflare-warp.mobileconfig                  # Cloudflare WARP
├── com-crowdstrike-falcon.mobileconfig               # CrowdStrike Falcon
├── com-dare-zappl-preferences.mobileconfig           # Zappl preferences
├── com-docker-config.mobileconfig                    # Docker Desktop
├── com-fxfactory-fxfactory.mobileconfig              # FxFactory
├── com-github-ants-framework.mobileconfig            # ANTS framework
├── com-github-macadmins-nudge.mobileconfig           # Nudge
├── com-github-macadmins-supportcompanion.mobileconfig # Support Companion
├── com-github-mpanighetti-install-or-defer.mobileconfig      # Install or Defer
├── com-github-wavebirddash-install-or-defer.mobileconfig     # Install or Defer (Wavebird)
├── com-google-chrome.mobileconfig                    # Google Chrome
├── com-google-drivefs-settings.mobileconfig          # Google Drive
├── com-google-keystone.mobileconfig                  # Google Keystone (auto-update)
├── com-grahamgilbert-crypt.mobileconfig              # Crypt (FileVault escrow)
├── com-grammarly-projectllama.mobileconfig           # Grammarly
├── com-hjuutilainen-munkiadmin.mobileconfig          # MunkiAdmin
├── com-jamf-setupmanager.mobileconfig                # Jamf Setup Manager
├── com-jelockwood-pinpoint.mobileconfig              # Pinpoint
├── com-jigsaw24-elevate24.mobileconfig               # Elevate24
├── com-jigsaw24-elevate24securityextension.mobileconfig # Elevate24 Security Extension
├── com-keepersecurity-passwordmanager.mobileconfig   # Keeper Password Manager
├── com-macjutsu-super.mobileconfig                   # S.U.P.E.R.M.A.N (super)
├── com-macpaw-site-theunarchiver.mobileconfig        # The Unarchiver (MacPaw)
├── com-mcneel-rhinoceros.mobileconfig                # Rhinoceros 3D
├── com-microsoft-autoupdate-fba.mobileconfig         # Microsoft AutoUpdate (FBA)
├── com-microsoft-autoupdate2.mobileconfig            # Microsoft AutoUpdate
├── com-microsoft-edge.mobileconfig                   # Microsoft Edge
├── com-microsoft-errorreporting.mobileconfig         # Microsoft Error Reporting
├── com-microsoft-excel.mobileconfig                  # Microsoft Excel
├── com-microsoft-office.mobileconfig                 # Microsoft Office (suite-wide)
├── com-microsoft-office365servicev2.mobileconfig     # Microsoft 365 service
├── com-microsoft-onedrive.mobileconfig               # Microsoft OneDrive
├── com-microsoft-onedriveupdater.mobileconfig        # OneDrive Updater
├── com-microsoft-onenote-mac.mobileconfig            # Microsoft OneNote
├── com-microsoft-outlook.mobileconfig                # Microsoft Outlook
├── com-microsoft-powerpoint.mobileconfig             # Microsoft PowerPoint
├── com-microsoft-rdc-macos.mobileconfig              # Microsoft Remote Desktop
├── com-microsoft-skypeforbusiness.mobileconfig       # Skype for Business
├── com-microsoft-wdav.mobileconfig                   # Microsoft Defender Antivirus
├── com-microsoft-word.mobileconfig                   # Microsoft Word
├── com-northpolesec-santa.mobileconfig               # Santa (binary allowlisting)
├── com-okta-mobile-auth-service-extension.mobileconfig # Okta Mobile Auth Extension
├── com-okta-mobile.mobileconfig                      # Okta Mobile
├── com-papercut-printdeploy-client.mobileconfig      # PaperCut Print Deploy
├── com-pratikkumar-airserver-mac.mobileconfig        # AirServer
├── com-profilecreator-developer-slider.mobileconfig           # ProfileCreator slider example
├── com-profilecreator-developer-textfieldfloat.mobileconfig   # ProfileCreator float field example
├── com-profilecreator-developer-textfieldinteger.mobileconfig # ProfileCreator integer field example
├── com-secondsonconsulting-baseline.mobileconfig     # Baseline
├── com-secondsonconsulting-renew.mobileconfig        # Renew
├── com-sentinelone-registration-token.mobileconfig   # SentinelOne registration token
├── com-sqwarq-detectx-swift.mobileconfig             # DetectX Swift
├── com-thomsonresearchsoft-endnote.mobileconfig      # EndNote
├── com-tinyspeck-slackmacgap.mobileconfig            # Slack
├── com-todesktop-230313mzl4w4u92.mobileconfig        # Linear
├── com-trusourcelabs-nomad.mobileconfig              # NoMAD
├── com-twingate-macos.mobileconfig                   # Twingate
├── com-twocanoes-xcreds.mobileconfig                 # XCreds
├── com-unity3d-unityeditor5-x.mobileconfig           # Unity Editor
├── com-vpntracker-365mac.mobileconfig                # VPN Tracker 365
├── com-zappl-appbar.mobileconfig                     # Zappl App Bar
├── com-zscaler-installparams.mobileconfig            # Zscaler
├── corp-sap-privileges.mobileconfig                  # SAP Privileges
├── cx-c3-theunarchiver.mobileconfig                  # The Unarchiver (cx.c3)
├── de-fau-rrze-networksharemounter.mobileconfig      # Network Share Mounter
├── dev-firezone-firezone.mobileconfig                # Firezone VPN
├── edu-ncsu-confboard.mobileconfig                   # ConfBoard
├── edu-psu-macoslaps.mobileconfig                    # macOS LAPS
├── io-macadmins-outset.mobileconfig                  # Outset
├── io-tailscale-ipn-macos.mobileconfig               # Tailscale (app)
├── io-tailscale-ipn-macsys.mobileconfig              # Tailscale (system extension)
├── managedinstalls.mobileconfig                      # Munki managed installs
├── menu-nomad-nomadpro.mobileconfig                  # NoMAD Pro
├── munkireport.mobileconfig                          # MunkiReport
├── net-glencode-particulars-widget.mobileconfig      # Particulars widget
├── net-glencode-particulars.mobileconfig             # Particulars
├── nl-root3-support.mobileconfig                     # Root3 Support App
├── notion-id.mobileconfig                            # Notion
├── org-churchofjesuschrist-dorm.mobileconfig         # DORM
├── org-mozilla-firefox.mobileconfig                  # Mozilla Firefox
├── org-videolan-vlc.mobileconfig                     # VLC
├── supportcompanion.mobileconfig                     # Support Companion (legacy domain)
├── uk-co-datajar-jamjar.mobileconfig                 # Jamjar
├── us-zoom-config.mobileconfig                       # Zoom
└── xyz-techitout-appautopatch.mobileconfig           # App Auto-Patch
```

#### `profiles/prefs/` — macOS system and Apple app preferences

Managed preferences for macOS system services and built-in Apple apps.

```
profiles/prefs/
├── accessibility.mobileconfig                        # Accessibility settings
├── adlib.mobileconfig                                # Ad library settings
├── assistant-support.mobileconfig                    # Siri / Assistant support
├── compressor.mobileconfig                           # Compressor
├── controlcenter.mobileconfig                        # Control Center
├── coreservices-uiagent.mobileconfig                 # CoreServices UI Agent
├── desktopservices.mobileconfig                      # Desktop Services (.DS_Store behaviour)
├── dt-xcode.mobileconfig                             # Xcode
├── enterprise-connect.mobileconfig                   # Enterprise Connect
├── finalcut.mobileconfig                             # Final Cut Pro
├── freeform.mobileconfig                             # Freeform
├── garageband10.mobileconfig                         # GarageBand
├── ibooksx.mobileconfig                              # Books
├── icloud-managed.mobileconfig                       # iCloud (managed)
├── imovieapp.mobileconfig                            # iMovie
├── itunes.mobileconfig                               # iTunes / Music
├── logic10.mobileconfig                              # Logic Pro
├── mdnsresponder.mobileconfig                        # mDNS Responder (Bonjour)
├── motionapp.mobileconfig                            # Motion
├── networkbrowser.mobileconfig                       # Network Browser
├── preferences-sharing-sharingprefsextension.mobileconfig  # Sharing preferences pane
├── print-add.mobileconfig                            # Printer addition
├── safari-sandboxbroker.mobileconfig                 # Safari sandbox broker
├── safari.mobileconfig                               # Safari
├── screencapture.mobileconfig                        # Screenshot settings
├── security.mobileconfig                             # Security settings
├── sharingd.mobileconfig                             # Sharing daemon
├── siri.mobileconfig                                 # Siri
├── spotlight.mobileconfig                            # Spotlight
├── terminal.mobileconfig                             # Terminal
├── textedit.mobileconfig                             # TextEdit
├── timed.mobileconfig                                # Time daemon (timed)
└── timemachine.mobileconfig                          # Time Machine
```

## References

- [Apple Declarative Device Management](https://developer.apple.com/documentation/devicemanagement/declarativedevicemanagement)
- [Apple Configuration Profile Reference](https://developer.apple.com/documentation/devicemanagement/configuration_profiles)
- [MDM Protocol Reference](https://developer.apple.com/documentation/devicemanagement)
