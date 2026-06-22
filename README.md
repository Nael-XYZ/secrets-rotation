# Secrets Rotation 🔄

Automated zero-downtime secrets rotation for databases, API keys, and certificates.

## Supported Secrets

| Secret | Method | Downtime |
|--------|--------|----------|
| DB Password | Dual-write | Zero |
| API Key | Rolling | Zero |
| TLS Cert | cert-manager | Zero |

## Quick Start

```python
from secrets_rotation import Rotator

rotator = Rotator(vault_url="https://vault.internal:8200")
rotator.rotate_db_password("production/db/password")
rotator.rotate_api_key("production/api/stripe")
```

## License

MIT