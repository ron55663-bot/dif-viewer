# DIF Viewer & Converter · DIF 檢視轉檔器

**v1.2.0** · Designed by Ron Chen

**Open the tool / 開啟工具：** https://ron55663-bot.github.io/dif-viewer/

A single-page browser tool for viewing EnSite / ADAS 3D `.dif` heart models, converting them for EnSite X, and building chamber models from cardiac CT.
Files are processed only in your own browser and are never uploaded.

在瀏覽器裡開啟 EnSite / ADAS 3D 的 `.dif` 心臟模型、轉成 EnSite X 讀得進去的格式，也可以從心臟 CT 重組心腔模型。
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
| Click a volume's color square to change its color (kept on export) | 點 Volume 的色塊可改顏色，匯出也用新顏色 |
| 中文 / English switch | 中英切換 |

## CT reconstruction · CT 重組（v1.2.0）

| English | 中文 |
|---|---|
| Open a DICOM CT folder (uncompressed), pick the series | 開啟 DICOM CT 資料夾（未壓縮），選擇序列 |
| Axial / coronal / sagittal views with zoom, pan, slice slider and arrow keys | 軸切、冠狀切、矢狀切，可放大、平移、滑桿或方向鍵換層 |
| Pick a structure and click its middle: the region is outlined in colour automatically | 選結構、點正中間，系統自動用顏色圈出範圍 |
| Chamber vs. vessel method chosen automatically | 心腔／血管方法自動判斷 |
| Fix the region: extra seeds, add brush, erase brush (also on the 3D model), undo/redo | 修正範圍：加種子點、加入筆刷、擦除筆刷（也可直接在 3D 上擦）、復原／重做 |
| “Generate 3D Geometry” builds the model; lock a finished structure to keep others out | 按「生成 3D Geometry」產生模型；做好的結構可鎖定，其他結構進不去 |
| 3D view with draggable XYZ axes linked to the CT crosshair; double-click jumps the CT there | 3D 有可拖曳的 XYZ 軸線，對應 CT 十字線；雙擊模型 CT 跳到該點 |
| Send to the 3D viewer and export DIF 5.0 for EnSite X | 送到 3D 檢視並匯出 EnSite X 用的 DIF 5.0 |

## Use · 使用方式

1. Open the link above in Chrome or Edge. / 用 Chrome 或 Edge 開上面的網址。
2. Drag a `.dif` file onto the page. / 把 `.dif` 檔拖進頁面。
3. For CT, press “Open CT (DICOM folder)” and choose the folder; use an arterial-phase series. / CT 請按「開啟 CT（DICOM 資料夾）」選資料夾，請用動脈期序列。
4. To use offline, download `index.html` and open it directly; no install needed. / 要離線使用，下載 `index.html` 直接開啟即可，不需安裝。

## Notes · 注意事項

- This is not an Abbott or ADAS 3D product and is not a medical device. Check any converted file against the original ADAS 3D images before clinical use.
- 本工具不是 Abbott 或 ADAS 3D 的產品，也不是醫療器材。轉出的檔案用於臨床前，請先與 ADAS 3D 原圖核對。
- CT-derived models are approximate; verify against the CT before use. / CT 重組的模型是近似結果，使用前請對照 CT 確認。
- Do not commit patient files to this repository. / 請勿把病人檔案放進這個 repo。
