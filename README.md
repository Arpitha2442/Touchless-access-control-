# Touchless-access-control-
# Touchless Access Control – Mobile-First Prototype

A mobile-first, PWA-ready prototype for *touchless access control* using:
- WebAuthn (passkeys) for device authentication
- WebCrypto (ECDSA) for local signing
- Geofencing (GPS) + simulated BLE presence
- Dynamic QR token OR direct transmission to controller
- Door controller simulator for debugging

## Features
- Register device with passkey (fallback supported)
- Generate and verify signed access tokens
- Unlock modes: *Direct* (simulated BLE/NFC) or *QR*
- Controller simulator verifies signature, TTL, and geofence
