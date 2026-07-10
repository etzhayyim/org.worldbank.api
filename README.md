# org.worldbank.api

`api.worldbank.org` の World Development Indicators API から取得した、全世界のエネルギー指標 snapshot を保全する DataLad dataset です。統合用 datom は `etzhayyim/global-energy-datoms` が生成します。

各 raw JSON は API 応答をそのまま保存し、`raw/source-catalog.edn` に指標コード・観測年・SHA-256 を記録します。WDI 指標ごとに最新利用可能年が異なるため、消費側は `:energy/year` を必ず条件に含めます。
