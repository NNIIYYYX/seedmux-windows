# Changelog

<p><strong>English</strong> · <a href="#简体中文">简体中文</a> · <a href="#繁體中文">繁體中文</a></p>

## 0.1.476

- A session you start from your phone in an empty space opens on screen, rather than only in the sidebar.

## 0.1.475

- A pane that comes into view only because another closed waits on its card even before Seedmux has heard whether its session is still there, and starts only when you click it.
- Resuming an archived conversation brings it back to the space, group, and tab it came from, rather than into the space you are in.
- Pinned tabs show at the top of every space and open in the space where you click them.
- The Agents list at the bottom of the sidebar holds only the agents that are working or waiting for you, conversations you go back and forth with for 10 minutes after their last turn, and the ones you choose to keep there.

## 0.1.470

- A message you send while the agent is working keeps its pictures while it waits in the queue, and when you take it back or send it again.
- A picture named in a message shows as a picture wherever its path stands, also right after a dash or a word.
- A pane that comes into view without a running session, when the tab you were on closes or you leave a zoomed pane, waits on a card with its name, folder, and Resume, and starts only when you click it.
- Switching spaces, the window's frame changes color along with the sidebar, and the panes fade out and back in.
- Cards in the right panel open and close without the content shifting along the way, and terminals resize once, when the panel settles.
- Settings: the phone card says which distro it goes through and how that distro is, with the same button the distro's own card offers; Diagnostics gives each distro that is not ready a line; Alerts has Conceal Titles under the Island.

## 0.1.457

- With Solid and still over remote desktop or saving power on, under Settings › Appearance › Window, every window of Seedmux now stops its motion during a remote desktop session or while Windows saves power, scrolling, transitions, and icon animations included. Before, some of them still played.
- Terminal output from WSL is let go of as soon as it is sent, rather than staying in memory a while.

## 0.1.455

- A session from before a restart opens with its conversation when you click it, whatever your settings. The Resume after restart switch is gone: with it off, such a session opened as an empty terminal and lost its conversation. Open last sessions at start still decides whether your sessions open when Seedmux starts.
- Settings › Appearance now changes the space you are in. Its first section, named for the space, has the Own look switch: on, themes, colors, and the window's transparency apply to that space alone; off, to every space that shares one look.
- Every space's menu in the sidebar offers Theme, not only a space with a look of its own.

## 0.1.450

- No visible changes. The code inside was tidied: comments cut to the ones that matter, and the longest functions split into smaller ones, with each screen they draw checked to look exactly as before.

## 0.1.358

- A setting in `config.toml` that holds a value it cannot take falls back on its own, and the rest of the file still applies. A look in `spaces.toml` with one bad value keeps everything else, a `spaces.toml` that does not parse is set aside as `spaces.toml.broken`, and a `themes.toml` that does not load is no longer replaced when you change a theme.
- In Settings, a row with two controls, such as the global hotkey's keys and its switch, disables only the one whose setting `config.local.toml` holds. Search lists results in the order the page shows them.
- In the conversation view, a message, a command, or Send Now waits while Seedmux is still working in the agent's terminal, such as going back to an earlier message or taking back a queued one.
- A pane you archive or delete stays out until its undo runs out, even across a restart. If its session ends within those 5 seconds, Undo brings the conversation back to Archived. A pane you close while its session cannot be reached is ended once it can.
- On the Island, Allow and Reject that come back after an undo notice wait until you move the pointer, so a click meant for the notice does not answer them.
- An uninstall that fails part way puts back what it took out, and Seedmux stays in Settings › Apps so you can run it again.

## 0.1.307

- Settings is redesigned as six pages: Sessions, Appearance, Alerts, Keys, Connections, and Seedmux. Search sits on the same line as the page title, and every page closes from its ×.
- Sessions picks the agent new sessions start with from a row of tiles; the gear on a tile opens that agent's own settings. Each WSL distro and your phone have a page of their own under Connections, and search finds what is on them.
- Alerts lets you choose between Windows notifications and the Island, the notch that shows over other apps. The notch and the Island now work as one: it stays out of the way while idle, comes down only when an agent needs you or a closed tab can be brought back, and lets you allow or reject right from it.
- Keys shows where the summoned window lands on a small screen you can click, and your shortcuts as a list or on a keyboard.
- A space with a look of its own picks its theme and grain from its menu in the sidebar.
- Text that does not fit fades out instead of ending in "…", icons line up with the words beside them, and the Info tab is clearer.

