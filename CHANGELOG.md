# CHANGELOG
All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html). See the [CONTRIBUTING guide](./CONTRIBUTING.md#Changelog) for instructions on how to add changelog entries.

## [Unreleased 2.x]
### Added
- Add support for async deletion in S3BlobContainer ([#15621](https://github.com/opensearch-project/OpenSearch/pull/15621))
- MultiTermQueries in keyword fields now default to `indexed` approach and gated behind cluster setting ([#15637](https://github.com/opensearch-project/OpenSearch/pull/15637))
- [Workload Management] Add Integration Tests for Workload Management CRUD APIs ([#15955](https://github.com/opensearch-project/OpenSearch/pull/15955))
- [Workload Management] QueryGroup resource cancellation framework changes ([#15651](https://github.com/opensearch-project/OpenSearch/pull/15651))
- [Workload Management] Add orchestrator for wlm resiliency (QueryGroupService) ([#15925](https://github.com/opensearch-project/OpenSearch/pull/15925))
- [Workload Management] Add QueryGroup Stats API Logic ([15777](https://github.com/opensearch-project/OpenSearch/pull/15777))
- Fallback to Remote cluster-state on Term-Version check mismatch - ([#15424](https://github.com/opensearch-project/OpenSearch/pull/15424))
- Implement WithFieldName interface in ValuesSourceAggregationBuilder & FieldSortBuilder ([#15916](https://github.com/opensearch-project/OpenSearch/pull/15916))
- Add successfulSearchShardIndices in searchRequestContext ([#15967](https://github.com/opensearch-project/OpenSearch/pull/15967), [#16110](https://github.com/opensearch-project/OpenSearch/pull/16110))
- [Tiered Caching] Segmented cache changes ([#16047](https://github.com/opensearch-project/OpenSearch/pull/16047))
- Add support for msearch API to pass search pipeline name - ([#15923](https://github.com/opensearch-project/OpenSearch/pull/15923))
- Add _list/indices API as paginated alternate to _cat/indices ([#14718](https://github.com/opensearch-project/OpenSearch/pull/14718))
- Add success and failure metrics for async shard fetch ([#15976](https://github.com/opensearch-project/OpenSearch/pull/15976))
- Add new metric REMOTE_STORE to NodeStats API response ([#15611](https://github.com/opensearch-project/OpenSearch/pull/15611))
- [S3 Repository] Change default retry mechanism of s3 clients to Standard Mode ([#15978](https://github.com/opensearch-project/OpenSearch/pull/15978))
- Add changes to block calls in cat shards, indices and segments based on dynamic limit settings ([#15986](https://github.com/opensearch-project/OpenSearch/pull/15986))
- New `phone` & `phone-search` analyzer + tokenizer ([#15915](https://github.com/opensearch-project/OpenSearch/pull/15915))
- Add _list/shards API as paginated alternate to _cat/shards ([#14641](https://github.com/opensearch-project/OpenSearch/pull/14641))
- Latency and Memory allocation improvements to Multi Term Aggregation queries ([#14993](https://github.com/opensearch-project/OpenSearch/pull/14993))
- Flat object field use IndexOrDocValuesQuery to optimize query ([#14383](https://github.com/opensearch-project/OpenSearch/issues/14383))

### Dependencies
- Bump `com.azure:azure-identity` from 1.13.0 to 1.13.2 ([#15578](https://github.com/opensearch-project/OpenSearch/pull/15578))
- Bump `protobuf` from 3.22.3 to 3.25.4 ([#15684](https://github.com/opensearch-project/OpenSearch/pull/15684))
- Bump `org.apache.logging.log4j:log4j-core` from 2.23.1 to 2.24.1 ([#15858](https://github.com/opensearch-project/OpenSearch/pull/15858), [#16134](https://github.com/opensearch-project/OpenSearch/pull/16134))
- Bump `peter-evans/create-pull-request` from 6 to 7 ([#15863](https://github.com/opensearch-project/OpenSearch/pull/15863))
- Bump `com.nimbusds:oauth2-oidc-sdk` from 11.9.1 to 11.19.1 ([#15862](https://github.com/opensearch-project/OpenSearch/pull/15862))
- Bump `com.microsoft.azure:msal4j` from 1.17.0 to 1.17.1 ([#15945](https://github.com/opensearch-project/OpenSearch/pull/15945))
- Bump `ch.qos.logback:logback-core` from 1.5.6 to 1.5.10 ([#15946](https://github.com/opensearch-project/OpenSearch/pull/15946), [#16307](https://github.com/opensearch-project/OpenSearch/pull/16307))
- Update protobuf from 3.25.4 to 3.25.5 ([#16011](https://github.com/opensearch-project/OpenSearch/pull/16011))
- Bump `org.roaringbitmap:RoaringBitmap` from 1.2.1 to 1.3.0 ([#16040](https://github.com/opensearch-project/OpenSearch/pull/16040))
- Bump `com.nimbusds:nimbus-jose-jwt` from 9.40 to 9.41.1 ([#16038](https://github.com/opensearch-project/OpenSearch/pull/16038))
- Bump `actions/github-script` from 5 to 7 ([#16039](https://github.com/opensearch-project/OpenSearch/pull/16039))
- Bump `dnsjava:dnsjava` from 3.6.1 to 3.6.2 ([#16041](https://github.com/opensearch-project/OpenSearch/pull/16041))
- Bump `com.maxmind.geoip2:geoip2` from 4.2.0 to 4.2.1 ([#16042](https://github.com/opensearch-project/OpenSearch/pull/16042))
- Bump `com.maxmind.db:maxmind-db` from 3.1.0 to 3.1.1 ([#16137](https://github.com/opensearch-project/OpenSearch/pull/16137))
- Bump Apache lucene from 9.11.1 to 9.12.0 ([#15333](https://github.com/opensearch-project/OpenSearch/pull/15333))
- Bump `com.azure:azure-core-http-netty` from 1.15.3 to 1.15.5 ([#16133](https://github.com/opensearch-project/OpenSearch/pull/16133), [#16311](https://github.com/opensearch-project/OpenSearch/pull/16311))
- Bump `org.jline:jline` from 3.26.3 to 3.27.0 ([#16135](https://github.com/opensearch-project/OpenSearch/pull/16135))
- Bump `netty` from 4.1.112.Final to 4.1.114.Final ([#16182](https://github.com/opensearch-project/OpenSearch/pull/16182))
- Bump `com.google.api-client:google-api-client` from 2.2.0 to 2.7.0 ([#16216](https://github.com/opensearch-project/OpenSearch/pull/16216))
- Bump `com.azure:azure-json` from 1.1.0 to 1.3.0 ([#16217](https://github.com/opensearch-project/OpenSearch/pull/16217))
- Bump `io.grpc:grpc-api` from 1.57.2 to 1.68.0 ([#16213](https://github.com/opensearch-project/OpenSearch/pull/16213))
- Bump `com.squareup.okio:okio` from 3.9.0 to 3.9.1 ([#16212](https://github.com/opensearch-project/OpenSearch/pull/16212))
- Bump `me.champeau.gradle.japicmp` from 0.4.3 to 0.4.4 ([#16309](https://github.com/opensearch-project/OpenSearch/pull/16309))
- Bump `com.google.oauth-client:google-oauth-client` from 1.35.0 to 1.36.0 ([#16306](https://github.com/opensearch-project/OpenSearch/pull/16306))
- Bump `lycheeverse/lychee-action` from 1.10.0 to 2.0.2 ([#16310](https://github.com/opensearch-project/OpenSearch/pull/16310))
- Bump `com.google.code.gson:gson` from 2.10.1 to 2.11.0 ([#16308](https://github.com/opensearch-project/OpenSearch/pull/16308))

### Changed
- Add support for docker compose v2 in TestFixturesPlugin ([#16049](https://github.com/opensearch-project/OpenSearch/pull/16049))
- Remove identity-related feature flagged code from the RestController ([#15430](https://github.com/opensearch-project/OpenSearch/pull/15430))
- Remove Identity FeatureFlag ([#16024](https://github.com/opensearch-project/OpenSearch/pull/16024))
- Ensure RestHandler.Wrapper delegates all implementations to the wrapped handler ([#16154](https://github.com/opensearch-project/OpenSearch/pull/16154))
- Enable coordinator search.request_stats_enabled by default ([#16290](https://github.com/opensearch-project/OpenSearch/pull/16290))
- Code cleanup: Remove ApproximateIndexOrDocValuesQuery ([#16273](https://github.com/opensearch-project/OpenSearch/pull/16273))
- Optimise clone operation for incremental full cluster snapshots ([#16296](https://github.com/opensearch-project/OpenSearch/pull/16296))

### Deprecated

### Removed

### Fixed
- Fix wildcard query containing escaped character ([#15737](https://github.com/opensearch-project/OpenSearch/pull/15737))
- Fix case-insensitive query on wildcard field ([#15882](https://github.com/opensearch-project/OpenSearch/pull/15882))
- Add validation for the search backpressure cancellation settings ([#15501](https://github.com/opensearch-project/OpenSearch/pull/15501))
- Fix search_as_you_type not supporting multi-fields ([#15988](https://github.com/opensearch-project/OpenSearch/pull/15988))
- Avoid infinite loop when `flat_object` field contains invalid token ([#15985](https://github.com/opensearch-project/OpenSearch/pull/15985))
- Fix infinite loop in nested agg ([#15931](https://github.com/opensearch-project/OpenSearch/pull/15931))
- Fix update settings with null replica not honoring cluster setting bug ([#14948](https://github.com/opensearch-project/OpenSearch/pull/14948))
- Fix race condition in node-join and node-left ([#15521](https://github.com/opensearch-project/OpenSearch/pull/15521))
- Streaming bulk request hangs ([#16158](https://github.com/opensearch-project/OpenSearch/pull/16158))
- Fix warnings from SLF4J on startup when repository-s3 is installed ([#16194](https://github.com/opensearch-project/OpenSearch/pull/16194))
- Document running remote backed storage in dev environment ([#16223](https://github.com/opensearch-project/OpenSearch/pull/16223))
- Fix protobuf-java leak through client library dependencies ([#16254](https://github.com/opensearch-project/OpenSearch/pull/16254))
- Fix multi-search with template doesn't return status code ([#16265](https://github.com/opensearch-project/OpenSearch/pull/16265))

### Security

[Unreleased 2.x]: https://github.com/opensearch-project/OpenSearch/compare/2.17...2.x
