---
theme: '@cxphoenix/slidev-theme-fhsh-aisp'
addons:
  - tldraw
title: 資安實務課程
fonts:
  sans: 'edukai, Noto Sans Traditional Chinese, Roboto'
  serif: 'Zen Antique, edukai, Noto Serif Traditional Chinese'
  mono: 'Source Code Pro, Noto Sans Mono'
  local:
    - edukai
drawings:
  persist: false
transition: slide-left
mdc: true
skipPageNumberLayouts:
  - cover
layoutsIncludeInToc:
  - section
---

# [CTF]{.font-mono style="display: inline;"} 第一次接觸

## @CXPh03n1x{.font-mono style="display: block;"}

---

# OUTLINE{.font-mono}

<CustomToc />

---
layout: section
---

# 第一次開始接觸

## 你要知道的基本知識

---

# 資安有一堆知識要學

::v-clicks
- 程式語言
- 計算機網路
- 作業系統
- 計算機結構
- 計算機組織
- 系統程式設計
- etc.{.font-mono}
::

---

::center-flex-block{classNames="pb-12"}
:::div{.text-4xl}
資安是整個資訊科學領域的[最後一步]{.text-rose-600 .text-5xl v-mark.red="'-1'"}
:::
::


---

# TERMS {.font-mono}

資安有很多重要名詞你要知道：

::v-clicks{depth='2'}
:::ul{.pl-18 .font-mono}
- C.I.A
  - Confidentiality
  - Integrity
  - Availability
- Risk
- Weakness
- Vulnerability
:::
::

---

# TERMS（cont.）{.font-mono}

當然還有基本的駭客文化相關名詞：

