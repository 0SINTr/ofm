# OSINT Funnel Methodology
**OFM - Methodology for OSINT Investigations**

[![Stable Release](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/0SINTr/ofm/releases/tag/v1.0.0)
[![Last Commit](https://img.shields.io/github/last-commit/0SINTr/ofm)](https://github.com/0SINTr/ofm/commits/main)

**OSINT Funnel Methodology** for creating a coherent data collection workflow in investigations.

![ofm](img/ofm.png)

## Goal
The main goal of OFM is to provide a clear path for performing the **Data Collection** phase of an OSINT investigation, so that enough and diverse data can be passed further to the **Data Process & Analysis** phases. With hundreds of websites, services and CLI tools available, conducting a coherent research may be overwhelming. For this reason, the OSINT-er should have a clear, easy-to-follow plan for collecting data in an organized manner.

**Important!**
- This methodology refers to passive, non-intrusive OSINT tasks.
- The mentioned tools are just examples, not an exhaustive list.
- The OFM methodology only addresses the Data Collection phase.
- The OFM best fits OSINT investigations related to individuals.

## Steps
**OFM** is meant to be followed in a **top-down approach**, starting with the widest types and methods of searching for data, and gradually implementing increasingly specialized tools and techniques. In the end, all the collected data is funneled into the **Data Process & Analysis** phase.

### Search engines
- This step may sometimes collect the most amount of data, although this data may be quite scattered and raw in the absence of any kind of automation. The tools used in this step are the most well-known search engines such as **Google**, **Bing**, **Yandex**, **Yahoo** and **DuckDuckGo**.
- For each search engine, **manual** or **automated** (API-based) **advanced search and scrape** methods can be applied to filter the results via built-in operators or patterns, and organize the data in structured formats e.g. **JSON**.

### Specialized tools
- After the first wave of (more or less) relevant data has been collected and filtered from search engines, the next step is to use **specialized OSINT tools** (find some examples in the diagram) on the most relevant bits of data that are available regarding the target (usernames, email addresses, phone numbers, names or nicknames etc.).
- These tools are meant to further filter and narrow the search, however they can also provide new insights and leads on the target's online presence. Combining these tools with the advanced searches from the previous step may already build a significant portion of the target's **digital footprint**.

### Social avenues
- The information collected in the previous two steps may point to one or more **social media profiles** that the target is using. These profiles may include, but not be limited to, well-known social media services - **Facebook**, **Instagram**, **TikTok**, **X** or **Reddit**, secondary or emerging social networks such as **Bluesky** or **Truth Social**, blogs, forums, or chat rooms such as **Telegram**, **Discord**, **Slack** etc.
- Any of these avenues can lead to discovering more information about the target, either **personal** (age, birthday, photos, workplace, locations, friends) or **ideological** such as political, cultural, religious or sexual preferences, among others. Any such lead can further unravel a suite of pathways to explore, and can also help paint a better picture of the target. This research is **mostly manual**.

### Data breaches
- Websites and APIs providing information and search capabilities on **data breaches and pastes** can sometimes prove to be extremely rewarding, especially if the previous steps have not provided a great deal of data about the target. Finding breaches that the target's username or email address has been a part of can provide crucial clues on some of the platforms where the target has (or at least had) accounts or profiles. Furthermore, this type of searches can easily be **automated** via Python scripts and libraries, at very low API costs. Of course, this can again lead to manual research once one or more pieces of data have been found.
- Typical tools in this step are **HaveIBeenPwned**, **Dehashed**, **Snusbase**, **LeakCheck**, **Pastebin**, **IntelX** etc.

### Dark web
- Finally, in some cases there may be a need to touch the dark web, especially if the target potentially uses this environment for **unethical or illegal activities**. Most of the time, tapping into the rabbit holes of the dark web is unnecessary since 99% of the data resides on the **clear web**. This type of research is **mostly manual**, it's done through the **Tor browser** and can expose the investigator to various **risks** if proper security measures are not implemented.

## Final considerations
- The **OFM may get updated in time** due to a rapidly-changing online landscape and the emergence of more sophisticated tools.
- In the context of this methodology, OSINT refers to **passive, non-intrusive** open-source intelligence tasks.
- **Any illegal or unethical use of this information is solely your responsibility**.