## 0.1.289

- Settings › General has a new switch, Quit ends all sessions, off by default. With it on, quitting Seedmux from the tray, or closing its window when the Close button is set to quit, also ends every session on Windows, in WSL, and on remote hosts. Your panes keep their places and start again the next time you open Seedmux.
- Opening Seedmux again soon after it stopped no longer leaves your WSL sessions out of reach for up to a minute. Updating to this build can still do so once, as the version it replaces stops the old way.

## 0.1.287

- The interface lines up on a 4-pixel grid: panels, controls, dividers, and dialogs keep sharp edges at 125% and other display scales, and English and Chinese text sit on the same line.
- Icons are centered on the words beside them in the sidebar, pane headers, the right panel, and Settings. Buttons and menu items no longer end in "…", and the tray menu no longer cuts off its longest item.
- The Git page is tidier: the branch says how far it is from its upstream only when they differ, each file shows only the counts that are not zero, and a long folder gives way before its counts.
- The sidebar shows a project's sessions and each session's panes as two clear levels.
- Fill Panel is remembered: Restore puts the divider back where it was, and Files fills the panel again after you hide it or restart.
- Closing the first of two tabs in the right panel no longer crashes Seedmux. If Seedmux does crash, the details go to a log beside its others.

## 0.1.273

- Going back to an earlier message in the conversation view holds steady when you switch to the terminal and back: the messages it took back stay out, and the agent's menus wait until it is done.
- Answering an agent's questions from the conversation waits while Seedmux is still working in that agent's terminal.

## 0.1.265

- Seedmux keeps its hooks out of your agents' own settings where it can: pi loads Seedmux's extensions only when it runs in a Seedmux pane, and Antigravity's hook is written only when you start it in one. Settings › Agents lists the agents whose global settings still hold a hook Seedmux wrote.
- Uninstalling also removes Seedmux from your running WSL distros and removes the Codex profile Seedmux created. A distro that was not running is listed with the command to run in it.
- Settings are saved in the background.

## 0.1.246

- In the conversation view, Codex, Antigravity, and OpenCode show their current model as soon as it opens and let you pick a model from it; OpenCode's agents and custom commands and Codex's permissions can be chosen there too.

---

## 简体中文

### 0.1.476

- 从手机在空的空间里新建的会话会直接显示出来，而不是只出现在侧栏里。

### 0.1.475

- 因为别的窗格关闭而露出的窗格，即使 Seedmux 还没确认它的会话在不在，也会先停在卡片上，点了才启动。
- 恢复已归档的会话时，它会回到原来所在的空间、分组和标签页，而不是你当前所在的空间。
- 置顶的标签页在每个空间的顶部都看得到，在哪个空间点开就在哪里打开。
- 侧栏底部的 Agents 列表只放正在工作或等你回应的 agent、最后一轮结束后 10 分钟内的多轮对话，以及你选择留在那里的。

### 0.1.470

- agent 工作时发出的消息，排队等候时、撤回或重发时都会带着图片。
- 消息里提到的图片路径，紧跟在短横线或文字后面时也会显示成图片。
- 你所在的标签页关闭、或退出放大的窗格后露出的没有会话的窗格，会停在一张卡片上，显示名字、文件夹和“恢复会话”，点了才启动。
- 切换空间时，窗口边框的颜色随侧栏一起过渡，窗格先淡出再淡入。
- 右侧面板里的卡片打开和关闭时，内容不再中途挪动；终端只在面板停稳后改一次尺寸。
- 设置：手机卡片写明它经由哪个发行版、那个发行版现在怎样，并带着发行版卡片上的同一个按钮；“诊断”为每个没就绪的发行版列一行；“提醒”页的灵动岛下多了“遮住标题”。

### 0.1.457

- 打开“设置 › 外观 › 窗口”里的“远程桌面和省电时用实色、关动效”后，在远程桌面里或 Windows 省电时，Seedmux 所有窗口的动效都会停下，滚动、过渡和图标动画也不例外；以前其中一部分仍会播放。
- 从 WSL 发出的终端输出，发送后立即释放，不再在内存里多留一阵。

### 0.1.455

