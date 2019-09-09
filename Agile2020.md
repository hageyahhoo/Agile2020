# Growing and Expanding Transformational Leaders Team with Experiments



## Abstract
Since I joined LINE Corporation as the first member of `SET (Software Engineer in Test)` in 2017, we have been solving a variety of software and organizational problems.

Through these achievements, we have been adjusting our responsibilities from software quality to software delivery, profitability, and organizational processes.

This report is about why and how we are becoming a team of [Transformational Leaders](https://en.wikipedia.org/wiki/Transformational_leadership) that is responsible for `software delivery performance and organizational culture` (*) based on experiments.
<br />
<br />
<br />
⭐️Service/Productの表記揺れをチェック<br />
⭐️なぜ・どうやって・どういう成果が出たかを意識して書き続ける<br />
<br />



## 1. INTRODUCTION
`LINE` is a free chatting and telecommunication service for smartphones that has released since 2011. Our company name is derived from this service.

After the first release, LINE Corporation has been increasing users and messages transferred rapidly and globally. Especially, high sound quality with free, and the "sticker" feature that we can send a variety of rich emoticons as a message attracted a lot of users.

For adapting to the rapid growth of LINE, we have been improving LINE's architectures and code base iteratively. We chose [Microservice Architecture](https://martinfowler.com/articles/microservices.html) to earn scaling out, independent development, and fast delivery capabilities.

**However, outages of LINE have also been increasing.** Features, especially fintech ones like payments and banking, have been increasing dramatically. Troubles at `Integration Points` (*) among each Microservices have also been increasing. They mean increases of negative monetary impacts to LINE users.

For reducing outages and improving product development processes, LINE Corporation decided to open new positions for a Scrum Master, a DevOps engineer, and an SET. I joined LINE Corporation as the first member of SET in 2017.
<br />
<br />
<br />



## 2. CLARIFY DEMANDS AND RESPONSIBILITIES TO START

### CHALLENGES
When I joined LINE Corporation, there were lots of problems which relate to not only software quality but a variety of software and organizational problems.

The biggest challenge was the confusions and disagreements about SET among stakeholders. There were no clear objective, missions, and responsibilities of SET. Additionally, there were no shared understanding about SET. Therefore, I needed to clarify them at first.

Other big challenge was that I was a newbie of LINE Corporation and I didn't have enough knowledge of our services, architectures, technologies used, and so on.

Moreover, there were few leaders to solve problems which affect more than one team and/or service. In other words, few leaders could act beyond silos. We have been widely adopting to Microservice Architecture. It was critical to overcome this problem for solving outages quickly and properly with less impacts to users.
<br />
<br />


### ACTIONS
For the smooth start of SET activities, I did the following actions.

#### 1. GATHER INFORMATION WITH PRODUCT DISCOVERY
To clarify objective, missions, and responsibilities of SET, I utilized the idea of [Product Discovery](http://productdiscoverycanvas.com/tag/david-hussman/) taught by [David Hussman](https://twitter.com/davidhussman) for gathering necessary information.

At first, I analyzed our services and products. I utilized static code analysis tool named [SonarQube](https://www.sonarqube.org/) to know the code coverage and technical debts for each service. I also added simple unit and integration test scripts to know behaviors of the products. Test scripts are good for understanding software under test (*).

Next, I focused on analyzing "outage reports". "Outage reports" mean both postmortem meetings and published reports. They are a treasure-trove of information we need to solve. I was able to know causes of outages, impact on sales and profits, and problematic products through those reports. I understood that public APIs provided for external users, and `Sticker Shop` were the most problematic products. Additionally, I found that reducing MTTR (Mean Time to Repair) would be an impactful solution as the first step.

Moreover, I talked stakeholders like developers, QA persons, product managers, senior managers, and executives to hear their concerns and troubles directly and beyond silos. Stakeholders' worries are also a treasure-trove of information to improve. Through those conversations, I understood that they had lots of non-verbalized problems. I also learned that verbalizing problems through direct and honest conversations is critical for discovering real needs, shared understanding, and collaborations beyond silos.
<br />

#### 2. ESTABLISH SOLUTIONS WITH ITERATIVE AND INCREMENTAL CONSENSUS
At the end of the first week I joined LINE Corporation, I built the first rough ideas of SET including objective, missions, responsibilities, solutions, and milestones based on gathered information I mentioned above. Additionally, I proposed them to "decision makers" like senior managers and executives.

I didn't think that I can build the perfect solutions and agree on them with decision makers at once. I supposed that it would be preferable not only me but decision makers to continue proposing ideas, getting feedbacks, and improving proposal. Additionally, there were few persons who could lead `strategy formulation` in LINE Corporation at that time. Leading decision making gave impacts to decision makers and it was good for attracting their interests in SET. Therefore, I chose to iterate build-propose-learn cycle weekly as `Iterative and Incremental Consensus` approach.

My first proposal was focusing on improving `Sticker Shop` due to frequency of outages, however I didn't define milestones. Through this approach, rough milestones were enough useful for decision makers to understand tasks, plan, and due date easily and quickly. Additionally, they also said that it was OK to update milestones if we knew additional information. Moreover, they taught me that `public APIs` were more important than `Sticker Shop` at that time from business perspective. On the other hand, they agreed on my idea that utilizing Test Automation for making failure detection faster and reducing MTTR was valuable as SET's responsibility. Through this approach, I could improve my proposal step by step. Finally, we agreed on the first solution and milestone within 45 days since I joined LINE Corporation.
<br />

#### 3. MANAGING IMPACTS BY PROVIDING RESULTS EVERY WEEK
In parallel with `Iterative and Incremental Consensus`, I tried to `manage impacts` (*) constantly to coworkers and decision makers for attracting their interests in SET.

From the first week I joined LINE Corporation, I achieved something every week and shared them with coworkers and decision makers. Especially, I shared working software or executable one. Additionally, I showed results quantitatively beyond silos.

Here is a list of achievements for my first 10 weeks.

| Week    | Achievements                                                     |
| ------- | ---------------------------------------------------------------- |
| Week 1  | Started writing test scripts to understand services/products     |
| Week 2  | Proposed first idea of SET activities to decision makers         |
| Week 3  | Built mechanism to run and report static code analysis regularly |
| Week 4  | Shared to developers how to build static code analysis           |
| Week 5  | Proposed milestones of activities to decision makers             |
| Week 6  | Agreed with proposals/milestones with decision makers            |
| Week 7  | Collected information and tools of QA/Tests in one place         |
| Week 8  | Implemented failure detection for public APIs                    |
| Week 9  | Guided to start regular meetings with developers and QAs         |
| Week 10 | Started solving problems by developers step by step              |

When I had been managing impacts, I utilized `3 KPIs`; Sales, Profit, and Employee Satisfaction. When I had worked at Rakuten, one of senior executives and my supervisor had taught me that every business can measure with this 3 KPIs. After that, I have been utilizing it for all activities.

Here are examples. I chose all activities as SET for improving Sales and Profit. I implemented test scripts for reducing MTTR, not only for expanding test automation. Additionally, I picked up actions that could affect Employee Satisfaction. For decision makers, I focused on discovering and verbalizing their anxieties, and providing quantitative information. For Developers and QAs, I tried to stimulate appetites for learning.

As a result, many colleagues started talking about SET. Their interests in SET led collaboration with product development teams, QAs/Test Automators, and Product Managers. It meant I could lead problem-solving beyond silos. Additionally, decision makers started supporting SET activities positively. Quick agreement on the first solution and milestones of SET was a good sign.
<br />
<br />


### RETROSPECTIVE
The idea of `Product Discovery` worked for clarifying responsibilities and activities of SET. Additionally, `Iterative and Incremental Consensus` was useful for collaborating with decision makers and agreeing with them quickly. Moreover, `managing impacts with 3 KPIs` attracted lots of colleagues from business perspectives, not only from technical ones.
<br />
<br />
<br />



## 3. SHIFT VERTICALLY

### CHALLENGES
After clarifying responsibilities and activities of SET, getting decision makers' supports and colleagues' interests, I started actions as SET. Additionally, LINE hired new employees and formed a team of SET. I thought we could proceed our activities more quickly and widely. However, we faced with new obstacles.

At first, we implemented a failure detection system for `public APIs`, however, it didn't become established in the product development team. We implemented test scripts for these APIs, called them via CI servers periodically, and notified errors and failures to the product development team quickly. We utilized Test Automation and CI as a failure detection system. We also used the common technologies like JUnit, Spring Boot, Jenkins, and so on for the product development team. Failure detection worked partially and some developers started implementing them. Although, test scripts written in JUnit were hard to read, implement, and maintain for the Product Manager and most of developers. Additionally, SET team and the product development team have been working at different offices. Our communications weren't sufficient to proceed improvements.

Other obstacle was that performance problems at `Sticker Shop` had emerged. They had been using one in-house performance testing tool. However, it couldn't provide enough capabilities to detect emerging issues. Moreover, they need to write test scripts with groovy, an unaccustomed programming language for them. Therefore, writing test scripts was not fast and effective.

Another challenge was that consulting-style approach didn't work. We often provided guidelines, ideas how to design good test scenarios, and test script examples widely. However, most of colleagues didn't utilize them to improve their testing problems. We needed to find ways to expand ideas and to improve their work more effectively.
<br />
<br />


### ACTIONS
For achieving our mission, we started working with product development teams deeply to improve their processes. In other words, we started to work, learn, and solve essential problems with them.
<br />

#### 1. REFINE FAILURE DETECTION SYSTEM WITH KARATE
For `public APIs`, we started direct conversations with the product development team members to discover their real needs and concerns at first. In other words, we did `Product Discovery` approach again. We talked daily via video conference system. We discussed with the Product Manager if he came to our office.

Through these discussions, we found that test scripts written in JUnit were hard for them. Therefore, we investigated and proposed lots of testing tools to them.

Finally, we chose [Karate](https://github.com/intuit/karate) framework. It provides features specific to API Testing with BDD (Behavior-Driven Development) style and Gherkin format. It was easy to read, implement, and maintain for both developers and the Product Manager. Especially, defining the preferable state was easy to understand for them.

After decision to use Karate framework, we SETs and the product development team members started to rewrite test scripts from JUnit to Karate collaboratively. SETs wrote examples at first. SETs guided `Developer Testing` to achieve and expand `Build Quality In` idea by working with developers. SETs supported solving architectural problems of Karate. After 3 months' collaborative work, finally failure detection system with Karate became established in this product development team.
<br />

#### 2. IMPLEMENT NEW PERFORMANCE TESTING TOOLS WITH KOTLIN
For `Sticker Shop`, we did the same approach as `public APIs` to discover their real needs and concerns at first.

We found that improving to use the existing in-house performance testing tool was impractical. It could produce only 10% of loads what we wanted to test. It was not easy to expand and/or modify features. Additionally, most of the product development team's members were familiar with Kotlin language. Implementing test scripts with Groovy was hard for them. Moreover, usage of [Docker](https://www.docker.com/) and [Kubernetes](https://kubernetes.io/) were expanding at that time in our company. We thought it was a good chance to utilize those new tools and approaches to improve our performance testing.

Therefore, we decided to create a new in-house performance testing tool named `Ayaperf`. Ayaperf is a Java wrapper of [Locust](https://locust.io/) that can use Kubernetes to increase loads easily with enough volume. Developers can write test scripts of performance testing with Java and Kotlin. We did iterative and incremental style to implement and improve Ayaperf with `Sticker Shop` developers. After 3 months' cowork, finally Ayaperf became stable. Developers started to detect performance issues with it before release. Additionally, they could correct issues by themselves without hurting production code. They found and solved 3 hidden performance issues by utilizing Ayaperf.
<br />

#### 3. IMPROVE PRODUCT DEVELOPMENT PROCESSES
⭐️
We can improve the process temporarily. But it tends to be a volatile?
If improvements don't continue, it means failure.

We did not only providing tools, but also improving product development processes for ach team.

```
Another challenge was that consulting-style approach didn't work. We often provided guidelines, ideas how to design good test scenarios, and test script examples widely. However, most of colleagues didn't utilize them to improve their testing problems. We needed to find ways to expand ideas and to improve their work more effectively.
```

After that, CGW clarified plans, milestones, and priorities by their own. Additionally, they could proceed improvements continuously without our help. They really becase the self-organized team.
<br />
<br />


### RETROSPECTIVE
We could solve essential problems and improve product development processes of each team by working with them deeply and collaboratively. Additionally, we learned a lot with them to improve our approaches.
- Implemented Test Automation and related techniques based on product development teams' (unclear) needs


The origin of the word "compassion" is "***"
- **compassion**（ラテン語で「共に苦しむ」→共感）
    - 実際にメンバーと一緒に痛い目に合わないと、本当の意味での協力関係は築けない
    - 一緒に痛い目に合うことから、本当のソリューションは見つけられる。
    - コンサル型ではなく、実際のツール・開発で実践して価値を出し続ける事が肝要ではないか？


- マネージャーは、プロダクションコードを変更するとチームの邪魔になりかねないが、テストコードならば邪魔せずにすむ
    - It's good to learn behavior of current products and teach members how to clarify requirements.
    - Guide Developer Testing for `Build Quality In`


On the other hand, we should keep the ratio
    - 縦80%、横20%
        - 縦：施策の効果は早いが、そのサービスに取り込まれて全体的視点を失う恐れもあり
        - 横：具体的施策まで踏み込めない恐れはあるが、全体的視点では動きやすい
<br />
<br />
<br />



## 4. BECOME TRANSFORMATIONAL LEADERS
⭐️純技術以外のあらゆるソリューションを適用する話＋組織改善へのシフト

### CHALLENGES
- 組織をまたぐ課題の解決がまだまだ不足
    - "Feature Team” だけで十分か？（特に組織論）
        - MSAの適用範囲拡大と、そこへの課題認識
            - お互いへの無関心の拡大
            - Microservice自体の技術的難易度の増大
                - テクハラの増加
            - 全体像の把握・全体最適の発想の欠如

Additionally, I also found that the idea of `Quality Assurance` narrowed our activities to improve services and products. The word `Test` was just a burden or a constraint for SET at that time.

- 各チームが目標・戦略・計画を提示できない
    - 各チームが何をやっていて、どこを目指すのかの情報が不足して、シニアマネージャー・役員が困るという状況が発生
    - タイムリーな報告ができない

- 新メンバーの増加＋役割の増加（プロセス改善）

- 発信不足で、価値があることが広く伝わっていかなったが、これを徐々に改善中。
- Build quality inが出来ていない
- Hard to test Microservices!
- There are little knowledge/patterns for testing Microservices.
<br />
<br />


### ACTIONS
- テスト自動化に限らない課題解決に、SETチームとして乗り出した
    - Clarify and share Mission and Milestone
        - Used them as the pointer of conversation (the same as User Story)
    - Improve meeting (Make Product Development Lean)
        - stop meeting that cannot provide any value
            - Mission & milestone worked for it
        - Eliminate meetings by reducing adjustment & non-productive communication
    - Increase presence of SET Team
        - Make presentations about our activities toward organizations (found opportunities)
        - Impact Meeting
            - [Four Questions to Fix Low Attendance at Your Sprint Reviews](https://www.mountaingoatsoftware.com/blog/four-questions-to-fix-low-attendance-at-your-sprint-reviews)

- テスト自動化を、コミュニケーションツールとして拡大利用する
    - Used examples of test scripts
        - Quick returns
        - Run them in front of members (= demo)
        - Run means repeatable & 安心感
            - Stateless or Immutable
    - Zipkin & Karate Reportの統合によるMTTR短縮（によって、マネジメントやビジネスに価値を提供する）
    - 技術的側面から切り込む必要があるので、技術力も必須。しかし技術によりすぎてもダメ。
        - Necessary to implement product & test properly (to make awesome)
        - Only technology does not solve all issues
        - Use technology as a communication driver is good.
        - 技術力はあっても、課題の言語化とその解決方法に目が行かない人ばかり。
            - SET/Agile は、その点で価値がある/価値を示す必要がある。
        - ベンチャーであれば、Technical Excellence のみで乗り切れる部分もあるが、expansion/ongoing では無理がある。
            - 仕組みを作り、それを広める。
            - 課題発見・解決能力を持ち、施策をチームの隔てなくリードする人間が必須。
    - **Resilience with Test Automation**
        - Detect and solve all bugs beforehand is impractical
        - Utilize Obervability with Test Automation

- Learning Session
    - 新メンバーの増加＋役割の増加（プロセス改善）
    - Shortage of knowledge for problem-solving
    - Learning Session
        - 引き継ぎの前倒し
        - Tech/Process/Practiceをお互いに共有し合う
        - onboarding++
    - Sharing works among SET Team’s members
        - チームとしての課題解決力を増やす
        - ランチや雑談などでの常時状況共有・改善 -> Retrospective
    - Experiments
        - Utilize failures as a source of learning
    - [組織論と評価制度](https://hageyahhoo.hatenablog.com/entry/2019/05/27/215334)
    - [Diffusion of Innovation](https://www.infoq.com/presentations/process-evolution-flat-structure/)

- 判断基準としてのFour Key Metrics
    - Sales/Profit/Employee Satisfaction
    - Profit/Productivity/Market Share
<br />
<br />


### RETROSPECTIVE
- Show results iteratively
    Especially to stakeholders
- Experience success with new ways
- Just guidelines and references didn't work
    - Need to work with members
- 人材・文化の変更
    - 個々の技術を追う人間と、全体から「次のアクション」を考えリードする人間とに二分化される
    - 全体を追うという意味でのpracticeを確立していく必要性
    - 「技術で他者を責める」から、「他者を繋いでいく」方向へシフトさせていく
<br />
<br />
<br />



## 5. LESSONS LEARNED
- Changing the difinition & responsibility of "SET"
    - Google由来のロールだが、「SET」という単語にはローカル性がある。
    - テスト自動化だけではなく、プロセス改善、全社のプラスになることの実施へと、やっていることを広げていっている。
- Beyond Quality Assurance
    - Software Delivery (Performance)
    - Organizational Performance/Culture
- Quality Assuranceからの脱却
    - 「品質」→ビジネス価値の向上・ビジネス損失の削減・DXの向上
    - Next Engineering Management
        - 簡潔な説明：エレベーターピッチ・User Story
        - 継続的なインパクト：DX強化？

- Team of Transformational Leaders
    - 究極は、CTOチームとして、DXの改善＆ビジネス価値の提供を実現する
    - "WOW DX”!
        - persuing "WOW DX" (= Great Developer eXperience for LINERS).
    - Need to learn a lot
    - Expansion
<br />
<br />
<br />



## 6. WHAT'S NEXT?
`Testable Infrastructure`
- Production-like test environment (with k8s and Containers)
- Immutable Test Infrastructure (with k8s and Containers)
    - Reduce barriers of testing
- Container as Mock/Test Harnesses
    - Make testing easier

We are investigating [Testcontainers](https://www.testcontainers.org/):
- [Immutable and disposable RDBMS for testing](https://www.testcontainers.org/modules/databases/)
- [E2E Testing with WebDriver](https://www.testcontainers.org/modules/webdriver_containers/)

- Design Sprint for Technical Problems
    - Agile2021で話す予定なので軽めに

- テクハラ
    - 「TDDに反するから意味がない」という人がいれば、他者を理解する意欲・スキルのない人と判断できる
<br />
<br />
<br />



## 7. CONCLUSIONS
- Changing the difinition & responsibility of "SET"
    - Google由来のロールだが、「SET」という単語にはローカル性がある。
    - テスト自動化だけではなく、プロセス改善、全社のプラスになることの実施へと、やっていることを広げていっている。
- Team of Transformational Leaders
    - 究極は、CTOチームとして、DXの改善＆ビジネス価値の提供を実現する
    - "WOW DX”!
        - persuing "WOW DX" (= Great Developer eXperience for LINERS).
    - コンサル型では機能しなかった。実際のツール・開発で実践して価値を出し続ける事が肝要ではないか？
    - Quality Assuranceからの脱却
<br />
<br />
<br />



## REFERENCES
- `software delivery performance and organizational culture`
    - ["ACCELERATE: The Science of Lean Software and DevOps: Building and Scaling High Performing Technology Organizations"](https://itrevolution.com/book/accelerate/) by Nicole Forsgren, Jez Humble, and Gene Kim
- `Integration Points`:
    - ["Release It!, 2nd Edition: Design and Deploy Production-Ready Software"](http://shop.oreilly.com/product/9781680502398.do%0A) by Michael Nygard
- `Test scripts are good for understanding software under test`
- `Give impacts constantly`:
    - ["How Google Tests Software"](https://www.amazon.com/dp/B007MQLMF2) by by James A. Whittaker, Jason Arbon, and Jeff Carollo
- [Sutherland] Sutherland, Jeff, "Scrum@Scale: An Interview with Agile Manifesto Co-Author and Scrum Co-Founder Jeff Sutherland" InfoQ
    - https://www.infoq.com/articles/sutherland-scrum/
- [Luci] Lucian, Chris, “Growing the Mob” Agile 2017 Conference, Orlando, Florida
    - https://www.agilealliance.org/wp-content/uploads/2017/02/GrowingTheMob.pdf
- [Luci] Lucian, Chris, "Learning to Experiment" Agile 2018 Conference, San Diego, California
    - https://www.agilealliance.org/wp-content/uploads/2018/02/C.Lucian.-Learning-to-Experiment.pdf
- [Ito] Ito, Hiroyuki, "Technology-Driven Development: Using Automation and Development Techniques to Grow an Agile Culture" Agile 2014 Conference, Orlando, Florida
    - https://www.agilealliance.org/wp-content/uploads/2015/12/ExperienceReport.2014.Ito_.pdf
<br />
<br />
<br />



# レビュアー向け補足
- Markdownでの見易さを考慮して、文ではなく意味の単位で改行しています。
    - 後日、Wordでリリース版を作成する際、これらの改行は削除します。
