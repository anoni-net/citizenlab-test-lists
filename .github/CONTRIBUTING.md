# 參與貢獻 | Contributing

**正體中文** | [English](#english)

這是匿名網路社群 anoni.net 維護的 [citizenlab/test-lists](https://github.com/citizenlab/test-lists) fork，用來整理台灣的網址檢測清單 `lists/tw.csv`，整理好的內容會送回上游。清單的格式與分類見上游的 README。

## 提供網址

- **零星補件**：直接用 OONI 的[網頁介面](https://test-lists.ooni.org/)提交，不必經過這個 fork。提交方式見 OONI 的[說明](https://ooni.org/get-involved/contribute-test-lists/)
- **一批台灣的網址**：在社群的 Matrix 討論，或寄信到 whisper@anoni.net。帳號與使用方式見[社群自架服務](https://anoni.net/docs/community/tools/)

這個 fork 沒有開 issue。

## 協作者的流程

1. 從上游的 `master`（`citizenlab/test-lists`）開分支，不要從 fork 的 `master` 開。fork 的 `master` 多了參與說明等只屬於 fork 的檔案，從它開分支會把多出來的檔案帶進送給上游的 PR
2. 內部審查推到社群約定的審查分支，例如 `tw-highweight-2026`
3. 改了 `lists/` 底下的檔案之後，執行 `python3 scripts/lint-lists.py lists/`，CI 也會執行同一支檢查
4. 審查完成後，批次 PR 送到 `citizenlab/test-lists` 的 `master`，不要送到 `ooni/test-lists`

---

## English

[正體中文](#參與貢獻--contributing) | **English**

This is the anoni.net community's fork of [citizenlab/test-lists](https://github.com/citizenlab/test-lists), where we maintain the Taiwan URL test list `lists/tw.csv` before submitting it upstream. See the upstream README for the list format and categories.

### Suggesting URLs

- **A few URLs**: submit them directly through OONI's [web interface](https://test-lists.ooni.org/); there is no need to go through this fork. See OONI's [guide](https://ooni.org/get-involved/contribute-test-lists/) for how
- **A batch of Taiwan URLs**: raise it on our Matrix or email whisper@anoni.net. See [our self-hosted services](https://anoni.net/docs/en/community/tools/) for Matrix accounts and usage

Issues are not enabled on this fork.

### Workflow for collaborators

1. Branch from upstream `master` (`citizenlab/test-lists`), not from this fork's `master`. The fork's `master` carries fork-only files such as this guide, and branching from it would bring them into the pull request sent upstream
2. Push internal review work to the community's agreed review branch, such as `tw-highweight-2026`
3. After changing anything under `lists/`, run `python3 scripts/lint-lists.py lists/`; CI runs the same check
4. Once reviewed, send batch pull requests to `master` on `citizenlab/test-lists`, not to `ooni/test-lists`
