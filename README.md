# Step-into-A-World

> 為已有圖片與世界設定的網站，加入擬真即時影像。

Step-into-A-World 是一套工具框架，由團隊 FlyPig AI 為 ASUS UGen AI League 2026（Creator AI 主題 × Lightning 輕量運算組 × 線上組）開發。框架服務的對象是 IP 擁有者及網站經營者：網站已有圖片與世界設定，框架讓觀測頁面每次開啟都能生成一段新的觀測影片。

## 專案介紹

靜態網站發佈那天就凍結了：所有訪客看到同一組圖片與影片。Step-into-A-World 讓同一個世界每次觀看都有不同內容，且符合原有設定。每次開啟觀測頁面，系統依領域、可能出現的物種／角色、氣候與時間，產生情境及提示詞，再生成新的觀測影片；每次觀測依當下條件發起新的影片生成。

## 使用流程

1. **網站與世界設定輸入**——網站既有圖片、領域資料、物種／角色名錄與世界規則，整理為框架的輸入。
2. **組成情境**——依當次觀測的領域、可能出現的物種／角色、氣候與時間，組合成這一回的情境。
3. **生成提示詞**——由 UGen300 負責情境理解與提示詞生成（見計畫技術與 UGen300 分工）。
4. **生成觀測影片**——影片生成模組依提示詞產生新的觀測影片。
5. **瀏覽器中觀看**——觀測頁面在網站既有頁面中播放影片；活動範圍與故事規則納入提示詞與內容檢查。
6. **內容檢查**——發佈前檢查設定一致性、活動範圍與語言，確保生成內容符合世界設定。

## 計畫技術與 UGen300 分工

架構分為兩個模組：情境／提示詞生成，與影片生成。UGen300（Hailo-10H、40 TOPS INT4、8GB）負責情境理解與提示詞生成；影片生成為獨立模組，不由 UGen300 端到端包辦，也不假設所有運算都在裝置內完成。具體影片後端與整合方式於第二階段開發時確定。

## 應用情境

透過可重用的框架，為不同 IP 與網站加入擬真即時影像：

- 小說／漫畫／遊戲世界——讀者重訪同一地點時，能看見該地點正在發生的畫面。
- 虛擬生態——物種與棲地網站，每次造訪呈現生態中的不同時刻。
- 旅遊場景——目的地頁面以動態觀測呈現地方風貌。
- 品牌故事網站——品牌世界觀從靜態頁面轉為可觀看的動態場景。

## 視覺示意

### 觀測體驗與視覺示意：K 的狩獵日誌

K 的狩獵日誌既有場景（雲梯讓道礦廊一帶的領域、物種與田野紀錄）展示預期的觀看體驗：觀測窗、領域介紹與物種紀錄構成的瀏覽方式，就是框架完成後希望達到的體驗樣貌。框架本身於第二階段開發。

- 既有觀測體驗：https://k-hunting-log.icareu.tw/journey/

### 預計驗證場景：深海熱泉觀測站

第二個世界以短篇原創正典寫成，作為第二階段的預計驗證場景，用來驗證同一框架能否服務完全不同的設定（熱泉、洋流、黑暗與深海物種）。目前尚未接入。

## 開發階段

- **第一階段**——提案與概念架構：框架概念、系統架構與驗證方法。截止 10 月 28 日台北時間 17:00；11 月 2 日公布入圍。
- 第二階段將開發框架原型，由 UGen300 負責情境理解與提示詞生成，並整合影片生成模組及網站觀測介面。11 月 6 日至 12 月 4 日；12 月 4 日繳件；12 月 19 日公布結果。

## 文件導覽

- `docs/PRD.md`——產品需求文件。
- `framework/`——框架程式碼（第二階段開發）。
- `examples/`——示意網站（規劃中）。

---

# Step-into-A-World (English)

> Lifelike live imagery for sites that already have images and a world setting.

Step-into-A-World is a tool framework by team FlyPig AI, built for ASUS UGen AI League 2026 (Creator AI theme × Lightning track × Online track). It serves IP holders and website operators: for a site that already has images and a world setting, the framework lets each observation page open generate a new observation video.

## Project overview

A static site freezes the day it is published: every visitor sees the same images and videos. Step-into-A-World lets the same world show different content on each viewing, consistent with its setting. Each time an observation page opens, the system builds a scenario and a prompt from the domain, the species or characters that may appear, the climate and the time, then generates a new observation video. Each observation initiates a new video generation based on the current conditions.

## How it works

1. **Site and world setting in** — the site's existing images, domain data, species/character lists and world rules, organised as the framework's input.
2. **Compose the scenario** — from the domain, the species or characters that may appear, the climate and the time for this viewing.
3. **Generate the prompt** — the UGen300 handles scenario understanding and prompt generation (see Technology and UGen300 division below).
4. **Generate the observation video** — a video generation module produces a new observation video from the prompt.
5. **Watch in the browser** — the observation page plays the video inside the site's existing pages; activity scope and story rules are included in prompts and content checks.
6. **Content checks** — before release, check setting consistency, activity scope and language, so generated content fits the world setting.

## Technology and UGen300 division

The architecture has two modules: scenario/prompt generation, and video generation. The UGen300 (Hailo-10H, 40 TOPS INT4, 8 GB) handles scenario understanding and prompt generation; video generation is a separate module, not generated end-to-end on the device, and the plan does not assume every step runs on the device. The video backend and integration details will be settled during Stage II development.

## Application scenarios

A reusable framework that adds lifelike live imagery to different IPs and websites:

- Fiction, comics and game worlds — readers revisiting a place can watch that place happening.
- Virtual ecology — species and habitat sites showing a different moment in the ecosystem on each visit.
- Travel and place storytelling — destination pages presented through live observation.
- Brand story sites — a brand's story world turned from static pages into watchable scenes.

## Visual reference

### Observation experience and visual reference: K's Hunting Log

The existing scenes of K's Hunting Log (domains, species and field notes around the cloud-ladder mining corridor) show the expected viewing experience: observation windows, domain introductions and species records are the browsing experience the finished framework aims to deliver. The framework itself is developed in Stage II.

- Existing observation experience: https://k-hunting-log.icareu.tw/journey/

### Planned validation scene: deep-sea hydrothermal observatory

A second world, written as a short original canon, serves as the planned validation scene in Stage II, testing whether the same framework can serve a very different setting (vents, currents, darkness and deep-sea species). It is not yet connected.

## Development stages

- **Stage I** — proposal and concept architecture: framework concept, system architecture and verification method. Deadline Oct 28, 17:00 Taipei time; shortlist announced Nov 2.
- **Stage II** — develop the framework prototype: the UGen300 handles scenario understanding and prompt generation, integrated with a video generation module and the website observation interface. Nov 6 to Dec 4; submission Dec 4; results announced Dec 19.

## Repository guide

- `docs/PRD.md` — product requirements.
- `framework/` — framework code (Stage II development).
- `examples/` — reference sites (planned).
