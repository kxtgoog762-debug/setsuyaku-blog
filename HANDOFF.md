# 🔄 引き継ぎ書｜ゆる節約ライフ（2026-06-28更新）

新しいセッションはこれを最初に読めば即続行できます。詳細履歴は `autonomous-pdca-log.txt`、
運用ルールは `autonomous-pdca.md`、戦略はメモリ `project_setsuyaku_blog_strategy.md` 参照。
オーナーは **太田賢吾（おおた けんご）さん**。非エンジニア。専門用語は避け平易な日本語で。リスクは先に指摘する。

---

## 0. プロジェクト概要
- ブログ「ゆる節約ライフ」https://yuru-setsuyaku.com （20代一人暮らしの節約・新NISA）
- 構成：Hugo + PaperMod / Cloudflare Pages（git push→自動デプロイ）/ 本番ブランチ master
- 作業ディレクトリ：`/Users/ootakengo/作業フォルダ/setsuyaku-blog`
- リポジトリ：`github.com:kxtgoog762-debug/setsuyaku-blog.git`（Private）
- 記事数：100本。キャラ：やっとかめ（先輩）× まなぶくん（後輩）の会話。筆者設定=28歳・資産2000万・35歳FIRE目標・宅建/FP3級保有

---

## 1. 🔴 いま進行中の案件（ここから続ける）

### A. 保険アフィリリンクの挿入（A8審査中＝承認待ち）★最優先で見る
- 対象記事：[content/posts/20dai-hoken-minaoshi.md](content/posts/20dai-hoken-minaoshi.md)「20代独身男に生命保険はほぼ不要だった話」
- 方針（太田さんと合意）：記事は「保険不要」論旨なので**生命保険加入リンクはNG**。代わりに**「保険の無料見直し相談」**アフィリを入れる（論旨と一致）。
- A8プログラム：**保険の見直しなら【保険見直し本舗】**（プログラムID `s00000027364001`／成果報酬 新規相談実施 **15,384円**）。
- 状態：**2026/06/23 に提携申請済み → A8で「申込中（審査中）」**。承認されると「参加プログラム」に移り**広告リンク**取得可。**取消ボタンは押さない**。
- **承認後の手順**：太田さんがA8で「広告リンク→テキスト」のコードを取得しチャットに貼る → 私が `px.a8.net/...` のhrefを抜き出し、下記CTAに入れて記事に挿入→commit。
- **挿入位置**：`## 公的保障を知れば、民間保険は最小限でいい` セクションの直後（「勧められるまま入る必要はありません。」の後）。
- **用意済みCTA文面**（hrefだけ差し込む。既存の`aff-btn`スタイル＋`rel="nofollow sponsored noopener"`）：
  > とはいえ「今の保険が過剰か足りないか」は自分では判断しづらい。中立のFPに無料で見直してもらうのが手っ取り早い…（前後の導入文込み）
  > `<a href="【px.a8.netの広告URL】" class="aff-btn aff-btn-primary" target="_blank" rel="nofollow sponsored noopener"><span class="aff-btn-main">無料で保険を見直してみる</span><span class="aff-btn-sub">中立のFPに相談・オンライン対応・相談だけでもOK</span></a>`
- 予備：審査落ちに備え「マネードクター」等の別の保険相談プログラムにも申請しておくと安心（未実施）。

### B. X（@yuru_setsuyaku）投稿の継続
- **投稿済み7本**：固定ツイート(ピン留め済)／#1格安SIM／#2リボ払い／B1あるある／A1投票／#3手取り20万／#6貯金危機（〜6/19）。
- **次に出す順番**＝[Xの次の投稿キュー.md](Xの次の投稿キュー.md)（上から：🔥S1夏ボーナス→B3→#4→C1→#5保険後悔→A2投票→P1→#7…）。本文は各 `x-*.md` からコピペ。
- 運用：1日1〜2本。リンク有(ブログ誘導)と無(交流)を交互。3:5:2バランス。数字公開は `x-number-templates.md` に**本人が実額記入**。
- **⚠️ ブラウザ接続が課題**（下記4参照）。接続できれば私が投稿、できなければ本人がコピペ。

### C. 週次レポート（6/16以降 未作成）
- 既存：`weekly-reports/2026-06-14.md`・`2026-06-16.md`（gitignore＝ローカルのみ）。**6/21・6/28分は未作成**。
- 理由：GA4/Search Consoleは**ログイン必須**でデータ自動取得できず、最近取得できていない。捏造せず、データが揃ったら作る。
- やり方：[日曜データ取得の手順.md](日曜データ取得の手順.md)で数字取得 → [週次レポート様式.md](週次レポート様式.md)で清書（メモリ `reference_weekly_report`）。

### D. 楽天証券アフィリ（A8にあり・未対応）
- 対象5記事のボタンが報酬の出ない公式直リンクのまま：nisa-hajimekata-rakuten / nisa-1nen-jisseki / nisa-shippai-20dai / nisa-20dai-portfolio / shogakukin-hensai-toushi
- A8に楽天証券プログラムあり（セルフバック口座開設9,200円も確認済）。**提携→広告URLを太田さんが貼れば、5記事一括置換してcommit**（1分）。捏造厳禁。

---

