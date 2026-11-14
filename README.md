# dev_purpose_of_alpaca-trad
Dev purpose
- Automated Trading System / Algorithmic Trading Bot
- REST API & amp
- WebSocket Streaming
- Risk Management / Position Sizing
- Order Management System (OMS)
- Event-Driven Architecture
- Fractional Trading
- SDK (Software Development Kit)
- 24/5 Trading
- Alpaca API
- Broker API

---

# Alpaca & MT5 Trading Bot

Alpaca API（株・暗号資産）と MetaTrader 5（FX）を統合した自動売買プロジェクト

## Tech Stack

| 用途 | 言語 / ツール |
|------|-------------|
| 株・暗号資産 | Python + Alpaca SDK |
| FX | MQL5 (MetaTrader 5) |
| 戦略共通 | Python (pandas, numpy) |

## 環境構築

### Python

```bash
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 環境変数

`.env` を作成（`.env.example` をコピー）：

```env
ALPACA_API_KEY=
ALPACA_SECRET_KEY=
ALPACA_PAPER=True
MT5_LOGIN=
MT5_PASSWORD=
MT5_SERVER=
```

> ⚠️ `.env` はコミットしないこと。

## ディレクトリ構成

```
.
├── alpaca/          # Alpaca 用ボット
├── mt5/             # MT5 EA / スクリプト
├── strategies/      # 共通戦略ロジック
├── data/            # 取得データ（gitignore）
├── outputs/         # バックテスト結果（gitignore）
├── .env             # 秘密情報（gitignore）
├── .env.example     # 雛形
├── requirements.txt
└── README.md
```

## 使い方

```bash
# Alpaca ボット実行
python alpaca/main.py

# MT5 EA は MetaTrader 5 上で .mq5 をコンパイル
```

## License

MIT
```

必要に応じて `## 使い方` やディレクトリ構成を調整してください。
`requirements.txt` も忘れずにコミットしておくと、他者（または将来の自分）が即再現できます。

---


