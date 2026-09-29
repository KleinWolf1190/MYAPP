# MYAPP

Unity APP 專案的需求、設計文件與原始碼儲存庫。

## 專案狀態

目前處於 **需求討論 / 設計階段**。

本階段暫不建立 Unity 程式碼，先確認：
- APP 的核心目的與目標使用者
- 功能範圍與優先級
- 使用者流程
- UI / UX 架構
- 資料模型與資料來源
- Unity 專案架構
- 後續 AI 協作規則

## 目錄規劃

```
MYAPP/
├─ README.md
├─ .gitignore
├─ doc/
│  ├─ 00-project-charter.md
│  ├─ 01-requirements.md
│  ├─ 02-app-architecture.md
│  ├─ 03-data-design.md
│  └─ 04-ai-handoff.md
├─ Assets/        # 後續 Unity 專案建立後使用
├─ Packages/      # 後續由 Unity 管理
├─ ProjectSettings/# 後續由 Unity 管理
└─ ...
```

## 工作原則

1. 需求未確認前，不先寫功能程式。
2. 設計決策以 `doc/` 為準，重要變更要同步記錄。
3. Unity 相關實作應盡量模組化，避免把所有邏輯集中在單一腳本。
4. AI 協作時，先閱讀 `README.md` 與 `doc/` 再修改專案。
5. 每次較大的設計或架構變更，都應留下可追蹤的文件與 Git commit。
6. 不把機密金鑰、帳號資訊或本機環境設定提交進 Git。

## 後續流程

需求討論 → 需求定稿 → UX/UI 規格 → 技術架構 → Unity 專案初始化 → 功能實作 → 測試 → 發布。

