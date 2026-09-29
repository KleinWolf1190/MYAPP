# MYAPP APP 架構規劃

> 本文件先定義未來 Unity 專案的架構方向，不包含實際程式碼。

## 1. 建議分層

未來可考慮採用以下邏輯分層：

```
Presentation
    ↓
Application / Use Cases
    ↓
Domain
    ↓
Infrastructure / Data
```

### Presentation
負責 UI、頁面、輸入與視覺回饋。

### Application
負責「使用者想完成什麼事情」的流程協調。

### Domain
負責 APP 最核心的資料與規則。

### Infrastructure / Data
負責本機檔案、資料庫、網路 API、雲端服務等實際資料來源。

---

## 2. Unity 場景策略

目前建議不要一開始建立大量 Scene。

第一階段可先規劃：
- Bootstrap / 啟動場景
- Main / 主體場景
- 依需求增加功能場景

實際場景數量等需求確定後再決定。

---

## 3. UI 架構

預計將 UI 視為獨立系統處理：

- 導航
- 頁面
- 彈窗
- 通知
- Loading
- Error State
- Empty State

UI 不應直接處理大量資料規則，避免未來修改 UI 時影響核心功能。

---

## 4. 資料流

初步方向：

```
User Input
   ↓
UI
   ↓
Use Case / Application Logic
   ↓
Domain
   ↓
Repository / Data Service
   ↓
Local / Network Data
```

實際技術方案待需求確定後決定。

---

## 5. Unity 專案目錄方向

未來 Unity 專案可以整理成：

```
Assets/
├─ Art/
├─ Audio/
├─ Prefabs/
├─ Scenes/
├─ Scripts/
│  ├─ Presentation/
│  ├─ Application/
│  ├─ Domain/
│  └─ Infrastructure/
├─ Data/
├─ Resources/
└─ Tests/
```

此處為規劃，不代表現在就建立這些目錄。

---

## 6. 架構決策原則

- 優先使用 Unity 官方長期可維護的方案。
- 外部套件要有明確理由再引入。
- 核心資料模型盡量不要依賴 UI。
- 網路功能與本機功能應可替換。
- AI 產生程式碼前，必須先讀取本文件與需求規格。