## 2. ⚠️ A8サイト登録のURL問題（要解決）
- A8のメディアID `a26042506020`。サイト名は「**ゆる節約ライフ**」に修正済み。
- **登録サイトURLが本番でなくプレビュー用 `https://setsuyaku-blog.pages.dev` になっていた。** 本番 `https://yuru-setsuyaku.com/` に修正しようとしたら「**サイトURLが既に登録されています**」エラー → 別枠にyuru-setsuyaku.comが既登録の可能性。**URL修正が完了したか未確認**。
- 影響：A8は登録サイトURLで提携審査・成果計測する。**pages.devのままだと審査落ち/成果非承認/規約リスク**。要整理（A8サポートに問い合わせ or 重複サイト枠の確認）。
- 別件だが関連：pages.devがGoogleにインデックスされる懸念（CLAUDE.md「preview_urls無効化」）。インフラ設定＝必要ならエンジニア相談。

---

## 3. サイトの現状＝「内部最適化は完全に飽和」＋SEO 18項目チェック済
- 全100記事が型統一済（リード4要素/PREP/会話/FAQ/CTA/内部リンク）。CTAボタン31本／E-E-A-Tボックス43本／スマホCSS済／リンク切れ0。
- 技術SEO：canonical・schema_json・OGP・Twitterカード・robots.txt(`enableRobotsTXT`)・sitemap.xml(本番350URL生成確認済) すべて実装済。description 100/100記事、英語slug、画像alt付き。
- **SEOやるべき18項目チェック実施→ほぼ全部OK**。残る要確認は2つだけ：①**Search Consoleでサイトマップを「送信」したか**（生成はOK、SC側送信操作が未確認）②**薄いタグページ（記事1本の「27歳」等）の整理/noindex**（任意・低優先）。
- ➡ **内部の量産・微修正は低価値。** 成長レバーは外部（X継続・アフィリ・Google再評価＝時間）。
- 問い合わせフォーム（旧Formspree不達）→ X DM導線に修正済・本番反映確認済（完了）。

---

## 4. ⚠️ 環境・ツールの注意点
- **Claude in Chrome がこの会話に接続できない状態が続いている**（`list_connected_browsers`が空・`switch_browser`も不可）。拡張はインストール/有効だがペアリング不成立。→ **当面は太田さんがスクショを貼る/コピペで手動運用**。Xの自動投稿・A8画面操作は接続復活が前提。安定化は将来エンジニア相談。
- **git author がローカルで空になることがある**（"No user exists for uid 501"でpush失敗も発生済）。commit前に必要なら：
  `git config user.name "太田賢吾" && git config user.email "ootakengo@ootakengonoMacBook-Air.local"`
- git push は時々タイムアウト/環境エラー→ `(git push origin master -q || (sleep 30 && git push origin master -q))` で再送。失敗時はローカルcommitを残し次回push。
- 夜間「おやすみ」自動化：短い「おやすみ」でUserPromptSubmitフックが夜間PDCAを起動（`~/.claude/hooks/oyasumi-pdca.sh`）。漢字「お休み」は起動しない。

---

## 5. 運用ドキュメント一覧
- **X運用**：`X運用ガイド_まずこれ.md`(入口)／`Xの次の投稿キュー.md`(次の順番)／`x-posting-calendar.md`(4週カレンダー)／`x-starter-tweets.md`(30本)／`x-tweets-batch3.md`(投票/質問/あるある/数字)／`x-blog-promo-tweets.md`(実記事告知7本)／`x-seasonal-tweets.md`(6〜7月)／`x-number-templates.md`(数字穴埋め)／`X予約投稿の使い方.md`
- **週次レポート**：`週次レポート様式.md`／`日曜データ取得の手順.md`
- 元ネタ：`~/Desktop/Claude用/X投稿ネタ完全ガイド.docx`（200本超）→ メモリ `reference_x_post_guide`

---

## 6. 重要ルール（厳守）
- 新記事は書かない（オーナーのキャパ／内部飽和）。やるなら実データ起点だけ。
- **公開アクション(X投稿)・本人情報(アフィリURL)は本人確認/本人取得が必要。** アフィリURL・数字・事実は捏造しない。
- 保険等YMYL・金融は慎重に。論旨と矛盾する広告は入れない（読者信頼/E-E-A-T優先）。
- コミット末尾：`Co-Authored-By: Claude ...`。記事タイトル(URL/slug)は変更しない（SEO評価が消える）。

---

## 7. 次セッションの最優先アクション（この順で）
1. **保険アフィリ（1-A）**：A8で「保険見直し本舗」が**承認されたか確認**→承認なら広告リンクをもらい記事挿入＆commit／まだ審査中なら待ち。
2. **A8サイトURL問題（2）**：pages.dev→yuru-setsuyaku.comの登録修正が済んだか確認（審査の前提）。
3. **X投稿（1-B）**：ブラウザ接続できれば `Xの次の投稿キュー.md` の上から投稿（まず🔥S1夏ボーナス）。
4. **週次レポート（1-C）**：日曜ならGA4/SCデータを一緒に取得→レポート作成。
5. **楽天証券アフィリ（1-D）**：提携URLをもらえたら5記事一括置換。
6. 内部記事の量産はしない。
