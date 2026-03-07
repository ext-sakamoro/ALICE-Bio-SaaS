# ALICE-Bio SaaS

Molecular structure and protein folding SDF API

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-Bio |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/fold` | タンパク質折りたたみ予測 |
| `POST /api/v1/energy` | 分子エネルギー計算 |
| `POST /api/v1/validate` | 構造バリデーション |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
