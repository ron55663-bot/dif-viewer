# DIF Viewer & Converter · DIF 檢視轉檔器

**v1.1.0** · Designed by Ron Chen

**Open the tool / 開啟工具：** https://ron55663-bot.github.io/dif-viewer/

A single-page browser tool for viewing EnSite / ADAS 3D `.dif` heart models and converting them for EnSite X.
Files are processed only in your own browser and are never uploaded.

在瀏覽器裡開啟 EnSite / ADAS 3D 的 `.dif` 心臟模型，並轉成 EnSite X 讀得進去的格式。
檔案只在你自己的瀏覽器裡處理，不會上傳到任何地方。

## Features · 功能

| English | 中文 |
|---|---|
| Open `.dif` / `.xml` models with every volume listed | 開啟 `.dif` / `.xml` 模型，列出所有 Volume |
| Scar maps (e.g. `L10_39_59`) colored with the file's own color table | 依檔案內附的色階表顯示疤痕 map（例如 `L10_39_59`） |
| Adjustable color bar thresholds | 色條門檻可拖曳調整 |
| Per-volume show/hide and opacity | 每個 Volume 可單獨顯示、隱藏、調不透明度 |
| Single or dual (side-by-side) view, each with its own camera | 單視窗或左右雙視窗，各自旋轉縮放 |
| Orientation torso and AP / PA / LL / RL / LAO / RAO / SUP / INF presets | 方向人形與 AP / PA / LL / RL / LAO / RAO / SUP / INF 視角 |
| Ctrl + click on the model sets the rotation center | Ctrl + 點模型設為旋轉中心 |
| Annotations on the surface: line, circle, box, text, eraser, undo/redo | 貼在模型表面的標註：畫線、圓圈、框框、文字、橡皮擦、復原／重做 |
| PNG snapshot | 快照存成 PNG |
| Export: EnSite DIF 5.0, PLY (with colors), STL, VTK | 匯出：EnSite DIF 5.0、PLY（含顏色）、STL、VTK |
| Optional removal of patient name, ID and birth date on DIF export | 匯出 DIF 時可清空病人姓名、ID、生日 |
| 中文 / English switch | 中英切換 |

## Use · 使用方式

1. Open the link above in Chrome or Edge. / 用 Chrome 或 Edge 開上面的網址。
2. Drag a `.dif` file onto the page. / 把 `.dif` 檔拖進頁面。
3. To use offline, download `index.html` and open it directly; no install needed. / 要離線使用，下載 `index.html` 直接開啟即可，不需安裝。

## Notes · 注意事項

- This is not an Abbott or ADAS 3D product and is not a medical device. Check any converted file against the original ADAS 3D images before clinical use.
- 本工具不是 Abbott 或 ADAS 3D 的產品，也不是醫療器材。轉出的檔案用於臨床前，請先與 ADAS 3D 原圖核對。
- Do not commit patient files to this repository. / 請勿把病人檔案放進這個 repo。