- 重启前的会话，点开时总会接上原来的对话，不再受设置影响。“重启后恢复对话”开关已删除：关掉它时，这类会话会以空白终端打开，对话随之丢失。“启动时打开上次的会话”仍决定启动时是否打开会话。
- “设置 › 外观”现在改的是你所在的空间。第一节以空间命名，带“单独的外观”开关：打开时，主题、配色和窗口透明度只作用于这个空间；关掉时，作用于所有共用一套外观的空间。
- 侧边栏里每个空间的菜单都有“主题”，不再只限有单独外观的空间。

### 0.1.450

- 没有可见的变化。整理了内部代码：注释只留必要的，过长的函数拆成小函数，它们画的每个界面都核对过，和之前完全一样。

### 0.1.358

- `config.toml` 里某一项的值不合规则时，只有这一项退回原值，文件里其余的设置照常生效。`spaces.toml` 里的外观有一个值不对时，其余的都保留；`spaces.toml` 无法解析时，会改名为 `spaces.toml.broken` 留着；`themes.toml` 读不出来时，修改配色不再覆盖它。
- 设置里同一行有两个控件时，例如全局热键的按键和开关，只禁用 `config.local.toml` 里写了的那一个。搜索结果按页面上的顺序排列。
- 对话视图里，Seedmux 还在操作 agent 的终端时（例如回到更早的消息、取回排队的消息），发送消息、命令和“现在发送”都会等它做完。
- 归档或删除的窗格，在撤销期结束前一直不会回来，重启也一样。如果会话在这 5 秒内自己结束了，撤销会把对话找回到“已归档”。连接不上会话时关闭的窗格，会在能连上时结束。
- 灵动岛上，撤销提示结束后重新出现的“允许”和“拒绝”，要等你移动指针后才能点，原本点向提示的那一下不会误答它们。
- 卸载中途失败时，已经移除的部分会放回去，Seedmux 也会留在“设置 › 应用”里，可以再运行一次。

### 0.1.307

- 设置页重新设计为六页：会话、外观、提醒、按键、连接和 Seedmux。搜索和页标题在同一行，每一页都能用 × 关闭。
- 在“会话”里用一排图块选新会话默认用的 agent；图块上的齿轮打开这个 agent 自己的设置。每个 WSL 发行版和手机在“连接”下各有自己的页面，搜索也能找到上面的设置。
- 在“提醒”里选择用 Windows 通知还是灵动岛（显示在其他应用上方的刘海）。刘海和灵动岛合为一体：空闲时不打扰，只在 agent 需要你、或有刚关闭的标签页可以找回时落下，并且可以直接在上面允许或拒绝。
- “按键”用一块可以点选的小屏幕显示呼出的窗口落在哪里，快捷键可以按列表或在键盘上查看。
- 有单独外观的空间，可以在侧栏的空间菜单里选主题和颗粒。
- 放不下的文字改为淡出，不再以“…”结尾；图标与旁边的文字对齐；“信息”页更清楚。

### 0.1.289

- “设置 › 通用”新增开关“退出时结束所有会话”，默认关闭。打开后，从托盘退出 Seedmux，或在“关闭按钮”设为退出时关闭窗口，会同时结束 Windows、WSL 和远程主机上的所有会话。窗格保留在原位，下次打开 Seedmux 时重新启动。
- Seedmux 停止后不久再次打开，WSL 会话不再最多一分钟连不上。更新到这一版的那一次仍可能出现一次，因为被替换的旧版仍按原来的方式停止。

### 0.1.287

- 界面对齐到 4 像素网格：面板、控件、分隔线和对话框在 125% 等缩放下边缘清晰，中英文文字落在同一条线上。
- 侧栏、窗格标题、右侧面板和设置里，图标与旁边的文字居中对齐。按钮和菜单项不再以“…”结尾，托盘菜单最长的一项也不再被截断。
- Git 页更清爽：分支只在与上游不一致时才显示相差多少；每个文件只显示不为零的计数；文件夹名太长时先让出位置，不挤占计数。
- 侧栏把项目的会话和会话里的窗格分成清楚的两级。
- “铺满”会被记住：“还原”把分隔线放回原处；隐藏面板或重启后，“文件”仍会铺满面板。
- 关闭右侧面板两个标签中的第一个不再导致 Seedmux 崩溃。万一崩溃，详情会写进与其他日志同处的日志文件。

### 0.1.273

- 在对话视图里回到之前某条消息时，中途切到终端再切回来也不会出岔子：撤回的消息不会再出现，agent 的菜单也会等撤回完成再操作。
- 在对话里回答 agent 的提问时，如果 Seedmux 还在那个 agent 的终端里操作，会等它做完。

### 0.1.265

