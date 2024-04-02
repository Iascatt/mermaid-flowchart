# Markdown с mermaid
 Диаграмма МАСТЕР-ПРИБОР
```mermaid
flowchart TD

subgraph gr2["ПРИБОР"]
direction TB
title[<b>Блок ПРИБОР</b>]
h1(["BPEMЯ=Tслом"])==> h2["сост:=<br>сломан"]
h2 ==> h3(["режим=<br>работа"])
h3 ==> h4(["мастер<br>=своб"])
h4 ==> h5["мастер:=занят<br>Tрем:=funс(x)"]
h5 ==> h6(["ВРЕМЯ=Трем"])
h6 ==> h7["сост:=рабочий<br>мастер:=своб<br>Tслом:=func(x)"]
h7 ==> h1
h2 -.->par3((сост))
h7 -.->par3
par1((режим))-.->h3
par2((мастер))-.->h4
h5 -.->par2
h7 -.->par2
h5 -.->par4((Трем))
par4 -.-> h6
p99[\I/] -.- h1
h99[/"Тслом = 100ч"\]
end

subgraph gr1["МАСТЕР"]
direction TB
title[<b>Блок МАСТЕР</b>]
h8["режим:-<br>отдых"]==> h9(["ВРЕМЯ=Траб"])
h8 -.->par1((режим))
par2((мастер))-.->h13
h9 ==> h10["режим:=работа<br>Тотд:=func__"]
h10 ==> h11(["ВРЕМЯ=Tотд"])
h11 ==> h12["Траб:=func__"]
h10 -.->par1
h12 ==> h13{"мастер<br>-..."}
h13 ==> |...=занят|h14["Трем:=Трем+<br>Траб-ВРЕМЯ"]
h14 ==> h8
h13 ==> |...=своб|h8
h14 -.->par4((Трем))
p98[\I/] -.- h8
h98[/"Траб = 9ч"\]
click par2 href "https://iu5.bmstu.ru" "переход для Мастера" _blank;
end

classDef cond fill:#bee,stroke:#aaa,stroke-width:1px;
classDef state fill:#9e8,stroke:#333,stroke-width:1px;
classDef navig fill:yellow,stroke:#333,stroke-width:1px;
class h13 navig;
class h5,h8,h2,h7,h8,h10,h12,h14 state;
class h1,h3,h4,h6,h9,h11,h13 cond;
style par1 fill:#fcc,stroke:#111,stroke-width:2px;
style par2 fill:#fae,stroke:#bbb,stroke-width:2px;
style par4 fill:#ccc,stroke:#555,stroke-width:2px;
style title fill:yellow,stroke:red;

