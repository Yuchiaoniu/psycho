# 心理路徑地圖專案 (Psych Resilience Web Tool)

## 專案背景

這個專案起源於一段深度對話，從生物學、心理學、社會學的角度探討人類行為與心理操控。最終目標是建立一個開放的靜態網頁工具，幫助所有人（施暴者、受害者、旁觀者）識別心理操控模式、建立正向錨定、提升社會韌性。

核心設計哲學：**去病理化**——施暴者不是怪物，是在錯誤路徑上累積太深的人。轉化比對抗更能增加社會韌性。

## 專案結構

```
C:\Users\yuchi\psycho\
├── index.html              # 完整單頁應用
├── data/
│   ├── paths.json          # 所有心理路徑資料（攻擊性+正錨）
│   ├── decision-tree.json  # 旁觀者決策樹資料
│   └── cases.json          # 情境模擬案例
├── .github/workflows/
│   └── deploy.yml          # GitHub Pages 自動部署
└── CLAUDE.md               # 本檔案
```

OpenSpec 規格文件位於：`C:\Users\yuchi\openspec\changes\psych-resilience-web-tool\`

GitHub 遠端：`https://github.com/Yuchiaoniu/psycho.git`

## 路徑資料現況

### 攻擊性路徑（12 條）

依層次排列：

**物理層**
1. 物理威脅定錨（Physical Threat Anchoring）— 第零條路徑，所有後續攻擊的通道開啟機制

**心理層**
2. 習得性無助（Learned Helplessness）
3. 補償性思維（Compensatory Thinking）
4. 侵入性思維（Intrusive Thinking）
5. 間歇性強化（Intermittent Reinforcement）
6. 創傷連結（Trauma Bonding）
7. 推拉策略（Push-Pull）
8. 認同攻擊者（Identification with the Aggressor）
9. 創傷重演（Trauma Reenactment）

**社會層**
10. 三角操控（Triangulation）
11. 勢力範圍擴張（Territory Expansion）

**環境層**
12. 環境控制（Environmental Control）

### 正錨路徑（26 條）

物理層反制：
- 熟悉安全存在建立（Familiar Safe Presence）— 熟悉度 > 強壯度
- 恐懼歸因重構（Fear Attribution Reframing）

心理層正錨：
- 正錨定、對比效應、情感顯著性、安全依附觸發、認知可及性
- 情緒調節他者、脈絡重建、共同調節、窗口期擴展
- 社會基線重建、後設認知重構、能動性喚醒
- 非依附性給予、正向顯著性植入、可預測性建立
- 自主性保護、社會健康示範、敘事重構
- 微小勝利累積、具身認知重置

操控環境策略層：
- 競爭歸因重構（Competition Attribution Reframing）— 三角操控次級效應的正確歸因
- 穩定能力培養（Stability Capacity Building）— 從評估他人穩定轉為建立自身穩定能力
- 自然脈絡擴張（Natural Context Expansion）— 純內在訓練，五層流程，感官擴張稀釋威脅梯度
- 壓力適應循環（Stress Adaptation Cycle）— 輕微壓力×選擇×完成，心理與身體同步積累強狀

### 複合攻擊五層結構

| 層次 | 名稱 | 權重 | 功能 |
|---|---|---|---|
| 1 | 物理層 | ★★★★ | 打開通道，定錨恐懼 |
| 2 | 環境層 | ★★★ | 縮減物理選擇空間 |
| 3 | 心理層 | ★★★★★ | 核心引擎，建立依賴迴路 |
| 4 | 社會層 | ★★★ | 封鎖外部資源與退路 |
| 5 | 資訊層 | ★★（×乘數） | 放大所有其他層次效果 |

## 微積分框架

心理狀態變化的數學隱喻：
- **一階導數 f'(t)**：變化方向，比當前數值更重要
- **二階導數 f''(t)**：改善加速度，正錨的複利效應
- **積分 ∫f dt**：累積正向面積，長期低強度勝過單次衝擊
- **臨界點 f'(c)=0**：相變，改變是突然的不是漸進的
- **梯度 ∂f/∂x**：壓力地形，建立替代谷底而非強拉出舊谷
- **收斂條件**：方向正確 × 步長適當 × 持續迭代

## 情境模擬 Case A 摘要

封閉機構環境中的複合操控案例，三個角色：
- **T（女性，目標）**：內向乖巧，出現明顯解離症狀
- **A（施壓者）**：高大，有社會資源和協作者，行動具組織性
- **B（旁觀者）**：與 T 認識約一年半，初期用力過猛後收斂為低強度策略

關鍵發現：
- B 面對的是有組織的結構，不是單一個人
- T 是受害者也是資訊節點（無意識）
- 熟悉度 > 強壯度（物理層反制的核心發現）
- 六種戰術手冊已收錄在 cases.json

## 網站功能頁面

1. **首頁** — 四個功能入口
2. **路徑地圖** — 攻擊性/正錨路徑索引，含三視角切換（受害者/旁觀者/施暴者）
3. **複合攻擊** — 五層結構分析
4. **微積分框架** — 六個概念卡片 + 積分互動模擬
5. **旁觀者決策樹** — 情境問答 → 具體介入建議
6. **情境模擬** — Case A 完整紀錄

## 本機開發

```powershell
cd C:\Users\yuchi\psycho
python -m http.server 8765
# 開啟 http://localhost:8765
```

## 待完成事項

- [ ] Git push 到 GitHub（git 未在 PATH 中，需透過 GitHub Desktop 或手動設定）
- [ ] GitHub Pages 設定：Settings → Pages → Source → GitHub Actions
- [ ] 持續補充心理路徑（目前仍有未收錄的路徑待探索）
- [ ] 所有「他」已改為「它」以模糊性別

## 對話延續提示

如果要繼續這個專案，可以說：
- 「繼續補充路徑」
- 「繼續 Case A 的分析」
- 「幫我 push 到 GitHub」
- 「繼續討論第 N 條路徑」
