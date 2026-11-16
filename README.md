# Vultr 評判：$2.5 的機器夠用嗎？客服與退款會不會踩雷？哪個方案最划算？（附全套餐價格表與隱藏計費規則）

Vultr 最低 $2.50/月能開一台 IPv6 Only 的小機器，$5/月拿到 1 vCPU、1GB 記憶體、25GB SSD 和 1TB 流量。它適合願意自己管伺服器、要機房多、要帳單看得懂的人；代價是只有工單支援、帳戶餘額官方明文不退、機器關機不刪除照樣計費。

下面按你真正會遇到的順序講：哪一檔夠用、Regular 和 High Performance 差在哪、哪些計費規則會讓你多付錢、負評集中在哪，最後給不同情況的選擇規則。

> **多數人的答案**
> 只有靜態網站、測試機、小 API：Regular 1GB / $5。
> 要跑 WordPress、資料庫、任何吃磁碟 I/O 的東西：直接上 High Performance 1GB / $6，一個月只多 $1。
> 只想試 Kubernetes：VKE 控制平面免費，只付 worker node 的錢。
> 👉 [先看目前所有方案的實際價格](https://www.vultr.com/pricing/?ref=9738262-9J)

## Vultr 方案與價格：從 $2.5 入門機到 8 卡 GPU

Vultr 的雲端主機分成兩條主線。Regular Performance 走共享 CPU 配一般 SSD，是同系列裡最便宜的；High Performance 換上 AMD EPYC 或 Intel Xeon 加 NVMe SSD，同規格只貴 $1 到 $3。以下價格為第三方整理的現行價目，**實際費用以官網結帳頁為準**，各地區可能略有差異。

### Regular Performance（共享 CPU + 一般 SSD）

| 方案 | vCPU / 記憶體 | 儲存 | 月費 | 開機 |
| --- | --- | --- | --- | --- |
| Regular IPv6 Only | 1 / 0.5GB | 10GB | $2.50 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| Regular | 1 / 0.5GB | 10GB | $3.50 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| Regular | 1 / 1GB | 25GB | $5 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| Regular | 1 / 2GB | 55GB | $10 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| Regular | 2 / 2GB | 65GB | $15 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| Regular | 2 / 4GB | 80GB | $20 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| Regular | 4 / 8GB | 160GB | $40 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| Regular | 6 / 16GB | 320GB | $80 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| Regular | 8 / 32GB | 640GB | $160 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| Regular | 16 / 64GB | 1280GB | $320 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| Regular | 24 / 96GB | 1600GB | $640 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |

### High Performance（新世代 CPU + NVMe SSD）

| 方案 | vCPU / 記憶體 | 儲存 | 月費 | 開機 |
| --- | --- | --- | --- | --- |
| HP | 1 / 1GB | 25GB | $6 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| HP | 1 / 2GB | 50GB | $12 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| HP | 2 / 2GB | 60GB | $18 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| HP | 2 / 4GB | 100GB | $24 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| HP | 4 / 8GB | 180GB | $48 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| HP | 4 / 12GB | 260GB | $72 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| HP | 8 / 16GB | 350GB | $96 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| HP | 12 / 24GB | 500GB | $144 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |

兩條線的頻寬額度也不同。同樣 1GB 記憶體，$5 的 Regular 給 1TB 流量，$6 的 High Performance 給 2TB，等於多付 $1 換 NVMe 加一倍流量。

### Storage Optimized（大容量、低 CPU 密度）

| 方案 | vCPU / 記憶體 | 儲存 | 月費 | 開機 |
| --- | --- | --- | --- | --- |
| SO | 1 / 8GB | 150GB | $75 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| SO | 2 / 16GB | 320GB | $125 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| SO | 2 / 16GB | 480GB | $155 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| SO | 4 / 32GB | 640GB | $250 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| SO | 4 / 32GB | 960GB | $310 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| SO | 8 / 64GB | 1280GB | $500 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| SO | 8 / 64GB | 1920GB | $620 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| SO | 16 / 128GB | 2560GB | $1,000 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| SO | 16 / 128GB | 3840GB | $1,240 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| SO | 24 / 192GB | 3840GB | $1,500 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| SO | 24 / 192GB | 5760GB | $1,850 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| SO | 32 / 256GB | 5760GB | $2,000 | [ 選購](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |

這一線的邏輯是每 vCPU 配 8GB 記憶體起跳，適合自建資料庫、日誌堆疊、影音快取這類「要磁碟不要核心」的工作。單純架網站買這個是浪費。

### Cloud GPU（按 GPU 小時計價）

| GPU 機型 | GPU 數 / 記憶體 | 單價 | 開機 |
| --- | --- | --- | --- |
| AMD Instinct MI300X | 8 / 192GB HBM3 | $1.841 / GPU / 小時 | [ 選購](https://www.vultr.com/products/bare-metal/?ref=9738262-9J) |
| NVIDIA GH200 | 1 / 96GB | $2.990 / GPU / 小時 | [ 選購](https://www.vultr.com/products/bare-metal/?ref=9738262-9J) |
| NVIDIA HGX H100 | 8 / 640GB | $2.300 / GPU / 小時 | [ 選購](https://www.vultr.com/products/bare-metal/?ref=9738262-9J) |
| NVIDIA L40S | 8 / 384GB | $0.848 / GPU / 小時 | [ 選購](https://www.vultr.com/products/bare-metal/?ref=9738262-9J) |
| NVIDIA HGX A100 | 8 / 640GB | $1.490 / GPU / 小時 | [ 選購](https://www.vultr.com/products/bare-metal/?ref=9738262-9J) |
| NVIDIA A100 PCIe | 4 / 320GB | $1.290 / GPU / 小時 | [ 選購](https://www.vultr.com/products/bare-metal/?ref=9738262-9J) |

GPU 機器的租用門檻比其他產品高，後面「真實成本」一節會講。

### 其他產品線

| 產品 | 起價 | 計費方式 | 前往 |
| --- | --- | --- | --- |
| Managed Databases（PostgreSQL / MySQL / Valkey / Kafka） | $15/月 | 固定月費 | [ 看資料庫方案](https://www.vultr.com/products/managed-databases/?ref=9738262-9J) |
| Object Storage（S3 相容） | $6/月，含 1TB 儲存與 1TB 流出 | 月費 + 超量 | [ 看物件儲存](https://www.vultr.com/products/object-storage/?ref=9738262-9J) |
| Block Storage（NVMe / HDD） | 按容量月計 | 依容量 | [ 看區塊儲存](https://www.vultr.com/products/block-storage/?ref=9738262-9J) |
| Kubernetes Engine（VKE） | 控制平面免費 | 只付 worker node | [ 看 VKE](https://www.vultr.com/kubernetes/?ref=9738262-9J) |

VKE 這條值得單獨看。AWS EKS 和 GCP GKE 的託管控制平面一般每月收 $70 以上，Vultr 把控制平面做成免費，你只為實際跑的節點付錢。想練 Kubernetes 又不想先付一筆固定費用的話，這是它少數明顯優於大廠的地方。

## 哪一檔夠你用：按場景給答案

先分三種情況，再談升級。

**0.5GB 的 $2.50 / $3.50 方案**：只適合當跳板機、DNS 節點、監控探針、Tailscale 中繼這類不吃記憶體的角色。$2.50 那檔只有 IPv6，沒有 IPv4 地址，如果你的 ISP 或使用者環境不支援 IPv6，等於連不上。跑 WordPress 會直接記憶體不足，不要省這 $1.5。

**1GB / $5（Regular）vs 1GB / $6（High Performance）**：這是全文最值得記住的一組對比。多 $1 你得到 NVMe SSD 和 2TB 流量。個人部落格、小型靜態站、爬蟲、簡單 API，$5 夠了；只要機器上有資料庫或會頻繁讀寫檔案，$6 的版本在磁碟等待時間上差距明顯，一個月 $12 的價差不值得省。

**2GB 這一段**：Regular $10 給 1 vCPU、55GB SSD、2TB 流量；High Performance $12 給 1 vCPU、50GB NVMe、3TB 流量。儲存少了 5GB，換來 NVMe 和更多流量。跑 WordPress 加 WooCommerce、小型 SaaS、GitLab 這一級，選 $12。

**4GB 以上**：Regular $20（2 vCPU / 80GB）對上 HP $24（2 vCPU / 100GB NVMe / 5TB）。到這個規模通常已經有真實流量，$4 的差價佔比很小，直接上 HP。真的要壓成本、工作負載又是純 CPU 運算（例如批次轉檔），Regular 才有意義。

**多人團隊、多個站**：不要把所有東西塞進一台大機器。開三台 $6 的 HP，比開一台 $48 的 HP 更容易做隔離和備份，掛一台不影響其他站。

👉 [從 Cloud Compute 頁面挑你要的規格](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J)

## 真實成本：五個會讓你多付錢的規則

這一段是多數評測沒有講清楚的部分，也是決定你適不適合用 Vultr 的關鍵。

**1. 關機不等於停止計費，要 Destroy**

Vultr 官方 FAQ 的原文意思是：處於停止狀態的實例仍會保留專屬的系統資源，因此在銷毀（Destroy）該實例之前都會持續產生費用。實務上最常見的踩坑情境是：開一台 $40 的機器測一小時，按了關機就出門，三週後帳單照樣寄來。不想再付錢只有一個動作，就是把實例徹底刪除。

**2. 帳戶餘額不退，官方文件寫得很清楚**

Vultr 的官方說明文件直接寫明：服務不提供退款，所有付款為最終付款，額度不可退還。這代表你存進去的錢只能拿去抵消費，不能提領。多位 G2 用戶反映存入數百美元後專案搬走、錢拿不回來；Trustpilot 上也有「儲值未反映在帳單」「綁卡後被扣款而沒有說明」這類抱怨。這些是使用者陳述，但方向與官方不退款的規定一致。儲值前先確認你真的會用完。

**3. 大額機器與 GPU 有額外的風控門檻**

Trustpilot 上有具體案例：有人要租每月約 $400 的 bare metal（vbm-8c-64gb-amd），註冊時先被要求 $5 綁卡，再被要求 $50 存款，之後仍被「Monthly Fee Limit Reached」擋下，客服還要求他 30 天內再消費 $250 才「解鎖」。另一則是要租 GPU，存了 $1,000 之後被告知要等 60 天，期間只能開少數 $5/月的節點。這些是單一用戶的陳述，不能當成通則，但如果你打算一次上大機器或 GPU，先開小機器跑一段時間、養一下帳號，會比直接衝大額方案省事。

**4. 計費單位是一小時，月費有上限**

絕大多數 Cloud Compute 方案按小時計費，每月上限 672 小時。意思是即使當月有 744 小時，全月開著也只收你月費那個數字，不會超過。5 分鐘和 59 分鐘同價，最低計費單位就是 1 小時。VX1 與 GPU 產品改用當月實際小時數計算，沒有 672 小時上限。發票在每月 1 號產生，結算上月用量；mid-cycle 升級會看到兩筆按比例拆分的費用。

**5. 附加項與流量**

每個帳戶每月有 2TB 免費出站流量，加上各實例自己的額度，超量 $0.01/GB，入站免費。快照 $0.05/GB/月（以壓縮後大小計），備份是方案價加 20%，DDoS 保護 $10/月/實例，Windows 授權另計，每個實例含一個公網 IPv4、Reserved IP 每月 $3。這些加起來不貴，但會讓人對「$5 一個月」產生錯誤期待。

另外，已部署的機器要降規格並不直覺，用戶在 TrustRadius 上把「難以輕易降配」列為主要缺點。實務做法多半是開一台小的、把資料搬過去、Destroy 舊的。

👉 [先看清楚目前各方案的實際單價，再決定要不要一次儲值](https://www.vultr.com/pricing/?ref=9738262-9J)

## 用戶評價怎麼讀：哪些是 Vultr 的問題，哪些是 VPS 的共性

G2 上 4.3 分、288 則評論，TrustRadius 的美國區評論裡 59% 提到相較其他供應商有明顯成本節省。正面的具體說法集中在幾件事：開機快（2 分鐘內能開出 72 核 512GB 或 512MB 的機器）、API 與 Terraform provider 好用、帳單扁平透明（有團隊說比原本用超大規模雲端省約 40%，財務不用再審 50 頁帳單）、映像選擇多（Ubuntu、LAMP、OpenVPN 開機即用）。一位 30 年 IT 從業者、用了五年以上，說從未遇到重大宕機，IP 信譽乾淨到可以拿來做郵件主機。也有從 Azure 搬過來的團隊說，Azure 設定繁瑣，Vultr 幾分鐘就能建好環境。

負面集中在三處。

**支援只有工單和自助資源。** G2、TrustRadius 的評論一致指出 Vultr 沒有電話、沒有即時線上聊天，只有 email／help desk 加 FAQ、論壇、知識庫。回覆速度和複雜問題的解決能力，個體差異很大：有人說「responsive、top tier」，也有人說問了半天只得到複製貼上的回覆。Trustpilot 上有客服八小時以上只回「不要重複開單」的案例，也有 Hackathon 參賽者週末被風控鎖住、連 API key 都設不了、週末沒人處理的經驗。這是自助式雲端的共性，不是 Vultr 獨有，但它的自助資源深度確實不如大廠。

**穩定性多數正面，有零星反例。** 多數長期用戶說沒遇過長時間宕機，維護或節點重啟會提前通知。同時 TrustRadius 上有「noisy neighbor」影響效能的說法，Trustpilot 有人稱機器無預警自行重啟。共享 CPU 的方案本來就有鄰居干擾的可能，這一點在選 Regular 時要有心理準備。

**安全與合規要自己扛。** 防火牆設定錯誤、作業系統過期，Vultr 不會主動警告你；被入侵時常見處理是把你的 IP null-route（直接離線）直到你自己修好。條款上也有限制，有使用者反映條款不允許任何加密貨幣相關網站，這是單一說法，但如果你要做這類專案，先讀條款。

## 規模、機房與不適合的人

Vultr 2014 年成立，母公司是 The Constant Company，官方口徑是全球 32 個雲端資料中心、服務 185 個國家、超過 150 萬客戶、累計部署 4,500 萬個以上實例。機房數量是它相對 DigitalOcean、Linode 這一梯隊的主要賣點之一，可以按使用者地理位置選點，對延遲敏感的事案有實際幫助。至於亞洲節點的實際延遲，資料裡沒有可靠的統一測速數字，建議你註冊後用官方提供的測試位址或自己 ping 一遍再決定開在哪一區。

不適合的情況也說清楚：

- 需要 turn-key 服務的架構，例如批次處理、訊息匯流排、進階安全與監控，Vultr 的服務廣度仍低於大型廠商
- 團隊裡沒有人願意管伺服器、管備份、管系統更新
- 需要電話或即時聊天支援才能安心
- 想要買了就自動幫你調校、修補、監控的託管服務

AWS 和 Azure 在託管服務的廣度上更完整，代價是同級價格高出一截；反過來說，如果你只需要便宜、乾淨、開機快的純算力，而且能自己處理作業系統，Vultr 的價格效能比是很難被說服去換的。想要便宜又有人幫你管，通常得透過 Cloudways 這類把 Vultr 當底層的託管平台，那是另一種成本結構。

## 常見問題

**Vultr 可以退款嗎？**
不行。官方說明文件寫明所有付款為最終付款、額度不可退還。這是全文最需要提前知道的一條。

**有免費試用嗎？**
官網目前以新用戶額度為主要招徠，首頁標示 $300 Code Credit 這類活動。這類促銷額度通常有三個限制：限首次註冊的新客戶、有效期約 30 天、只能用於部分產品，而且要先把信用卡或 PayPal 綁好完成驗證才會入帳（會有一筆小額暫時授權，幾天內釋放）。註冊當下就要在 Billing 頁面輸入，事後補不了。實際額度與條件以官網註冊頁當前活動為準，不要預設一定拿得到 $300。

**按小時計費怎麼算？開一小時多少錢？**
以 $5 的方案為例，官網標示約 $0.007/小時。最低計費單位是 1 小時，開 5 分鐘和 59 分鐘同價。大多數方案有每月 672 小時上限，超過也不會多收。

**關機就不收錢了嗎？**
不是。停止狀態的實例仍保留資源並持續計費，只有 Destroy 才會停。

**可以降規格嗎？**
可以，但不直覺。用戶普遍反映降配流程麻煩，實務上常是另開一台小機器、搬資料、銷毀舊機。

**亞洲機房快不快？**
Vultr 在亞太多個地點有節點，但延遲取決於你的使用者和線路。資料裡沒有可信的統一延遲數字，建議開機後實測。

## 下單前確認兩件事

按你的情況選：

- 純測試、跳板、監控：$2.50（IPv6）或 $3.50，記得用完就 Destroy
- 個人網站、小型 API：Regular 1GB / $5
- WordPress、資料庫、任何吃 I/O 的服務：High Performance 1GB / $6，這 $1 不要省
- 小型 SaaS、多站託管：High Performance 2GB / $12 起
- 練 Kubernetes：VKE，控制平面免費
- 自建資料庫、日誌：Storage Optimized，從 $75 起

下單前確認兩件事：一，機器不用了就 Destroy，不要只關機；二，先看清楚官網當前的促銷額度與有效期，再決定要儲值多少，因為存進去的錢不會退。

👉 [從官網目前方案開始，挑一台用完就刪的機器試水溫](https://bit.ly/VuLtr)