- Seedmux 尽量不把钩子写进 agent 自己的配置：pi 只在 Seedmux 的窗格里运行时才加载 Seedmux 的扩展；Antigravity 的钩子只在你从 Seedmux 窗格启动它时才写入。“设置 › Agents”会列出全局配置里还留有 Seedmux 钩子的 agent。
- 卸载时会一并清理正在运行的 WSL 发行版里的 Seedmux，并删除 Seedmux 创建的 Codex 配置。没在运行的发行版会列出来，附上要在里面运行的命令。
- 设置改为在后台保存。

### 0.1.246

- 对话视图里，Codex、Antigravity 和 OpenCode 一打开就显示当前模型，并可在其中切换模型；OpenCode 的 agent 和自定义命令、Codex 的权限也可以在那里选择。

---

## 繁體中文

### 0.1.476

- 從手機在空的空間裡新建的工作階段會直接顯示出來，而不是只出現在側欄裡。

### 0.1.475

- 因為別的窗格關閉而露出的窗格，即使 Seedmux 還沒確認它的工作階段在不在，也會先停在卡片上，點了才啟動。
- 恢復已封存的工作階段時，它會回到原本所在的空間、群組和分頁，而不是你目前所在的空間。
- 置頂的分頁在每個空間的頂部都看得到，在哪個空間點開就在哪裡開啟。
- 側欄底部的 Agents 清單只放正在工作或等你回應的 agent、最後一輪結束後 10 分鐘內的多輪對話，以及你選擇留在那裡的。

### 0.1.470

- agent 工作時送出的訊息，排隊等候時、收回或重新送出時都會帶著圖片。
- 訊息裡提到的圖片路徑，緊跟在短橫線或文字後面時也會顯示成圖片。
- 你所在的分頁關閉、或退出放大的窗格後露出的沒有工作階段的窗格，會停在一張卡片上，顯示名稱、資料夾和「恢復工作階段」，點了才啟動。
- 切換空間時，視窗邊框的顏色隨側欄一起過渡，窗格先淡出再淡入。
- 右側面板裡的卡片開啟和關閉時，內容不再中途移動；終端機只在面板停穩後調整一次尺寸。
- 設定：手機卡片寫明它經由哪個發行版、那個發行版現在如何，並附上發行版卡片上的同一個按鈕；「診斷」為每個沒就緒的發行版列一行；「提醒」頁的靈動島下多了「遮住標題」。

### 0.1.457

- 開啟「設定 › 外觀 › 視窗」中的「遠端桌面和省電時用實色、關動效」後，在遠端桌面中或 Windows 省電時，Seedmux 所有視窗的動效都會停下，捲動、轉場和圖示動畫也不例外；以前其中一部分仍會播放。
- 從 WSL 送出的終端機輸出，送出後立即釋放，不再在記憶體裡多留一陣。

### 0.1.455

- 重新啟動前的工作階段，點開時總會接上原來的對話，不再受設定影響。「重新啟動後恢復對話」開關已移除：關閉它時，這類工作階段會以空白終端機開啟，對話隨之遺失。「啟動時開啟上次的工作階段」仍決定啟動時是否開啟工作階段。
- 「設定 › 外觀」現在修改的是你所在的空間。第一節以空間命名，附有「單獨的外觀」開關：開啟時，主題、配色和視窗透明度只套用到這個空間；關閉時，套用到所有共用同一套外觀的空間。
- 側邊欄裡每個空間的選單都有「主題」，不再只限有單獨外觀的空間。

### 0.1.450

- 沒有可見的變化。整理了內部程式碼：註解只留必要的，過長的函式拆成小函式，它們畫的每個介面都核對過，和之前完全一樣。

### 0.1.358

- `config.toml` 裡某一項的值不合規則時，只有這一項退回原值，檔案裡其餘的設定照常生效。`spaces.toml` 裡的外觀有一個值不對時，其餘的都保留；`spaces.toml` 無法解析時，會改名為 `spaces.toml.broken` 留著；`themes.toml` 讀不出來時，修改配色不再覆寫它。
- 設定裡同一列有兩個控制項時，例如全域快速鍵的按鍵和開關，只停用 `config.local.toml` 裡寫了的那一個。搜尋結果依頁面上的順序排列。
- 對話檢視裡，Seedmux 還在操作 agent 的終端機時（例如回到更早的訊息、取回排隊的訊息），傳送訊息、指令和「現在傳送」都會等它做完。
- 封存或刪除的窗格，在復原期結束前一直不會回來，重新啟動也一樣。如果工作階段在這 5 秒內自己結束了，復原會把對話找回到「已封存」。連不上工作階段時關閉的窗格，會在能連上時結束。
- 靈動島上，復原提示結束後重新出現的「允許」和「拒絕」，要等你移動指標後才能點，原本點向提示的那一下不會誤答它們。
- 解除安裝中途失敗時，已經移除的部分會放回去，Seedmux 也會留在「設定 › 應用程式」裡，可以再執行一次。

