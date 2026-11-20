<img src="icons/icon-192.png" width="96" alt="SeeMo icon">

# 心模 SeeMo

**v1.5.1** · Designed by Ron Chen

SeeMo (心模, “heart model”; sounds like *see more*) — formerly *DIF Viewer & Converter / DIF 檢視轉檔器*.

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
| **v1.5.1** Volume list shows each model's volume (ml); fixed the eraser error on measurements | **v1.5.1** 結構清單顯示每個模型的體積（ml）；修正橡皮擦刪除測量線時的錯誤 |
| **v1.4.0** Measure tool: drag on the model or click two points to show the straight-line distance (mm) | **v1.4.0** 測量工具：在模型上拖曳或點兩點，顯示直線距離（mm） |
| 中文 / English switch | 中英切換 |

## CT reconstruction · CT 重組（v1.2.0 – v1.5.0）

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
| **v1.3.0** Auto-detect LA, AO, RA, LV, RV and esophagus: review the seeds, then segment all at once, with gap filling | **v1.3.0** 自動辨識 LA、AO、RA、LV、RV、食道：先確認種子點，再一次切好，並自動填滿空隙 |
| **v1.3.0** New layout: vertical tool rail (Pan, Click add, Add / Erase brush), shortcuts, 2×2 or one-big-three-small views, collapsible left column | **v1.3.0** 新版面：左側直排工具（平移、點選加入、加入／擦除筆刷）、快捷鍵、2×2 或一大三小、左欄可收合 |
| **v1.3.0** Edit several structures, then generate all their 3D models at once | **v1.3.0** 可以連續修好幾個結構，最後一次生成 3D |
| **v1.5.0** More accurate auto-detect: the aorta is traced up from the descending aorta (PA and SVC stay out), chambers are searched only at heart level, uncertain LV/RV points are left for the competition, and esophagus tracking stops at the liver | **v1.5.0** 自動辨識更準：主動脈從降主動脈往上長（不會長進肺動脈、SVC），心腔只在心臟高度範圍內找，分不清的 LV／RV 點不硬分，食道追蹤碰到肝臟就停 |
| **v1.5.0** Fix: the structure list shows ml again after auto segmentation | **v1.5.0** 修正：自動切完後，結構清單恢復顯示 ml 數 |
| **v1.4.0** Measure on CT slices (drag) and on the 3D view (two points); rename “Other” structures (e.g. SVC, IVC, LAA) | **v1.4.0** 在 CT 切面（拖曳）和 3D（點兩點）上測量；「其他」結構可改名（例如 SVC、IVC、LAA） |

## Use · 使用方式

1. Open the link above in Chrome or Edge. / 用 Chrome 或 Edge 開上面的網址。
2. Press “Open file” / “Open folder”, or drag a `.dif` / `.xml` file or a DICOM CT folder onto the page. The type is detected automatically: `.dif` / `.xml` → 3D model, DICOM CT → CT reconstruction. / 按「開啟檔案」「開啟資料夾」，或把 `.dif`／`.xml` 檔、DICOM CT 資料夾拖進頁面；系統自動判斷：`.dif`／`.xml` → 3D 模型，DICOM CT → CT 重組。
3. For CT, use an arterial-phase series with the whole heart opacified. / CT 請用整顆心臟都有顯影的動脈期序列。
4. To use offline, download `index.html` and open it directly; no install needed. / 要離線使用，下載 `index.html` 直接開啟即可，不需安裝。

## Notes · 注意事項

- This is not an Abbott or ADAS 3D product and is not a medical device. Check any converted file against the original ADAS 3D images before clinical use.
- 本工具不是 Abbott 或 ADAS 3D 的產品，也不是醫療器材。轉出的檔案用於臨床前，請先與 ADAS 3D 原圖核對。
- CT-derived models are approximate; verify against the CT before use. / CT 重組的模型是近似結果，使用前請對照 CT 確認。
- Do not commit patient files to this repository. / 請勿把病人檔案放進這個 repo。
