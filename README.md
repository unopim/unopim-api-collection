# UnoPim Official API Collection

[![Run in Postman](https://run.pstmn.io/button.svg)](https://www.postman.com/unopim/unopim-apis)

Official Postman collection for the [UnoPim](https://unopim.com) REST API — a headless, open-source PIM system.

## What's Included

| Resource | Methods |
|---|---|
| Authentication | Password grant, Refresh token |
| Locale | List, Get by code |
| Currency | List, Get by code |
| Channel | List, Get by code |
| Category | List, Get, Create, Update, Upload media |
| Category Fields | List, Get, Create, Update |
| Category Field Options | List, Create, Update |
| Attribute | List, Get, Create, Update |
| Attribute Options | List, Create, Update |
| Attribute Groups | List, Get, Create, Update |
| Attribute Families | List, Get, Create, Update |
| Product (Simple) | List, Get, Create, Update |
| Product (Configurable) | List, Get, Create, Update, Add variant, Upload media |

## Getting Started

### 1. Import the Collection

Click the **Run in Postman** button above, or manually import:

1. Download `collections/Official-UnoPim-APIs.postman_collection.json`
2. In Postman → **Import** → select the file

### 2. Import the Environment

1. Download `environments/UnoPim-Local.postman_environment.json`
2. In Postman → **Environments** → **Import** → select the file
3. Fill in your values:

| Variable | Description |
|---|---|
| `base_url` | Your UnoPim instance URL (e.g. `http://localhost:8000`) |
| `client_id` | OAuth client ID from UnoPim admin |
| `client_secret` | OAuth client secret from UnoPim admin |
| `access_token` | Auto-filled after running the Auth request |
| `refresh_token` | Auto-filled after running the Auth request |

### 3. Authenticate

Run the **Authentication by password** request first — it will auto-set `access_token` and `refresh_token` in your environment.

## Contributing

We welcome contributions! To add or update API requests:

1. Fork this repository
2. Import the collection + environment into your local Postman
3. Make your changes in Postman → export the updated collection JSON
4. Replace `collections/Official-UnoPim-APIs.postman_collection.json` with the new export
5. Open a Pull Request with a clear description of what changed

The maintainers will review and merge — the GitHub Action will then auto-sync the latest collection to the official Postman workspace daily.

## Auto-Sync

This repo uses a GitHub Action (`.github/workflows/sync-postman.yml`) to pull the latest collection from the Postman API every day at midnight UTC, keeping GitHub and Postman always in sync.

## Links

- [UnoPim Website](https://unopim.com)
- [UnoPim Documentation](https://docs.unopim.com)
- [UnoPim GitHub](https://github.com/unopim/unopim)
- [Postman Workspace](https://www.postman.com/unopim/unopim-apis)
