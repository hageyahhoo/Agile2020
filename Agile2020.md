# Growing and Expanding Transformational Leaders Team with Experiments



## Abstract
Since I joined LINE Corporation as the first member of `SET (Software Engineer in Test)` in 2017, we have been solving a variety of software and organizational problems.

Through these achievements, we have been adjusting our responsibilities from software quality to software delivery, profitability, and organizational processes.

This report is about why and how we are becoming a team of [Transformational Leaders](https://en.wikipedia.org/wiki/Transformational_leadership) that is responsible for `software delivery performance and organizational culture` (*) based on experiments.
<br />
<br />
<br />



## 1. INTRODUCTION
`LINE` is a free chatting and telecommunication service for smartphones that has released since 2011. Our company name is derived from this service.

After the first release, LINE Corporation has been increasing users and messages transferred rapidly and globally. Especially, high sound quality with free, and the "sticker" feature that we can send a variety of rich emoticons as a message attracted a lot of users.

For adapting to the rapid growth of LINE, we have been improving LINE's architectures and code base iteratively. We chose [Microservice Architecture](https://martinfowler.com/articles/microservices.html) to earn scaling out, independent development, and fast delivery capabilities.

**However, outages of LINE have also been increasing.** Features, especially fintech ones like payments and banking, have been increasing dramatically. Troubles at `Integration Points` (*) among each Microservices have also been increasing. They mean increases of negative monetary impacts to LINE users.

For reducing outages and improving product development processes, LINE Corporation decided to open new positions for a Scrum Master, a DevOps engineer, and an SET.
I joined LINE Corporation as the first member of SET in 2017.
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

Next, I focused on analyzing "outage reports". "Outage reports" mean both postmortem meetings and published reports. They are a treasure-trove of information we need to solve. I was able to know causes of outages, impact on sales and profits, and problematic products through those reports. I understood that public APIs provided for external users was the most problematic product. Additionally, I found that reducing MTTR (Mean Time to Repair) would be an impactful solution as the first step.

Moreover, I talked stakeholders like developers, QA persons, product managers, senior managers, and executives to hear their concerns and troubles directly and beyond silos. Stakeholders' worries are also a treasure-trove of information to improve. Through those conversations, I understood that they had lots of non-verbalized problems. I also learned that verbalizing problems through direct and honest conversations
is critical for discovering real needs, shared understanding, and collaborations beyond silos.
<br />

⭐️TODO
#### 2. ESTABLISH SOLUTIONS WITH ITERATIVE CONSENSUS
After the first information gathering, I built the first version of rough solutions and proposed them to decision makers like senior managers and executives.

I didn't think that I can build the perfect solutions and agree with decision makers.
I decided to iterate build, propose, learn cycle quickly
to clarify objective, missions, and responsibilities of SET and agree on them with decision makers. I utilized `Iterative and Incremental consensus` approach at that time.

- Solutions
I decided target products based on frequency of outages and impact on users, sales and profit.
Prioritized
- public APIs provided for external users
- Sticker Shop
- Core Microservices

Aim to make failure detection faster and reduce MTTR by utilizing Test Automation


- Establish proposals and solutions to solve above needs
    - Iterative consensus on above ones with managers/executive
    - Re-examine solutions constantly and iteratively

- Iterative and Incremental consensus
    - Propose ideas and get feedback weekly
    - Discover proper solutions gradually
    - Achieve a consensus on solutions step by step
    - Re-examine solutions constantly

- Lead decision making by proposing rough milestones
- All decision makers have agile mindsets
    - Didn't require fixed schedules

Finally, we agreed on the first solution and milestone within 45 days I joined LINE Corporation.
<br />

#### 3. PROVIDE RESULTS EVERY WEEK FOR GIVING IMPACTS
- `Give impacts constantly`
    - Achieve something every week and share them with coworkers and decision makers
    - Show results quantitatively
    - Beyond silos

- `3 KPIs`: Sales, Profit, and Employee Satisfaction
    - Developer/Manager が目的・メリットを理解し共感できる程度の詳細さでレポートしよう。
<br />
<br />


### RETROSPECTIVE
- Show results from business perspective, not only from technical one
- `3 KPIs`: Sales, Profit, and Employee Satisfaction
    - Developer/Manager が目的・メリットを理解し共感できる程度の詳細さでレポートしよう。
- Troubles in Testing
    - Testers/QAs do only UI testing. -> 協力しあっても役に立たなくね？
    - Hard to identify the points to collaborate with developers.
- 一方で、人が足りないと、やりたいこともできないと痛感。
    - そこで採用を増やし、一緒に働ける人を見つけた
    - ⭐️ここを書きすぎると、本筋から逸れそう
<br />
<br />
<br />



## 3. SHIFT VERTICALLY
⭐️現場から学ぶことで、深い課題解決にたどり着いたという気づきを説明する

### CHALLENGES
SETへの関心は持ってもらえた、施策も少しずつ始めたが、施策の幅と深さが足りない
- Increasing outages at/between Microservices
- Struggling with testing [Microservices](https://martinfowler.com/articles/microservices.html)
    - Build quality inが出来ていない
    - Hard to test Microservices!
    - There are little knowledge/patterns for testing Microservices.
- 資料などは提示していたが、いまいち実践にたどり着かない
- 仮にテストを実装できても、自力でプロセス改善できるようにしなければダメ
<br />
<br />


### ACTIONS
- Work with `Product Development Team`/Frontline/現場に立つ
    - Guide Developer Testing for `Build Quality In`
    - 実際にメンバーと一緒に痛い目に合わないと、本当の意味での協力関係は築けない
    - 比率：縦80%、横20%
        - 縦：施策の効果は早いが、そのサービスに取り込まれて全体的視点を失う恐れもあり
        - 横：具体的施策まで踏み込めない恐れはあるが、全体的視点では動きやすい

- Implement Test Automation and related techniques based on product development teams' (unclear) needs
    - Failure Detection
        - Spring Boot -> [Karate](https://github.com/intuit/karate)
    - Performance Testing
        - Gatling -> `Ayaperf` (in-house framework/tool)

- Improve product development process
    - Clarify milestones/plans
    - Implement self-running style
<br />
<br />


### RETROSPECTIVE
- 一緒に痛い目に合うことから、本当のソリューションは見つけられる。
- コンサル型ではなく、実際のツール・開発で実践して価値を出し続ける事が肝要ではないか？
    - Scrum@Scale
- 発信不足で、価値があることが広く伝わっていかなったが、これを徐々に改善中。
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

- 各チームが目標・戦略・計画を提示できない
    - 各チームが何をやっていて、どこを目指すのかの情報が不足して、シニアマネージャー・役員が困るという状況が発生
    - タイムリーな報告ができない

- 新メンバーの増加＋役割の増加（プロセス改善）
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
