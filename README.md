# 於AzureML部署客製化模型及存取
【撰寫時間：2023/4/30 writen by Markov Chen】

2023 AI EXPO向我們展示大模型的時代已經來臨，Winner-Take-All的趨勢商業結構改變了整個產業的商業價值與定位，許多業者也重新開始思考高階人才對於公司而言是甚麼樣的存在？從工作價值、職責規劃到適任條件，該如何面對新時代的職場生態是每個人都須認清的課題。

資訊科技從過去 **[材料能源]>[電腦]>[通訊技術]>[伺服器]>[巨量數據]** 發展到現在的 **[AI/區塊鏈]** ，每個主題在其所處的時代都會有其結構性的關鍵工作。而經歷了將近百年多研究的AI也成為了現代所有研發量能的核心，無論是化學、電機、機械、電子或資訊或是其它相關領域，過去在工程上難以分析處理的數學、統計問題都在這項技術的幫助下迎刃而解，藉此衍伸出更高的 **"服務/產品"** 水準，因此業界也開始出現了一種專門為不同主題提供AI解決方案的新工作 -*「資料科學家」*。

近幾個月迅速崛起的生成式AI對於**產品導向**的半導體及電子相關產業而言也無疑是一項激勵，無論是自動化製造、知識管理、客戶服務或人機協同都增強了對資料科學的依賴。然而，這些內容對硬體設備的規格與要求也急遽提升，例如：NVIDIA在一顆V100 GPU的情況下要訓練出1024 * 1024的影像生成模型[StyleGAN3](https://nvlabs-fi-cdn.nvidia.com/stylegan3/stylegan3-paper.pdf)大約就需要92年的時間。尤其是考慮到擁有多個事業群的企業，龐大的資料中心與計算的時間、成本將會是AI導入的關鍵。除了那些擁有關鍵資源的網路巨擘，我們很難想像每間企業都能夠擁有自己獨立的大模型訓練伺服器(就像是說他們通通都要有google規模等級的機房)，除了在經濟上不切實際之外，這樣無疑也會對全球ESG帶來沉重的負擔。因此，這些處於結構洞的網路巨擘紛紛開始起到領頭羊的角色，透過**雲端**向企業們提供AI應用開發的關鍵資源，諸如資料中心、GPU運算、Foundation模型、線上推論API、環境工具...等，希望能夠藉由這樣的專業化分工幫助各個產業更好地發揮其本身所具有的商業價值。

對於大部分的"一般"非資深的資料科學家而言，我們首要考量的不應只局限於模型的優化與調校(這主要也是理論型學者的工作)，而是更著重於這些現成的AI模型在產業上該如何應用。雲端的開發能力便是其中不可或缺的基本功，因為混合Edge和Cloud的工作環境將會成為業界的一種常態(它們之間如何取捨則需視各家的資安規範而定)，但不可否認的是它絕對會是一種更為高效的開發模式。因此這個`repository`的目的就是為這個基本的開發流程提供一個釋例，透過AzureML實現深度學習於PCB-AoI的應用。

## 目錄

- [開發工具](#背景)

## 目錄

![](https://i.imgur.com/CJoI8uZ.png)
![](https://i.imgur.com/xJ3jZdA.png)
