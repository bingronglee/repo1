# 門牌座標分析專案

本專案是一個基於 Flask 的 Web 應用程式，用於分析 DXF 檔案中的多邊形區域與門牌座標的空間關係。支援從 DXF 檔案中提取多邊形，並與 SQLite 資料庫中的門牌座標進行空間分析，最終生成包含分析結果的 DXF 檔案。

---

## 功能特色
- **DXF 檔案解析**：讀取 DXF 檔案中的多邊形區域。
- **門牌座標分析**：與 SQLite 資料庫中的門牌座標進行空間分析。
- **結果導出**：生成包含分析結果的 DXF 檔案。
- **高效查詢**：使用 SQLite 資料庫提升查詢效率。

---

## 安裝步驟

### 1. 環境需求
- Python 3.8+
- 以下 Python 套件：
  ```bash
  flask
  geopandas
  pandas
  shapely
  ezdxf
  scipy
  numpy
  sqlalchemy
  ```

### 2. 安裝依賴
1. 克隆專案：
   ```bash
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   ```
2. 安裝依賴：
   ```bash
   pip install -r requirements.txt
   ```


---

## 使用方式

### 1. 啟動應用程式
執行以下指令啟動 Flask 應用程式：
```bash
python main.py
```
應用程式將運行於 `http://localhost:5000`。

### 2. 上傳 DXF 檔案
1. 開啟瀏覽器，訪問 `http://localhost:5000`。
2. 選擇區域（如「高雄」）並上傳 DXF 檔案。
3. 系統將分析 DXF 檔案中的多邊形與門牌座標的空間關係。

### 3. 下載結果
分析完成後，頁面將顯示統計結果並提供包含分析結果的 DXF 檔案下載連結。



---

## 專案結構
```
│  main.py                # 主程式
│  database.py            # 資料庫初始化腳本
│  requirements.txt       # 依賴套件列表
│  README.md              # 專案說明文件
├─data
│      KH.csv             # 高雄門牌座標 CSV
│      TC.csv             # 台中門牌座標 CSV
│      TN.csv             # 台南門牌座標 CSV
│      YI_202311.csv      # 雲林門牌座標 CSV
│      addresses.db       # SQLite 資料庫（自動生成）
├─outputs                 # 分析結果 DXF 檔案
├─templates               # Flask 模板檔案
│      index.html         # 主頁面
│      result.html        # 結果頁面
└─uploads                 # 上傳的 DXF 檔案
```

---

## 貢獻與授權
- **貢獻**：歡迎提交 Issue 或 Pull Request。
- **授權**：本專案採用 [MIT 授權](LICENSE)。

---