### 0.1.307

- 設定頁重新設計為六頁：工作階段、外觀、提醒、按鍵、連線和 Seedmux。搜尋和頁面標題在同一行，每一頁都能用 × 關閉。
- 在「工作階段」裡用一排圖塊選新工作階段預設使用的 agent；圖塊上的齒輪會開啟這個 agent 自己的設定。每個 WSL 發行版和手機在「連線」下各有自己的頁面，搜尋也能找到上面的設定。
- 在「提醒」裡選擇用 Windows 通知還是靈動島（顯示在其他應用程式上方的瀏海）。瀏海和靈動島合而為一：閒置時不打擾，只在 agent 需要你、或有剛關閉的分頁可以找回時落下，並且可以直接在上面允許或拒絕。
- 「按鍵」用一塊可以點選的小螢幕顯示叫出的視窗落在哪裡，快捷鍵可以依清單或在鍵盤上檢視。
- 有獨立外觀的空間，可以在側邊欄的空間選單裡選主題和顆粒。
- 放不下的文字改為淡出，不再以「…」結尾；圖示與旁邊的文字對齊；「資訊」頁更清楚。

### 0.1.289

- 「設定 › 一般」新增開關「退出時結束所有工作階段」，預設為關閉。開啟後，從系統匣退出 Seedmux，或在「關閉按鈕」設為退出時關閉視窗，會一併結束 Windows、WSL 和遠端主機上的所有工作階段。窗格保留在原位，下次開啟 Seedmux 時重新啟動。
- Seedmux 停止後不久再次開啟，WSL 工作階段不再最多一分鐘連不上。更新到這一版的那一次仍可能出現一次，因為被取代的舊版仍按原來的方式停止。

### 0.1.287

- 介面對齊到 4 像素網格：面板、控制項、分隔線和對話方塊在 125% 等縮放下邊緣清晰，中英文文字落在同一條線上。
- 側欄、窗格標題、右側面板和設定中，圖示與旁邊的文字置中對齊。按鈕和選單項目不再以「…」結尾，系統匣選單最長的一項也不再被截斷。
- Git 頁更清爽：分支只在與上游不一致時才顯示相差多少；每個檔案只顯示不為零的計數；資料夾名稱太長時會先讓出位置，不擠佔計數。
- 側欄把專案的工作階段和工作階段裡的窗格分成清楚的兩層。
- 「鋪滿」會被記住：「還原」把分隔線放回原處；隱藏面板或重新啟動後，「檔案」仍會鋪滿面板。
- 關閉右側面板兩個分頁中的第一個不再導致 Seedmux 當機。萬一當機，詳細資訊會寫進與其他記錄檔同處的記錄檔。

### 0.1.273

- 在對話檢視中回到先前某則訊息時，中途切到終端機再切回來也不會出錯：撤回的訊息不會再出現，agent 的選單也會等撤回完成再操作。
- 在對話中回答 agent 的提問時，如果 Seedmux 還在那個 agent 的終端機裡操作，會等它完成。

### 0.1.265

- Seedmux 盡量不把鉤子寫進 agent 自己的設定：pi 只在 Seedmux 的窗格裡執行時才載入 Seedmux 的擴充功能；Antigravity 的鉤子只在你從 Seedmux 窗格啟動它時才寫入。「設定 › Agents」會列出全域設定裡還留有 Seedmux 鉤子的 agent。
- 解除安裝時會一併清理正在執行的 WSL 發行版中的 Seedmux，並刪除 Seedmux 建立的 Codex 設定檔。沒在執行的發行版會列出來，附上要在其中執行的指令。
- 設定改為在背景儲存。

### 0.1.246

- 對話檢視中，Codex、Antigravity 與 OpenCode 一開啟就顯示目前的模型，並可在其中切換模型；OpenCode 的 agent 與自訂指令、Codex 的權限也可以在那裡選擇。
