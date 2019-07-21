# NSSLab Thesis Template

本專案目前僅支援 IEEE 論文模板。

---
## Installation

> 關於安裝資訊：https://www.latex-project.org/get/#tex-distributions

* Windows
    * 安裝 [MiKTeX](https://miktex.org/)
* MacOS
    * 安裝 [MacTeX](http://www.tug.org/mactex/)
* Linux
    * 安裝 [TeXLive](https://www.tug.org/texlive/)
* Online LaTeX Service
    * [Overleaf](https://www.overleaf.com)

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
## Description

```bash
# In alphabetical order
nsslab-thesis-template
├── Bib/                        # 參考書目
│   └── thesis.bib
├── Chapters/                   # 論文各節內容 (可自行新增)
│   ├── 0-Abstract.tex
│   ├── 1-Introduction.tex
│   ├── 2-RelatedWork.tex
│   ├── 3-Design.tex
│   ├── 4-Evaluation.tex
│   └── 5-Conclusion.tex
├── Class/                      # 論文模板
│   └── IEEEtran.cls
├── Config/                     # 相關參數設定
│   └── config.tex              
├── Figurs/                     # 論文圖片 (可自行新增)
│   └── ...
├── .gitignore                  # 檔案忽略清單 (不需更動)
├── CONTRIBUTING.md             # 說明文件：如何貢獻本專案
├── GNUmakefile                 # 編譯論文檔案所用 
├── LICENSE                     # 專案授權 (不需更動)
├── main.tex                    # 論文主要檔案
├── main.pdf                    # 論文輸出檔案
└── README.md                   # 說明文件 (本檔案)
```

* [`main.tex`](main.tex)：論文主要檔案
* [`main.pdf`](main.pdf)：論文輸出檔案
* [`GNUmakefile`](GNUmakefile)：編譯論文檔案所用，生成的 PDF 檔案會在 `Output/` 資料夾下
* [`Bib/`](Bib/)：論文參考書目
    * [`main.tex`](Bib/main.tex)：引入 `thesis.bib` 所用
    * [`thesis.bib`](Bib/thesis.bib)：參考書目的內容
* [`Chapters/`](Chapters/)：論文各節內容 (可自行新增)
* [`Class/`](Class/)：論文模板
    * [`IEEEtran.cls`](Class/IEEEtran.cls)：IEEE 論文格式
* [`Config/`](Config/)：相關參數設定
    * [config.tex](Config/config.tex)：設定論文題目、作者資訊等
* [`Figures/`](Figures/)：論文圖片 (可自行新增)

---
## Useful Plugins

* **LaTeX Workshop** (on Visual Studio Code)
    * 透過 `Ctrl + S` 存檔時進行編譯，但是編譯檔案會出現在 `Output/` 資料夾外。
    * 備註：LaTeX Workshop 有時會出現無法按下 `Enter` 的錯誤訊息，可以改安裝 `v6.0` 版本就會解決。

---
## Reference

* [The LaTex Project](https://www.latex-project.org/)
* [CTAN](https://www.ctan.org/)
* [LaTeX Wikibooks](https://en.wikibooks.org/wiki/LaTeX)

---
## Contributor

> **NOTICE:** You can follow the contributing process [CONTRIBUTING.md](CONTRIBUTING.md) to join me. I am very welcome any issue!

This website is dedicatd for all members in Networking and Sensing Systems Laboratory (NSSLAB).

* [David Lu](https://github.com/yungshenglu)

---
## License

[GNU GENERAL PUBLIC LICENSE Version 3](LICENSE)