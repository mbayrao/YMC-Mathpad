# YMC-Mathpad

## **Overview**

這是我第一次用Git…有好多操作要學…Work on it...

這款鍵盤靈感來自Summa-Congni/Mathpad，當我在2025年的某日給女朋友看到能夠方便輸入數學符號的Mathpad
她知道我喜歡也能製做出電路板，便鼓勵我著手製作此project而誕生。
此板為第一版設計，製作時有許多問題導致設計不斷變更直到最後。
主要思路為無線藍芽連接內置5V USB Type C充電電路並提供電量指示燈、有OLED螢幕可供視覺回饋挑選符號


* **Wireless**：Buletooth 5
* **Screen Size**：0.96 inch
* **Layout**：正交排列,按鍵數量6(Maxium: 12) 鍵位配置為上、下、左、右、Enter及切換下一頁的Layer鍵
* **MCU**： ESP32-C3FH4
* **Firmware**：自訂韌體(使用Arduino IDE)
* **Battery life**： 5hrs(600mAh lithium batteries)
* **Mathematical Symbols**：56個符號(一頁14個，共四頁)，根據需求還可以再擴充
* **Dimension**：101mm x 87mm x 13mm

## **Features**

使用Gateron Low Profile THT軸體搭配白色矮鍵，
0.96吋雙色I2C OLED螢幕顯示現在電量、數學符號及實際發送文字

數學符號 

Layer1： ±×÷…≤≥≠√∑∏∞αβγ

Layer2： δεμφπσθ∈∉∫∂∆∇≈

Layer3： ≅≡∪∩≃≄∨∧∴∵⊆⊇⊂⊃

Layer4： ⊗⊕⊙∀∃ℕℤℚℝℍℙρ⇒⇔


## **Repository Contents**
此 Repository 包含自行製作一把鍵盤所需的所有檔案：

| Folder | Contents |
| ----- | ----- |
| `/hardware/pcb` | KiCad/Eagle 電路圖、PCB 佈局、Gerber 製造檔、BOM |
| `/hardware/cad` | CAD 原始檔（STEP）、外殼／定位板 STL 輸出檔 |
| `/firmware` | 韌體原始碼 |
| `/keymap` | 鍵位配置／Keymap 定義 |
| `/docs` | 製作指南、配線圖、圖片 |

## **Build Instructions**

1. **PCB**：使用 `/hardware/pcb/gerbers` 中的 Gerber 製造檔，向 \[JLCPCB/PCBWay/其他\] 下單製作。  
2. **Case**：使用 `/hardware/cad` 中的 STEP 檔進行 3D 列印或 CNC 加工。  
3. **Assembly**：請依照 [docs/build-guide.md](https://claude.ai/chat/docs/build-guide.md) 的說明進行組裝。  
4. **Firmware**：依照下方的說明進行韌體燒錄。

## **CAD / Case Files**

* **Format**：STEP（可編輯）、STL（可直接列印）  
* **Software used**：\[Fusion 360 / FreeCAD / SolidWorks\]  
* **Location**：`hardware/cad/`

## **Wiring / Schematic**

完整電路圖 PDF：[hardware/pcb/schematic.pdf](https://claude.ai/chat/hardware/pcb/schematic.pdf)

## **Credits / Acknowledgments**

本專案受到 [Mathpad](https://github.com/Summa-Cogni/Mathpad)（作者：\[nup002\dancergraham]）的啟發，並以其為基礎進行開發。

## **Disclaimer**

本專案為業餘／開源專案，以「現況」提供，不提供任何保固。下單或焊接前，請確認所有元件的規格與額定值符合需求。
