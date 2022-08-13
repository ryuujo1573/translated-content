---
title: Pragma
slug: Web/HTTP/Headers/Pragma
tags:
  - Caching
  - Deprecated
  - HTTP
  - ヘッダー
  - リクエスト
translation_of: Web/HTTP/Headers/Pragma
---
{{HTTPSidebar}}

**`Pragma`** は HTTP/1.0 の一般ヘッダーで、実装固有のヘッダーであり、リクエスト - レスポンスチェーンに沿ってさまざまな影響を与えます。 `Cache-Control` HTTP/1.1 ヘッダーがまだ存在しない HTTP/1.0 キャッシュとの下位互換性のために使用されます。

> **Note:** **メモ**: `Pragma` は HTTP レスポンスには指定されていないため、リクエストの `Cache-Control` ヘッダーフィールドが省略されている場合は `Cache-Control: no-cache` と同じように動作しますが、一般的な HTTP/1.1 `Cache-Control` ヘッダーの代わりに信頼できるものではありません。`Pragma` は HTTP/1.0 クライアントとの下位互換性のためにのみ使用してください。

| ヘッダー種別                                                                                                                             | {{Glossary("General header", "一般ヘッダー")}}, ただしレスポンスの振る舞いは指定されていないため、実装固有です。 |
| ---------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| {{Glossary("Forbidden header name", "禁止ヘッダー名")}}                                                     | いいえ                                                                                                                                 |
| {{Glossary("CORS-safelisted response header", "CORS セーフリストレスポンスヘッダー")}} | はい                                                                                                                                   |

## 構文

    Pragma: no-cache

## ディレクティブ

- no-cache
  - : `Cache-Control: no-cache` と同じです。キャッシュされたコピーを解放する前に、キャッシュが検証のためにオリジンサーバーにリクエストを送信するようにします。

## 例

    Pragma: no-cache

## 仕様書

| 仕様書                                       | 題名                                            |
| -------------------------------------------- | ----------------------------------------------- |
| {{RFC("7234", "Pragma", "5.4")}} | Hypertext Transfer Protocol (HTTP/1.1): Caching |

## ブラウザーの互換性

{{Compat("http.headers.Pragma")}}

## 関連情報

- {{HTTPHeader("Cache-Control")}}
- {{HTTPHeader("Expires")}}