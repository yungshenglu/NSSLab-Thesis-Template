# NSSLab Thesis Template

本專案目前僅支援 IEEE 論文模板

---
## Compilation

1. 執行以下指令進行編譯
    ```bash
    # Make sure your current directory is correct
    $ make
    ```
    * 需等待 2-3 秒，若編譯成功，則不會有任何錯誤訊息。
    * 編譯成功後會自動生成 PDF 檔案 `main.pdf` 在 `Output/` 下。
2. 如何移除編譯過程所產生的中間檔案 (e.g., `main.aux`, `main.bbl`, `main.blg`, etc.)？
    ```bash
    # Make sure your current directory is correct
    $ make clean
    ```
    * 中間檔案為非必要檔案，已經寫入 `.gitignore` 中。

---
## File Structure

* [`main.tex`](main.tex)：論文主要檔案
* [`GNUmakefile`](GNUmakefile)：編譯 LaTex 檔案所用，生成的 PDF 檔案會在 `Output/` 資料夾下
* [`Class/`](Class/)：論文格式設定
    * [`IEEEtran.cls`](Class/IEEEtran.cls)：IEEE 論文格式
    * [`main.sty`](Class/main.sty)：設定常用的共同參數
* [`Chapters/`](Chapters/)：論文主要內容 (可自行新增)
    * [`main.tex`](Chapters/main.tex)：引入各章節的檔案所用
* [`Bib/`](Bib/)：論文參考書目
    * [`main.tex`](Bib/main.tex)：引入 `thesis.bib` 所用
    * [`thesis.bib`](Bib/thesis.bib)：參考書目的內容
* [`Figures/`](Figures/)：論文圖片 (可自行新增)
* [`Output/`](Output/)：輸出 PDF 檔案

---
## Useful Plugins

* **LaTex Workshop**
    * 透過 `Ctrl + S` 存檔時進行編譯，但是編譯檔案會出現在 `Output/` 資料夾外。
    * 備註：LaTex Workshop v7.0 有時會出現無法按下 `Enter` 的錯誤訊息，可以改安裝 `v6.0` 版本就會解決。

---
## Contributor

> **NOTICE:** You can follow the contributing process [CONTRIBUTING.md](CONTRIBUTING.md) to join me. I am very welcome any issue!

* [David Lu](https://github.com/yungshenglu)

---
## License

[GNU GENERAL PUBLIC LICENSE Version 3](LICENSE)