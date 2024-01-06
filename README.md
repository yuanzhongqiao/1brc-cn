<div class="Box-sc-g0xbh4-0 bJMeLZ js-snippet-clipboard-copy-unpositioned" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><h1 tabindex="-1" dir="auto"><a id="user-content-1️⃣️-the-one-billion-row-challenge" class="anchor" aria-hidden="true" tabindex="-1" href="#1️⃣️-the-one-billion-row-challenge"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1️⃣🐝🏎️十亿行挑战</font></font></h1>
<p dir="auto"><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1 月 1 日状态：本次挑战</font></font><a href="https://www.morling.dev/blog/one-billion-row-challenge/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">开放提交</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">！</font></font></em></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">十亿行挑战 (1BRC) 是一次有趣的探索，探讨现代 Java 在聚合文本文件中的 10 亿行方面能走多远。</font><font style="vertical-align: inherit;">抓住所有（虚拟）线程，使用 SIMD，优化 GC，或使用任何其他技巧，并创建最快的实现来解决此任务！</font></font></p>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="/gunnarmorling/1brc/blob/main/1brc.png"><img src="/gunnarmorling/1brc/raw/main/1brc.png" alt="1BRC" style="width: 50%; max-width: 100%;"></a></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">该文本文件包含一系列气象站的温度值。</font><font style="vertical-align: inherit;">每一行都是格式为 的一个测量值</font></font><code>&lt;string: station name&gt;;&lt;double: measurement&gt;</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，测量值恰好有一个小数位。</font><font style="vertical-align: inherit;">以下以十行为例：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>Hamburg;12.0
Bulawayo;8.9
Palembang;38.8
St. John's;15.2
Cracow;12.6
Bridgetown;26.9
Istanbul;6.2
Roseau;34.4
Conakry;31.2
Istanbul;23.0
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="Hamburg;12.0
Bulawayo;8.9
Palembang;38.8
St. John's;15.2
Cracow;12.6
Bridgetown;26.9
Istanbul;6.2
Roseau;34.4
Conakry;31.2
Istanbul;23.0" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">任务是编写一个 Java 程序，该程序读取文件，计算每个气象站的最低、平均和最高温度值，并在标准输出上发出结果，如下所示（即按气象站名称的字母顺序排序，每个气象站的结果值在格式</font></font><code>&lt;min&gt;/&lt;mean&gt;/&lt;max&gt;</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，四舍五入到一位小数）：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>{Abha=-23.0/18.0/59.2, Abidjan=-16.2/26.0/67.3, Abéché=-10.0/29.4/69.0, Accra=-10.1/26.4/66.4, Addis Ababa=-23.7/16.0/67.0, Adelaide=-27.8/17.3/58.5, ...}
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="{Abha=-23.0/18.0/59.2, Abidjan=-16.2/26.0/67.3, Abéché=-10.0/29.4/69.0, Accra=-10.1/26.4/66.4, Addis Ababa=-23.7/16.0/67.0, Adelaide=-27.8/17.3/58.5, ...}" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在 2024 年 1 月 31 日之前提交您的实现并成为排行榜的一部分！</font></font></p>
<h2 tabindex="-1" dir="auto"><a id="user-content-results" class="anchor" aria-hidden="true" tabindex="-1" href="#results"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">结果</font></font></h2>
<table>
<thead>
<tr>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">#</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">结果（分：秒.毫秒）</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">执行</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">JDK</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">提交者</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1.</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:07.999</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_royvanrijn.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-graal</font></font></td>
<td><a href="https://github.com/royvanrijn"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">罗伊·范·赖恩</font></font></a></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:10.589</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_artsiomkorzun.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-graal</font></font></td>
<td><a href="https://github.com/artsiomkorzun"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">阿齐奥姆·科尔尊</font></font></a></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3.</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:10.613</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_spullara.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-graal</font></font></td>
<td><a href="https://github.com/spullara"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">萨姆·普拉拉</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:10.870</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_ebarlas.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-格雷斯</font></font></td>
<td><a href="https://github.com/ebarlas"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">埃利奥特·巴拉斯</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:12.988</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_isolgpus.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/isolgpus"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">杰米·斯坦斯菲尔德</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:13.430</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_jotschi.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/Jotschi"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">约翰内斯·舒特</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:13.463</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_yemreinci.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/yemreinci"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">耶姆赖因吉</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:13.857</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_filiphr.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-graal</font></font></td>
<td><a href="https://github.com/filiphr"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">菲利普·赫里萨福夫</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:14.411</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_deemkeen.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/deemkeen"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">迪姆肯</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:16.196</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_artpar.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/artpar"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">帕斯穆德加尔</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:17.905</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_lawrey.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/peter-lawrey"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">彼得·劳瑞</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:18.789</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_palmr.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/palmr"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">尼克·帕尔默</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:19.561</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_gabrielreid.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/gabrielreid"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">加布里埃尔·里德</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:22.709</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_seijikun.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-graal</font></font></td>
<td><a href="https://github.com/seijikun"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">马库斯·艾伯纳</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:23.078</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_richardstartin.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/richardstartin"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">理查德·斯塔廷</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:24.351</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_yavuztas.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-graal</font></font></td>
<td><a href="https://github.com/yavuztas"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">严酷塔斯</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:24.879</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_davecom.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/davecom"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">大卫·科佩克</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:26.576</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_fatroom.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/fatroom"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">罗曼·罗曼丘克</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:27.787</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_nstng.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/nstng"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">尼尔斯·塞梅尔洛克</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:28.167</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_truelive.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/truelive"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">罗曼·施韦策</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:32.764</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_moysesb.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/moysesb"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">莫伊塞斯·博尔赫斯·福尔塔多</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:34.848</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_armandino.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/armandino"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">阿曼·谢里夫</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:36.518</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_rby.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/rby"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">拉姆齐·本·叶海亚</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:38.510</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_bjhara.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/bjhara"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">汉普斯拉姆</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:50.547</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_padreati.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/padreati"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">奥雷利安·图图亚努</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:51.678</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_twobiers.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-tem</font></font></td>
<td><a href="https://github.com/twobiers"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">飞鸟</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">00:53.679</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_criccomini.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/criccomini"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">克里斯·里科米尼</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">01:24.721</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_Ujjwalbharti.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/Ujjwalbharti"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">乌吉瓦尔·巴蒂</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">01:27.912</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_jgrateron.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/jgrateron"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">雅罗·格拉特隆</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">01:58.536</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_kuduwa_keshavram.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/kuduwa_keshavram"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">库杜瓦·克沙夫拉姆</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">02:00.101</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_khmarbaise.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/khmarbaise"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">克马尔拜色</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">02:08.315</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_itaske.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/itaske"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">伊塔斯克</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">02:16.635</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_anandmattikopp.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/anandmattikopp"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">两难事</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">02:23.316</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_abfrmblr.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/AbfrmBlr"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">阿比拉什</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">03:42.297</font></font></td>
<td><a href="https://github.com/gunnarmorling/1brc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage_fragmede.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关联</font></font></a></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/fragmede"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">参孙</font></font></a></td>
</tr>
<tr>
<td></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">04:13.449</font></font></td>
<td><a href="https://github.com/gunnarmorling/onebrc/blob/main/src/main/java/dev/morling/onebrc/CalculateAverage.java"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">链接</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">（基线）</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">21.0.1-开放</font></font></td>
<td><a href="https://github.com/gunnarmorling"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">冈纳·莫林</font></font></a></td>
</tr>
</tbody>
</table>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">请参阅</font></font><a href="#entering-the-challenge"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">下面的</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">说明，了解如何使用您自己的实现来参加挑战。</font></font></p>
<h2 tabindex="-1" dir="auto"><a id="user-content-prerequisites" class="anchor" aria-hidden="true" tabindex="-1" href="#prerequisites"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">先决条件</font></font></h2>
<p dir="auto"><a href="https://openjdk.org/projects/jdk/21/" rel="nofollow"><font style="vertical-align: inherit;"></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您的系统上必须安装</font><a href="https://openjdk.org/projects/jdk/21/" rel="nofollow"><font style="vertical-align: inherit;">Java 21 。</font></a></font></p>
<h2 tabindex="-1" dir="auto"><a id="user-content-running-the-challenge" class="anchor" aria-hidden="true" tabindex="-1" href="#running-the-challenge"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">运行挑战</font></font></h2>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">该存储库包含两个程序：</font></font></p>
<ul dir="auto">
<li><code>dev.morling.onebrc.CreateMeasurements</code><font style="vertical-align: inherit;"></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">（通过create_measurements.sh</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">调用）：</font><font style="vertical-align: inherit;">在此项目的根目录中</font><font style="vertical-align: inherit;">创建文件</font></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">measurements.txt ，其中包含可配置数量的随机测量值</font></font></em><font style="vertical-align: inherit;"></font></li>
<li><code>dev.morling.onebrc.CalculateAverage</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">（通过</font></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">calculate_average_baseline.sh调用）：计算文件</font></font></em><font style="vertical-align: inherit;"><em><font style="vertical-align: inherit;">measurements.txt</font></em><font style="vertical-align: inherit;">的平均值</font></font><em><font style="vertical-align: inherit;"></font></em></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">执行以下步骤来运行挑战：</font></font></p>
<ol dir="auto">
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用 Apache Maven 构建项目：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>./mvnw clean verify
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="./mvnw clean verify" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">创建包含 1B 行的测量文件（仅一次）：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>./create_measurements.sh 1000000000
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="./create_measurements.sh 1000000000" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">这将需要几分钟的时间。
</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">注意：</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">生成的文件大小约为。</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">12 GB</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，因此请确保有足够的磁盘空间。</font></font></p>
</li>
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">计算平均测量值：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>./calculate_average_baseline.sh
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="./calculate_average_baseline.sh" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">提供的简单示例实现使用 Java 流 API 来处理文件，并在用于</font></font><a href="#evaluating-results"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">结果评估</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">的环境中在大约 2 分钟内完成任务。</font><font style="vertical-align: inherit;">它可以作为比较您自己的实现的基线。</font></font></p>
</li>
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">优化它：</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">以您认为合适的任何方式调整</font></font><code>CalculateAverage</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">程序以加快速度（只需遵守下面描述的一些规则）。</font><font style="vertical-align: inherit;">选项包括并行计算、使用（孵化）Vector API、同时内存映射文件的不同部分、使用 AppCDS、GraalVM、CRaC 等来加速应用程序启动、选择和调整垃圾收集器，以及多得多。</font></font></p>
</li>
</ol>
<h2 tabindex="-1" dir="auto"><a id="user-content-flamegraphprofiling" class="anchor" aria-hidden="true" tabindex="-1" href="#flamegraphprofiling"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">火焰图/分析</font></font></h2>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">提示是，如果您安装了</font></font><a href="https://jbang.dev" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">jbang</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ，您可以通过</font><a href="https://github.com/jvm-profiling-tools/ap-loader"><font style="vertical-align: inherit;">ap-loader运行</font></a></font><a href="https://github.com/jvm-profiling-tools/async-profiler"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">async-profiler</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">来获取程序的火焰图
</font><font style="vertical-align: inherit;">：</font></font><a href="https://github.com/jvm-profiling-tools/ap-loader"><font style="vertical-align: inherit;"></font></a><font style="vertical-align: inherit;"></font></p>
<p dir="auto"><code>jbang --javaagent=ap-loader@jvm-profiling-tools/ap-loader=start,event=cpu,file=profile.html -m dev.morling.onebrc.CalculateAverage_yourname target/average-1.0.0-SNAPSHOT.jar</code></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">或者直接在 .java 文件上：</font></font></p>
<p dir="auto"><code>jbang --javaagent=ap-loader@jvm-profiling-tools/ap-loader=start,event=cpu,file=profile.html src/main/java/dev/morling/onebrc/CalculateAverage_yourname</code></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">当您运行它时，它将在 profile.html 中生成火焰图。</font><font style="vertical-align: inherit;">然后您可以在浏览器中打开它并查看您的程序在哪里花费了时间。</font></font></p>
<h2 tabindex="-1" dir="auto"><a id="user-content-rules-and-limits" class="anchor" aria-hidden="true" tabindex="-1" href="#rules-and-limits"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">规则和限制</font></font></h2>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">可以使用以下任何 Java 发行版：
</font></font><ul dir="auto">
<li><font style="vertical-align: inherit;"><a href="https://sdkman.io/jdks" rel="nofollow"><font style="vertical-align: inherit;">SDKMan</font></a><font style="vertical-align: inherit;">提供的任何构建</font></font><a href="https://sdkman.io/jdks" rel="nofollow"><font style="vertical-align: inherit;"></font></a></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">可以使用 openjdk.net 上提供的早期访问版本（包括 Valhalla 等 OpenJDK 项目的 EA 版本）</font></font></li>
<li><font style="vertical-align: inherit;"></font><a href="https://builds.shipilev.net/openjdk-jdk-lilliput/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在builds.shipilev.net</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">上构建</font><font style="vertical-align: inherit;">
如果您想使用无法通过这些渠道获得的构建，请联系我们讨论是否可以考虑。</font></font></li>
</ul>
</li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">不能使用外部库依赖项</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">实现必须作为单个源文件提供</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">计算必须在应用程序</font></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">运行时进行，即您无法在</font></font></em><font style="vertical-align: inherit;"></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">构建时</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">处理测量文件</font><font style="vertical-align: inherit;">
（例如，使用 GraalVM 时）并将结果烘焙到二进制文件中</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">输入值范围如下：
</font></font><ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">站名称：非空 UTF-8 字符串，最小长度为 1 个字符，最大长度为 100 个字符</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">温度值：-99.9（含）和 99.9（含）之间的非空双精度数，始终带有一位小数</font></font></li>
</ul>
</li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">最多有 10,000 个唯一的站名</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">实现不得依赖于给定数据集的细节，例如必须支持根据上述约束的任何有效站名称和任何数据分布（每个站的测量数量）</font></font></li>
</ul>
<h2 tabindex="-1" dir="auto"><a id="user-content-entering-the-challenge" class="anchor" aria-hidden="true" tabindex="-1" href="#entering-the-challenge"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">进入挑战</font></font></h2>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要将您自己的实施提交给 1BRC，请按照以下步骤操作：</font></font></p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"></font><a href="https://github.com/gunnarmorling/onebrc/"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">创建onebrc</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> GitHub 存储库的分支</font><font style="vertical-align: inherit;">。</font></font></li>
<li><font style="vertical-align: inherit;"></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">创建CalculateAverage.java</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">的副本</font><font style="vertical-align: inherit;">，命名为</font></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">CalculateAverage_&lt;your_GH_user&gt;.java</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，例如</font></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">CalculateAverage_doloreswilson.java</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">加快实施速度。</font><font style="vertical-align: inherit;">真的很快。</font></font></li>
<li><font style="vertical-align: inherit;"></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">创建一份calculate_average_baseline.sh</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">的副本</font><font style="vertical-align: inherit;">，命名为</font></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">calculate_average_&lt;your_GH_user&gt;.sh</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，例如</font></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">calculate_average_doloreswilson.sh</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">调整该脚本，使其引用您的实现类名称。</font><font style="vertical-align: inherit;">如果需要，请通过</font></font><code>JAVA_OPTS</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">该脚本中的变量提供任何 JVM 参数。</font><font style="vertical-align: inherit;">确保脚本除了计算结果之外不会将任何内容写入标准输出。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenJDK 21 是默认值。</font><font style="vertical-align: inherit;">如果需要自定义 JDK 构建，请</font></font><code>sdk use java [version]</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在应用程序启动之前将 SDKMAN 命令包含在启动 shell 脚本中。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">（可选）如果您想使用本机二进制文件 (GraalVM)，请调整</font></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">pom.xml</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文件，以便它构建该二进制文件。</font></font></li>
<li><font style="vertical-align: inherit;"></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">通过执行/test.sh &lt;your_GH_user&gt;</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">运行测试套件</font><font style="vertical-align: inherit;">；</font><font style="vertical-align: inherit;">如果报告有任何差异，请在提交实施之前修复它们。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">针对上游存储库创建拉取请求，明确说明
</font></font><ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您的实现类的名称。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">程序在您系统上的执行时间及其规格（CPU、核心数量、RAM）。</font><font style="vertical-align: inherit;">这仅供参考，官方运行时间将按如下所述确定。</font></font></li>
</ul>
</li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我将运行该程序并确定其性能（如下一节所述），并将结果输入记分板。</font></font></li>
</ul>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">注意：</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果我对实施感到怀疑，我保留不评估特定提交的权利（即我不会运行你的比特币矿工；）。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您想与社区讨论任何实施 1BRC 的潜在想法，您可以使用此存储库的</font></font><a href="https://github.com/gunnarmorling/onebrc/discussions"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GitHub 讨论</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font><font style="vertical-align: inherit;">请保持友好和文明。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">挑战持续到 2024 年 1 月 31 日。在 2024 年 1 月 31 日 23:59 UTC 之后创建的任何提交（即拉取请求）将不予考虑。</font></font></p>
<h2 tabindex="-1" dir="auto"><a id="user-content-evaluating-results" class="anchor" aria-hidden="true" tabindex="-1" href="#evaluating-results"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">评估结果</font></font></h2>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="https://www.hetzner.com/cloud" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">结果通过在Hetzner Cloud CCX33 实例</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">（8 个专用 vCPU、32 GB RAM）</font><font style="vertical-align: inherit;">上运行程序来确定。</font><font style="vertical-align: inherit;">该</font></font><code>time</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">程序用于测量执行时间，即测量端到端时间。</font><font style="vertical-align: inherit;">每个竞争者将连续运行五次。</font><font style="vertical-align: inherit;">最慢和最快的运行将被丢弃。</font><font style="vertical-align: inherit;">剩余三轮比赛的平均值是该竞争者的结果，并将添加到上面的结果表中。</font><font style="vertical-align: inherit;">完全相同的</font></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">measurements.txt</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文件用于评估所有竞争者。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您想在 Hetzner Cloud 上启动自己的盒子进行测试，您可能会发现这些</font></font><a href="https://github.com/gunnarmorling/cloud-boxes/"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">设置脚本</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">（基于 Terraform 和 Ansible）很有用。</font><font style="vertical-align: inherit;">请注意，这将产生您需要承担的费用，我不会支付您的云账单:)</font></font></p>
<h2 tabindex="-1" dir="auto"><a id="user-content-prize" class="anchor" aria-hidden="true" tabindex="-1" href="#prize"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">奖</font></font></h2>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您参加此挑战，您可能会学到新东西，激励他人，并为看到您的名字列在上面的记分牌上而感到自豪。</font><font style="vertical-align: inherit;">有传言获胜者还可能获得一件独特的 1️⃣🐝🏎️ T 恤！</font></font></p>
<h2 tabindex="-1" dir="auto"><a id="user-content-faq" class="anchor" aria-hidden="true" tabindex="-1" href="#faq"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">常问问题</font></font></h2>
<p dir="auto"><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">问：我可以使用 Kotlin 或 Java 之外的其他 JVM 语言吗？</font></font></em><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">
答：不，本次挑战仅针对 Java。</font><font style="vertical-align: inherit;">不过，请随意非正式地分享明显优于任何列出结果的实现。</font></font></p>
<p dir="auto"><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">问：我可以使用非 JVM 语言和/或工具吗？</font></font></em><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">
答：不，本次挑战仅针对 Java。</font><font style="vertical-align: inherit;">不过，请随意非正式地分享有趣的实现和结果。</font><font style="vertical-align: inherit;">例如，看看 DuckDB 如何完成这项任务将会很有趣。</font></font></p>
<p dir="auto"><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">问：我已经有了一个实现，但它不是用 Java 编写的。</font><font style="vertical-align: inherit;">我可以在某个地方分享吗？</font></font></em><font style="vertical-align: inherit;"><a href="https://github.com/gunnarmorling/1brc/discussions/categories/show-and-tell"><font style="vertical-align: inherit;">答：虽然非 Java 解决方案无法正式提交挑战，但欢迎您在Show and Tell</font></a><font style="vertical-align: inherit;"> GitHub 讨论区</font></font><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">
分享。</font></font><a href="https://github.com/gunnarmorling/1brc/discussions/categories/show-and-tell"><font style="vertical-align: inherit;"></font></a><font style="vertical-align: inherit;"></font></p>
<p dir="auto"><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">问：我可以使用 JNI 吗？</font></font></em><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">
答：提交内容必须完全用Java实现，即不能用C/C++编写JNI粘合代码。</font><font style="vertical-align: inherit;">不过，您可以通过 GraalVM 使用 Java 代码的 AOT 编译，可以通过 AOT 编译整个应用程序，也可以通过创建本机库（请参阅</font></font><a href="https://www.graalvm.org/22.0/reference-manual/native-image/ImplementingNativeMethodsInJavaWithSVM/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">此处</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">.</font></font></p>
<p dir="auto"><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">问：measurements.txt 文件的编码是什么？</font></font></em><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">
答：文件是用UTF-8编码的。</font></font></p>
<p dir="auto"><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">问：我可以对数据集中显示的气象站名称做出假设吗？</font></font></em><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">
答：不，虽然数据集生成器仅使用一组固定的电台名称，但任何解决方案都应该适用于任意 UTF-8 电台名称（为了简单起见，保证名称不包含任何</font></font><code>;</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">字符）。</font></font></p>
<p dir="auto"><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">问：我可以复制其他提交的代码吗？</font></font></em><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">
答： 是的，可以。</font><font style="vertical-align: inherit;">挑战的主要焦点是学习新东西，而不是“获胜”。</font><font style="vertical-align: inherit;">当您这样做时，请注明相关来源提交的内容。</font><font style="vertical-align: inherit;">请不要重新提交没有改进或仅有微不足道改进的其他条目。</font></font></p>
<p dir="auto"><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">问：使用哪个操作系统进行评估？</font></font></em><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">
答：费多拉 39。</font></font></p>
<p dir="auto"><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">问：为什么</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1️⃣🐝🏎️ </font></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">？</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">A ：</font></font><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">
这是项目名称的缩写：</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">One </font></font></strong> <strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Billion </font></font></strong><font style="vertical-align: inherit;"></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">R</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ow </font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Challenge</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<h2 tabindex="-1" dir="auto"><a id="user-content-license" class="anchor" aria-hidden="true" tabindex="-1" href="#license"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">执照</font></font></h2>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">此代码库可在 Apache 许可证版本 2 下使用。</font></font></p>
<h2 tabindex="-1" dir="auto"><a id="user-content-code-of-conduct" class="anchor" aria-hidden="true" tabindex="-1" href="#code-of-conduct"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">行为守则</font></font></h2>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">彼此都要优秀！</font><font style="vertical-align: inherit;">这次挑战的目的不仅仅是获胜，还在于获得乐趣并学习新知识。</font></font></p>
</article></div>
