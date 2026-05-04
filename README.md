# Control Room Python SDK

Python client for the [Control Room API](https://getcontrolroom.com). Generated from `spec/openapi.yaml` using [Fern](https://buildwithfern.com).

## Installation

```bash
pip install getcontrolroom
```

## Quick Start

```python
from getcontrolroom import ControlRoomClient

client = ControlRoomClient(
    base_url="https://api.getcontrolroom.com",
    token="your-token",
)

bookings = client.bookings.list()
```

## Auth

**Service-to-service** (app → api):

```python
client = ControlRoomClient(
    base_url="https://api.getcontrolroom.com",
    user_id="usr_...",
    service_secret="secret",
)
```

**Bearer token**:

```python
client = ControlRoomClient(
    base_url="https://api.getcontrolroom.com",
    token="your-bearer-token",
)
```

## Regenerating

Requires [fern](https://buildwithfern.com) and the spec at `../spec/openapi.yaml`.

```bash
bun add --global fern-api
cd ../fern && fern generate --local
```

## License

MIT — see [LICENSE](LICENSE).

---

Built by [Control Room](https://getcontrolroom.com) · Developed by [Clover Labs](https://cloverlabs.io)
