# fizz-llm-client

**Fizz** (AITuber system in [Almide](https://github.com/almide/almide)) — §3 brain 部品。

マルチプロバイダ LLM クライアント (almai 互換 interface を stdlib http.request で実装)。`call_with` / `Message` / `LLMResponse` / provider 解析 / body 構築 / レスポンス解析。**almai が現行 almide で壊れているための代替**で、almai 修正後は drop-in 置換可能。

責務は一行で、入力 → 出力が型で言い切れる単位 (openaituber `docs/almide-component-breakdown.md` §3)。

## Install

```toml
[dependencies]
fizz_llm_client = { git = "https://github.com/Aid-On/fizz-llm-client", tag = "v0.1.0" }
```

## Tests

```bash
almide test
```

純ロジックなのでネットワーク・API キー不要でテストできる。
