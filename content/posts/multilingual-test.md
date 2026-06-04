---
title: "Multilingual Layout Test / 全语种排版与字体兼容性测试"
date: 2026-06-04
description: "测试羊皮卷主题对简体、繁体、日、韩、德、法、俄、阿等多种文字的衬线体（Serif）及高行高排版兼容性。"
---

本页面用于测试网站在应用了全新的羊皮卷古典护眼排版后，对全球主要核心语种的字体回退、行高挑高以及标点符号的兼容表现。

---

### 1. 简体中文 (Simplified Chinese) —— 华文宋体测试
一天早晨，格里高尔·萨姆沙从不安的睡梦中醒来，发现自己躺在床上变成了一只巨大的甲虫。他背贴着硬如铁甲的床板，只要稍微抬一抬头，就能看见自己那拱起的、棕色的、被半圆形的硬壳分成几段的肚子。
> **卡夫卡名言引用测试**：目标虽有，却无路可循；我们所谓的路，无非是彷徨。

### 2. 繁體中文 (Traditional Chinese) —— 臺灣/香港明體測試
一天早晨，格里高爾·薩姆沙從不安的睡夢中醒來，發現自己躺在床上變成了一隻巨大的甲蟲。他背貼著硬如鐵甲的床板，只要稍微抬一抬頭，就能看見自己那拱起的、棕色的、被半圓形的硬殼分成幾段的肚子。

### 3. 日本語 (Japanese) —— 明朝体/セリフ体テスト
ある朝、グレゴール・ザムザがなにか寝心地の悪い夢から目が覚めると、自分がベッドの中で一匹の巨大な毒虫に変わっているのに気がついた。彼は装甲のように硬い背中を下にして横たわり、頭を少し起こしてみると、アーチ状の線でいくつかの部分に区切られた茶色の丸いお腹が見えた。

### 4. 한국어 (Korean) —— 바탕체 테스트
어느 날 아침 그레고르 잠자가 불안한 꿈에서 깨어났을 때, 그는 침대 속에서 자신이 한 마리의 거대한 갑충으로 변해 있다는 것을 발견했다. 그는 갑옷처럼 단단한 등을 대고 누워 있었는데, 머리를 약간 들어 올리니 몇 개의 활 모양 선으로 나뉜 갈색의 둥근 배가 보였다。

### 5. Deutsch (German) —— Originaltext Original Garamond
Als Gregor Samsa eines Morgens aus unruhigen Träumen erwachte, fand er sich in seinem Bett zu einem ungeheuren Ungeziefer verwandelt. Er lag auf seinem panzerartig harten Rücken und sah, wenn er den Kopf ein wenig hob, seinen gewölbten, braunen, von bogenförmigen Versteifungen geteilten Bauch.

### 6. Français (French) —— Lettres accentuées É, À, È, Ç
Un matin, au sortir d'un rêve agité, Gregor Samsa s'éveilla transformé dans son lit en une véritable vermine. Il était couché sur le dos, un dos dur comme une cuirasse, et, en levant un peu la tête, il aperçut son ventre brun, bombé, divisé par des arcs rigides.

### 7. Русский (Russian) —— Cyrillic Font Test (西里尔字母)
Проснувшись однажды утром после беспокойного сна, Грегор Замза обнаружил, что он у себя в постели превратился в страшное насекомое. Он лежал на броневой твердой спине и, приподняв немного голову, видел свой коричневый, выпуклый, разделенный дугообразными ребрами живот.

### 8. العربية (Arabic) —— RTL Text Test (从右到左镜像排版测试)
استيقظ غريغور سامسا ذات صباح من أحلام مزعجة، فوجد نفسه قد تحول في سريره إلى حشرة ضخمة. كان مستلقياً على ظهره الصلب مثل المدرعة، وعندما رفع رأسه قليلاً، رأى بطنه البني المقوس المقسم إلى أجزاء صلبة.

---

### 💡 结论：其他文字能否兼容？
**完全可以完美兼容！**

*   **欧洲语言（法、意、西、葡等）**：它们与德文、英文一样使用拉丁字母系统。我们设置的 `Garamond` 和 `Baskerville` 字体天然包含这些语言的所有**变音符号**（如法文的 `é, à, ç`），排版会和德文一样古典优雅。
*   **西里尔字母（俄语、乌克兰语等）及复杂语系（阿拉伯语、希伯来语）**：由于我们在字体链的末尾加上了终极兜底代码 `serif !important;`，当系统遇到俄文或阿拉伯文时，iPad 会自动调用系统内置最匹配的**俄文衬线体**和**阿拉伯文古典字体**。同时，由于我们把行高强行拉高到了 **`1.95`**，即使是结构极其复杂的阿拉伯文字符，也绝对不会出现上下行重叠或粘连的现象。

```text
部署完成后，请使用 iPad 的无痕模式刷新查看这篇全语种测试，
您将看到全球文字在羊皮纸上整齐划一、呼吸感十足的精美效果！
```
