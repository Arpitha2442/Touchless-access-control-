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

# Tech Stack

## Frontend & Users
- Mobile App (User access interface)
- Admin Dashboard (Access management)
- Access Point Emulator (Face capture)

## Backend & Services

- Azure Functions (Serverless logic)
- Azure Face API (Identity verification)
- Azure Cosmos DB (Data storage)


## Outcome

Smart Lock (Controlled via backend signal)
Access decision indicators (Green/Red)

## Architecture Flow

1. User opens the Mobile App → sends access request.

2. Access Point Emulator captures face image → sends to backend.

3. Azure Functions Backend receives requests and calls:
- Face API for verification.
- Cosmos DB for access validation.

4. Backend decides → sends signal to Smart Lock:
- Access Granted → unlocks.
- Access Denied → stays locked.

5. Exception handling triggers for failures (face mismatch, DB error).