::v-clicks{depth='2'}
:::ul{.pl-18 .font-mono}
- Hacker
  - [The Conscience of a Hacker](https://phrack.org/issues/7/3#article){.text-sky-600 .underline}
  - [The Hacker's Renaissance: A Manifesto Reborn](https://phrack.org/issues/72/19#article){.text-sky-600 .underline}\
    [(同場加映翻譯版本)](https://g.co/gemini/share/811516820e78){.text-orange-600 .underline .text-lg .block .text-end}
- Penetration Testing
- Red team
- Blue team
:::
::

---

# TERMS（cont.）{.font-mono}

你也要知道一些資安常見的開源專案與架構：

::v-clicks{depth='2'}
:::ul{.pl-18 .font-mono}
- [OWASP](https://owasp.org/){.text-sky-600 .underline}
  - [OWASP Top 10](https://owasp.org/www-project-top-ten/){.text-sky-600 .underline}
  - [OWASP WSTG](https://owasp.org/www-project-web-security-testing-guide/){.text-sky-600 .underline}
- [Common Weakness Enumeration (CWE)](https://cwe.mitre.org/){.text-sky-600 .underline}
- [Common Vulnerability and Exposures (CVE)](https://www.cve.org/){.text-sky-600 .underline}
- [Cyber Kill Chain](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html){.text-sky-600 .underline}
- [ATT@CK](https://attack.mitre.org/){.text-sky-600 .underline}
:::
::

---

# TERMS（cont.）{.font-mono}

也有電腦處理時會用到的名詞：

::v-clicks{depth='2'}
:::ul{.pl-18 .font-mono}
- Root
- Priviledge
- Path
- Access
- Request
- Response
- Directory
:::
::

---

# TERMS（cont.）{.font-mono}

當然，還有資安攻擊時會用到的名詞：

::v-clicks{depth='2'}
:::ul{.pl-18 .font-mono}
- Zeroday
- Injection
- Bypass
- Blind
- [Oracle](https://en.wikipedia.org/wiki/Padding_oracle_attack){.text-sky-600 .underline}
- Brute Force
:::
::

---

::center-flex-block{classNames="gap-3 pb-8"}
結束了嗎？

當然還有很多名詞...{v-click}

但真的太多了...所以先停在這{v-click}
::

---

# RECAP{.font-mono}

::v-clicks{depth='2'}
1. 資訊安全領域聚集非常多的知識。
2. 你必須要記得 [C.I.A]{.font-mono}。
3. 至少分清楚 [Weakness]{.font-mono} 和 [Vulnerability]{.font-mono} 的差異。
4. 很多名詞，而且還沒提到一堆縮寫...。
5. 後面你會慢慢記得的。
::

---
layout: section
---

# 我們的訓練

## 各種訓練模式

---

# 我們會用到的訓練：[CTF]{.font-mono}

## Capture The Flag{.font-mono .pl-3}

- 「搶旗賽」。
- 從軍事演練而來。
- 藉由滲透進目標主機，取得特定的「字串」。
- [flag]{.font-mono} 格式通常為：

::div{v-click .text-center .font-mono .text-4xl .text-rose-600 .p-6 .rounded-lg .bg-yellow-200 .mx-10}
競賽名稱\{一串隨機的字串}
::

---

# [CTF]{.font-mono} 模式

多種遊玩模式：

::v-clicks
- [Jeopardy]{.font-mono v-mark.red="+4"}
- Attack & Defense (A&D) {.font-mono}
- King of Hill (KoH) {.font-mono}
::

::div{.absolute .w-full .bottom-20 .text-center .text-3xl v-click="['1', '+1']"}
關卡挑戰型，挑戰一關得到一定分數。
::

::div{.absolute .w-full .bottom-20 .text-center .text-3xl v-click="['2', '+1']"}
攻防模式，互相攻擊各自的主機。
::

::div{.absolute .w-full .bottom-20 .text-center .text-3xl v-click="['3', '+1']"}
占地模式，攻擊四散的主機。
::

::div{.absolute .w-full .bottom-20 .text-center .text-3xl v-click="4"}
基本上我們都是使用 [Jeopardy]{.font-mono} 模式。
::

---

# 除此之外...

## Wargame{.font-mono .pl-4}

::v-clicks
:::ul{.pl-16}
- 傳統闖關式。
- 比速度。
- 闖關到一半停下來後，忘記密碼會很麻煩...{.text-rose-600}
::

---

# 我們先來小試身手

::center-flex-block{classNames="pb-22 font-mono text-3xl"}
[https://buckeye-bazaar.osucyber.club/](https://buckeye-bazaar.osucyber.club/){.text-sky-600 .underline}
::

::div{.absolute .w-[80%] .bottom-14 .left-22 .text-center .text-2xl .bg-yellow-200 .rounded-lg .font-mono .p-5}
flag format: flag\{s0m3th1ng_in_h3r3...}
::

---

# RECAP{.font-mono}

- [CTF]{.font-mono} 用於訓練
- 還有 [Wargame]{.font-mono}
- 你需要跳出框架，才能找洞！

---
layout: section
---

# 開始資安轉生

## 用 [Wargame]{.font-mono style="display: inline;"} 來進入資安世界

---

# 為什麼用 [Wargame]{.font-mono}

::v-clicks
- 因為剛好選到的很多古老的洞。
- 因為可以強迫各位作筆記。
- 因為看看你們的記憶力好不好 [(*´Д`)つ))´∀`)]{.font-mono}。
::

---

# 使用的平台：[Natas]{.font-mono}

![Natas 平台首頁](/natas.png){.w-190 .mx-auto .mt-2}

[https://overthewire.org/wargames/natas/](https://overthewire.org/wargames/natas/){.font-mono .absolute .bottom-8 .right-10 .text-sky-600 .underline}

---

::center-flex-block{classNames="pb-12 gap-4"}
因為前 [2]{.font-mono} 關超級簡單，

所以請你自己完成到 [Natas 2]{.font-mono} 吧！
::

---
layout: image
---

![Natas 2 畫面](/level_2.png)

---

# RECAP{.font-mono}

- 我們用 [Natas]{.font-mono} 來開局
- 記得寫 [Writeup]{.font-mono}。

---
layout: section
skipInToc: true
---

# 今天就上到這～

## 記得做筆記，寫 [Writeup]{.font-mono style="display: inline;"} 喔！