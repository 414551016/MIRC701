# 林盈達

## [Reinforcement Learning-Driven Honeypots: Tactic-Based Defense for Industrial Control Systems," IEEE Transactions on Machine Learning in Communications and Networking, to appear.](https://github.com/414551016/MIRC701/blob/main/Papers/%E6%9E%97%E7%9B%88%E9%81%94/Reinforcement_Learning-Driven_Honeypots_Tactic-Based_Defense_for_Industrial_Control_Systems.pdf)
> 強化學習驅動的蜜罐：工業控制系統的基於策略的防禦
> 發表日期： 2026 年 4 月 17 日  版本的最終更新日期（current version）為 2026 年 4 月 28 日
> 這份研究提出了一種基於強化學習（Reinforcement Learning）的動態誘餌系統（Honeypot），旨在解決傳統工業控制系統（ICS）防禦工具反應僵化且易被看穿的缺陷。該系統透過將網路行為映射至 MITRE ATT&CK for ICS 框架，能即時根據駭客的攻擊階段採取延遲、修改或阻斷等欺敵策略，進而延長對手的參與時間。實驗顯示，相較於停留在早期階段的靜態誘餌，這種自適應防禦（Adaptive Defense）能引導攻擊者進入更深層的殺傷鏈，藉此蒐集更具價值的威脅情資。最終，這項技術為保護能源、水力等關鍵基礎設施提供了一種能與時俱進、自動優化欺敵邏輯的高階安全方案。
> 
### 摘要
這篇研究針對工業控制系統（ICS）強化學習（Reinforcement Learning, RL）驅動的適應性誘捕系統（Honeypot），旨在解決傳統誘捕系統因反應固定、容易被攻擊者識破而導致無法捕捉深層攻擊行為的問題。

以下是該研究摘要的核心重點：
- 核心問題：
  > 傳統的 ICS 誘捕系統設計過於靜態，攻擊者在幾次互動後就能辨識其偽裝，這限制了防禦者對攻擊鏈（Kill Chain）後期階段的了解。
- 解決方案：
  > 研究團隊將強化學習嵌入誘捕系統中，使其能根據攻擊者的行為實時調整回應策略。該系統參考了 MITRE ATT&CK for ICS 框架，將每次網路互動映射為具體的攻擊戰術，並利用 Q-learning 演算法 來選擇最佳的欺敵行動（如延遲回應、修改數據或阻斷特定指令）
- 評估與結果：
  研究透過 Metasploit 腳本模擬真實的 ICS 攻擊場景，並對比了三種配置：
  - Static0： 預設的靜態誘捕系統
  - Static1： 經過手動增強、支援更多功能碼的變體
  - Dynamic (RL-driven)： 本研究提出的強化學習適應性系統
- 關鍵成效：
  實驗證明，靜態誘捕系統的攻擊深度通常停留在戰術等級 4 或 7，而 RL 驅動的系統能在 700 次互動循環內引誘攻擊者到達最後的戰術階段。此外，該系統將攻擊者的平均參與時間增加了一倍以上（從約 17 秒延長至超過 70 秒），並能在部署早期就提供深層的威脅情報
- 研究價值：
  此研究顯示 RL 增強型誘捕系統具有自主學習與適應能力，能有效引誘攻擊者深入攻擊鏈，為防禦者提供更完整且具價值的 ICS 威脅情報
