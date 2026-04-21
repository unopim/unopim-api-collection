# UnoPim Official API Collection

[![Run in Postman](https://run.pstmn.io/button.svg)](https://www.postman.com/unopim/unopim-apis)

Official Postman collection for the [UnoPim](https://unopim.com) REST API, open-source PIM system.

## What's Included

| Resource | Methods |
|---|---|
| Authentication | Password grant, Refresh token |
| Locale | List, Get by code |
| Currency | List, Get by code |
| Channel | List, Get by code |
| Category | List, Get, Create, Update, Delete, Partial Update, Upload media |
| Category Fields | List, Get, Create, Update |
| Category Field Options | List, Create, Update |
| Attribute | List, Get, Create, Update |
| Attribute Options | List, Create, Update, Upload swatch media |
| Attribute Groups | List, Get, Create, Update |
| Attribute Families | List, Get, Create, Update |
| Product (Simple) | List, Get, Create, Update, Delete, Partial Update |
| Product (Configurable) | List, Get, Create, Update, Partial Update, Add variant, Upload media |

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
| `url` | Your UnoPim instance URL (e.g. `http://localhost:8000`) |
| `clientId` | OAuth client ID from UnoPim admin |
| `secret` | OAuth client secret from UnoPim admin |
| `username` | Admin email (e.g. `admin@example.com`) |
| `password` | Admin password |
| `token` | Auto-filled after running the Auth request |
| `refreshToken` | Auto-filled after running the Auth request |

### 3. Authenticate

Run the **Authentication by password** request first — it will auto-set `token` and `refreshToken` in your environment.

## Contributing

We welcome contributions! To add or update API requests:

1. Fork this repository
2. Import the collection + environment into your local Postman
3. Make your changes in Postman → export the updated collection JSON
4. Replace `collections/Official-UnoPim-APIs.postman_collection.json` with the new export
5. Open a Pull Request with a clear description of what changed

Once merged, the **Push to Postman** GitHub Action automatically syncs the updated collection to the official Postman workspace.

## Workflows

| Workflow | Trigger | Direction |
|---|---|---|
| **Push Collection to Postman** | On push to `main` (collection file changed) | GitHub → Postman |
| **Sync Postman Collection** | On GitHub Release published | Postman → GitHub |

## Links

- [UnoPim Website](https://unopim.com)
- [UnoPim Documentation](https://docs.unopim.com)
- [UnoPim GitHub](https://github.com/unopim/unopim)
- [Postman Workspace](https://www.postman.com/unopim/unopim-apis)
