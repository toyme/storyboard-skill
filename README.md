# Storyboard Skill

這是一個給 Codex 使用的分鏡輔助技能。

它可以幫你把故事、場景描述、分鏡想法，整理成更清楚的「畫面語言」和「AI 圖像生成提示詞」。  
適合用在 AI 圖像分鏡、角色一致性管理、畫面連續性檢查、修圖提示詞整理。

## 這個 Skill 可以幫你做什麼？

你可以用它來：

- 把一段劇情拆成分鏡
- 把分鏡整理成 shot list
- 幫每一格分鏡寫 AI 圖像 prompt
- 檢查角色前後是否一致
- 檢查服裝、髮型、道具、場景是否跑掉
- 檢查畫面是否有 NSFW、未成年人、暴力、真人肖像、版權角色等風險
- 幫已生成的圖片寫修正 prompt

簡單說，它的用途是：

> 幫你把「我腦中的畫面」整理成「AI 比較容易理解的畫面指令」。

## 適合什麼情境？

例如你有這樣的描述：

```text
主角情緒已經撐不住了，但他重新鼓起勇氣，快步走到門邊，停頓一下，打開門走出去。
```

這個 skill 可以幫你整理成：

- 這一段需要幾個鏡頭
- 每個鏡頭要拍什麼
- 主角表情和動作怎麼描述
- 鏡位是中景、特寫、背面還是側面
- 光線和氣氛怎麼寫
- 給 AI 圖像工具的 prompt 要怎麼寫
- 有沒有不符合平台規範的地方

## 不適合做什麼？

這個 skill 只專注在「分鏡」和「圖像 prompt」。

它不負責：

- 直接生成圖片
- 直接生成影片
- 連接 Seedance、Higgsfield、Runway、Kling 等平台
- 自動上傳到任何網站
- 取代法律、版權或平台官方審查

如果你要生成圖片，這個 skill 會幫你準備 prompt；  
實際生成還是要到你的圖像工具裡操作。

## 安裝方式

把這個 repo 放到 Codex 的 skills 資料夾裡。

Windows 範例：

```powershell
git clone https://github.com/YOUR_NAME/storyboard-skill.git C:\Users\admin\.codex\skills\storyboard-skill
```

安裝後，確認檔案位置長這樣：

```text
C:\Users\admin\.codex\skills\storyboard-skill\SKILL.md
```

如果 Codex 沒有馬上讀到這個 skill，可以重新開一個新對話，或重啟 Codex。

## 怎麼使用？

你可以直接對 Codex 說：

```text
Use $storyboard-skill to turn this scene into storyboard image prompts.
```

或用中文說：

```text
使用 $storyboard-skill 幫我把這段劇情整理成分鏡和圖像 prompt。
```

也可以這樣說：

```text
使用 $storyboard-skill 檢查這些分鏡 prompt 有沒有角色不一致或 NSFW 風險。
```

修圖時可以說：

```text
使用 $storyboard-skill 幫我寫修正 prompt，只改手的姿勢，不要改角色長相、服裝和構圖。
```

## 建議的專案結構

如果你要做比較完整的分鏡專案，可以用這種資料夾結構：

```text
storyboard-project/
  bible/
    character_bible.md
    visual_style_bible.md
    continuity_rules.md
  scenes/
    scene_01.yaml
  shots/
    scene_01_shots.yaml
  prompts/
    scene_01_shot_001.md
  reviews/
    continuity_review.md
```

不用一開始就全部建立。  
如果只是測試，可以先從一段劇情或一個場景開始。

## 這些檔案是做什麼的？

### character_bible.md

記錄角色設定，例如：

- 角色名字
- 年齡範圍
- 髮型
- 臉部特徵
- 服裝
- 重要道具
- 不能改變的地方

### visual_style_bible.md

記錄整體畫風，例如：

- 寫實或插畫
- 色調
- 光線
- 鏡頭語言
- 材質感
- 畫面比例

### continuity_rules.md

記錄連續性規則，例如：

- 主角不能換衣服
- 場景時間是晚上
- 道具必須一直在右手
- 不要突然新增角色

### scene_01.yaml

記錄某一場戲的內容。

### scene_01_shots.yaml

記錄這場戲拆成哪些鏡頭。

### prompts/

存放每個鏡頭的 AI 圖像 prompt。

### reviews/

存放連續性檢查、安全檢查或修改建議。

## 內建參考文件

這個 skill 內含幾份參考文件：

```text
references/project-structure.md
```

說明分鏡專案資料夾怎麼整理。

```text
references/prompt-patterns.md
```

提供 image prompt、fix prompt、review 的格式。

```text
references/prompt-safety-checklist.md
```

用來檢查 NSFW、未成年人、暴力、真人肖像、版權角色、隱私資料等風險。

## 使用範例

你可以給 Codex：

```text
主角站在雨中的巷口，手裡拿著一封信。他猶豫很久，最後把信撕掉，轉身離開。
```

然後要求：

```text
使用 $storyboard-skill 幫我拆成 5 個分鏡，並替每個分鏡寫 AI 圖像 prompt。
```

Codex 會輸出類似：

```text
[SHOT ID]
scene_01_shot_001

[PURPOSE]
建立主角孤獨與猶豫的情緒。

[CAMERA]
中遠景，街角側面構圖。

[LIGHTING]
夜晚雨中街燈，冷色調。

[IMAGE PROMPT]
...
```

## 注意事項

- 如果角色很多，建議先建立角色設定。
- 如果畫風很重要，建議先建立 visual style bible。
- 如果已經有生成過的圖片，請明確說哪些地方要保留、哪些地方要修改。
- 如果要做商業作品，請注意肖像權、版權和平台規範。
- 安全檢查只能協助降低風險，不能保證一定符合所有平台最新規定。

## 一句話總結

這個 skill 的目標是：

> 讓你的分鏡更清楚、角色更一致、prompt 更穩定，也比較不容易踩到平台規範問題。
