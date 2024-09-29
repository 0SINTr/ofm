# OSINT Funnel Methodology
**OFM - Methodology for OSINT Investigations**

[![Stable Release](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/0SINTr/ofm/releases/tag/v1.0.0)
[![Last Commit](https://img.shields.io/github/last-commit/0SINTr/ofm)](https://github.com/0SINTr/ofm/commits/main)

**OSINT Funnel Methodology** for creating a coherent data collection workflow in person-based investigations.

![ofm_2024](img/ofm.png)

## OFM GOAL
The main goal of OFM is to provide a clear path for performing the **Data Collection** phase of an OSINT investigation, so that enough and diverse data can be passed further to the **Data Process & Analysis** phases. With hundreds of websites, services and CLI tools available, conducting a coherent research may be overwhelming. For this reason, the OSINTer should have a clear, easy-to-follow plan for collecting data in an organized manner.

**Important!**
- This methodology refers to **passive, non-intrusive OSINT tasks**.
- The mentioned tools are just examples, not an exhaustive list.
- The OFM methodology only addresses the **Data Collection** phase.
- The OFM best fits OSINT investigations related to individuals.
- Any OSINT investigations should be preceded by [**proper OpSec**](https://github.com/0SINTr/ooo).

## Stages
**OFM** is meant to be followed in a **top-down approach**, starting with the widest types and methods of searching for data, and gradually implementing increasingly specialized tools and techniques. In the end, all the collected data is funneled into the **Data Process & Analysis** phase.

### STAGE 1: Search Engines
- The main goal of this stage is to **collect more PII** (Personal Identifiable Information, e.g. email addresses and/or usernames) about the target. The discovery of new PII is useful both for **recursively searching the web** for more data on the target, as well as **feeding this PII to specialized OSINT tools** during Stages 2-5.
- This stage may sometimes collect **the most amount of data**, although this data may be quite scattered and raw in the absence of any kind of automation or filtering algorithm.
- For each search engine, **manual** or **automated** (API-based) **advanced search and scrape** methods can be applied to filter the results via built-in operators or patterns, and also to organize the data in structured formats e.g. **JSON**.
- Furthermore, **recursive searching and scraping** should be applied for each piece of **PII** collected during previous searches. This can be done best by using an automated tool.
- The **tools** used in this stage are the most **well-known search engines**, either queried manually or programmatically:
    - [Google Advanced Search](https://www.google.com/advanced_search)
    - [Bing Advanced Search](https://support.microsoft.com/en-us/topic/advanced-search-keywords-ea595928-5d63-4a0b-9c6b-0b769865e78a)
    - [Yandex Advanced Search](https://yandex.com/support/search/query-language/search-operators.html)
    - [Yahoo Advanced Search](https://search.yahoo.com/web/advanced)
    - [DuckDuckGo Advanced Search](https://duckduckgo.com/duckduckgo-help-pages/results/syntax/)
    - [Qwant Advanced Search](https://help.qwant.com/en/docs/qwant-search/searching/comment-utiliser-les-raccourcis-de-recherche-qwick/)
    - [Startpage Advanced Search](https://support.startpage.com/hc/en-us/articles/4521473758228-Advanced-Search-on-Startpage)
- Automated OSINT tool **G.R.A.S.S. - Google Recursive Advanced Search & Scrape**:
    - [osintr](https://github.com/0SINTr/osintr)

### STAGE 2: Specialized Tools
- After the first wave of (more or less) relevant data has been collected and filtered from search engines, the next step is to use **specialized OSINT tools** on the most relevant bits of data that have been collected during Stage 1 (usernames, email addresses, phone numbers, profile URLs etc.).
- These tools are meant as additional filters for the OSINT investigation, however they can also provide **new insights and leads** on the target's online presence. Combining these tools with the advanced searches from the previous stage may already build a significant portion of the target's **digital footprint**.
- Some of the **tools** used in this stage are:
    - **Username** search:
        - [Sherlock](https://github.com/sherlock-project/sherlock)
        - [Maigret](https://github.com/soxoj/maigret)
        - [Whatsmyname](https://whatsmyname.app/)
        - [Spiderfoot](https://github.com/smicallef/spiderfoot)
        - [Marple](https://github.com/soxoj/marple)
        - [Mailcat](https://github.com/sharsil/mailcat)
        - [IntelTechniques User Tools](https://inteltechniques.com/tools/Username.html)
        - [Bellingcat People Toolkit](https://bellingcat.gitbook.io/toolkit/categories/people)
    - **Email** search:
        - [Holehe](https://github.com/megadose/holehe)
        - [Epieos](https://epieos.com/)
        - [Ghunt](https://github.com/mxrch/GHunt)
        - [Spiderfoot](https://github.com/smicallef/spiderfoot)
        - [theHarvester](https://github.com/laramies/theHarvester)
        - [Whoxy](https://www.whoxy.com/)
        - [IntelTechniques Email Tools](https://inteltechniques.com/tools/Email.html)
        - [Bellingcat People Toolkit](https://bellingcat.gitbook.io/toolkit/categories/people)

### STAGE 3: Social Avenues
- The information collected in the previous two steps may point to one or more **social media profiles** that the target is using. These profiles may include, but not be limited to, well-known social media services - **Facebook**, **Instagram**, **TikTok**, **X** or **Reddit**, secondary or emerging social networks such as **Bluesky** or **Truth Social**, blogs, forums, or chat rooms such as **Telegram**, **Discord**, **Slack** etc.
- Any of these avenues can lead to discovering more information about the target, either **personal** (age, birthday, photos, workplace, locations, friends) or **ideological** such as political, cultural, religious or sexual preferences, among others. Any such lead can further unravel a suite of pathways to explore, and can also help paint a better picture of the target. This research is **mostly manual**, however the **tools** below may provide additional or faster insight.
    - [Socid-Extractor](https://github.com/soxoj/socid-extractor): Extract data from specified URL
    - [Ignorant](https://github.com/megadose/ignorant): Phone number to Snapchat or Instagram
    - [Toutatis](https://github.com/megadose/toutatis): Extract data from Instragram page
    - [Quidam](https://github.com/megadose/Quidam): Extract data via forgotten login
    - [Nqntnqnqmb](https://github.com/megadose/nqntnqnqmb): Extract LinkedIn information
    - [Cqfd](https://github.com/megadose/cqfd): Get Skype ID from name
    - [Telemetryapp](https://www.telemetryapp.io/): Telegram API
    - [Gitfive](https://github.com/mxrch/GitFive): Search GitHub users
    - [IntelTechniques Facebook Search](https://inteltechniques.com/tools/Facebook.html)
    - [IntelTechniques Twitter Search](https://inteltechniques.com/tools/Twitter.html)
    - [IntelTechniques Instagram Search](https://inteltechniques.com/tools/Instagram.html)
    - [IntelTechniques LinkedIn Search](https://inteltechniques.com/tools/Linkedin.html)
    - [IntelTechniques Communities (Reddit, TikTok etc.)](https://inteltechniques.com/tools/Communities.html)
    - [Bellingcat Social Media Toolkit](https://bellingcat.gitbook.io/toolkit/categories/social-media)

### STAGE 4: Data Breaches
- Websites and APIs providing information and search capabilities on **data breaches and pastes** can sometimes prove to be extremely rewarding, especially if the previous steps have not provided a great deal of data about the target. Finding breaches that the target's username or email address has been a part of can provide crucial clues on some of the platforms where the target has (or at least had) accounts or profiles. Furthermore, this type of searches can easily be **automated** via Python scripts and libraries, at very low API costs. Of course, this can again lead to manual research once one or more pieces of data have been found.
- Typical **tools** in this step are:
    - [HaveIBeenPwned](https://haveibeenpwned.com/)
    - [Dehashed](https://dehashed.com/)
    - [Snusbase](https://snusbase.com/)
    - [LeakCheck](https://leakcheck.io/)
    - [CheckLeaked](https://checkleaked.cc/)
    - [Pastebin](https://pastebin.com/)
    - [IntelX](https://intelx.io/)
    - [H8Mail](https://github.com/khast3x/h8mail)
    - [IntelTechniques Breaches & Leaks](https://inteltechniques.com/tools/Breaches.html)
    - [IntelTechniques Pastes](https://inteltechniques.com/tools/Pastes.html#gsc.tab=0)

### STAGE 5: Dark Web
- Finally, in some cases there may be a need to touch the dark web, especially if the target potentially uses this environment for **unethical or illegal activities**. Most of the time, tapping into the rabbit holes of the dark web is unnecessary since 99% of the data resides on the **clear web**. This type of research is **mostly manual**, it's done through the **Tor network** and can expose the investigator to various **risks** if proper security measures are not implemented.
- Most common Dark Web OSINT **tools** include:
    - [Tor Browser](https://www.torproject.org/download/)
    - [Onion Search](https://github.com/megadose/OnionSearch)
    - [Midnight Sea](https://github.com/RicYaben/midnight_sea)
    - [Darkus](https://github.com/Lucksi/Darkus)
    - [TorBot](https://github.com/DedSecInside)

## OFM Updates
- The **OFM may get updated over time** due to a rapidly-changing online landscape and the emergence of more sophisticated tools.
- Tools, websites or services that are not **actively maintained** (2yrs+) will be gradually removed and new ones will be added.

## Disclaimers
- In the context of this methodology, OSINT refers to **passive, non-intrusive** open-source intelligence.
- Tool mentions are **not** endorsements. I am in **no way** affiliated with any of these tools.
- Keep in mind that **any illegal or unethical use of this information is solely your responsibility**.
