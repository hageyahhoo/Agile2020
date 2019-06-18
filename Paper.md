
# Growing and Expanding Transformational Leaders Team (with Experiments)



## Abstract
Since I joined LINE Corporation as the first member of [SET (Software Engineer in Test)](---) in 2017,
we have been solving a variety of software and organizational problems.

Through these achievements, we have been adjusting our responsibilities
from software quality to software delivery, profitability, and organizational processes.

This report is about why and how we are becoming a team of [Transformational Leaders](https://en.wikipedia.org/wiki/Transformational_leadership) that is responsible for software delivery performance and organizational culture based on experiments.
<br />
<br />
<br />



## 1. INTRODUCTION
`LINE` is a free chatting and telecommunication service for smartphones that has released since **2012**. Our company name is derived from this service.

After the first release, LINE has been increasing users and messages transferred rapidly and globally. Especially, high sound quality with free, and the `sticker` feature that we can send a variety of rich emoticons as a message attracted a lot of users.

For adapting to the rapid growth of LINE, we have been improving LINE's architectures and code base iteratively. We chose [Microservice Architecture](https://martinfowler.com/articles/microservices.html) to earn scaling out, independent development, and fast delivery capabilities.

**However, outages of LINE have also been increasing.** Features, especially `fintech` ones like payments and banking, have been increasing dramatically. Troubles at `Integration Points` among each Microservices have also been increasing. They mean increases of negative monetary impacts to LINE users.

For reducing outages and improving product development processes,
LINE Corporation decided to open new positions for a Scrum Master, a DevOps engineer, and an SET.
<br />
<br />
<br />



## 2. BACKGROUND, CHALLENGES, DETAILS
⭐️初期から今まで続く課題を整理する
- Struggling with testing [Microservices](https://martinfowler.com/articles/microservices.html)
- Solving problems beyond "silos"



- Increasing outages at/between Microservices
    * Build quality inが出来ていない
    * Hard to test Microservices!
    * There are little knowledge/patterns for testing Microservices.

- Shortage of knowledge for problem-solving

- SET’s mission was vague
    * Continuous Decision Making
- Troubles in Testing
    * Testers/QAs do only UI testing. -> 協力しあっても役に立たなくね？
    * Hard to identify the points to collaborate with developers.
- Poor organization?
    * ミーティングや情報共有が下手など
    * 組織横断の課題解決を出来る人が少ない
<br />
<br />
<br />



## 3. EXPERIMENTS, SUCCESS AND FAILURES

### Approaches
* Increasing outages at/between Microservices
    * Work with Developers
        * Guide Developer Testing
        * Build Quality In
        * 実際にメンバーと一緒に痛い目に合わないと、本当の意味での協力関係は築けない
    * Tools/Solutions
        * Failure Detection
            * Spring Boot -> Karate
        * Performance Testing
            * Gatling -> Ayaperf (in-house framework/tool)
* Shortage of knowledge for problem-solving
    * Learning Session -> Review
        * 引き継ぎの前倒し
        * Tech/Process/Practiceをお互いに共有し合う
        * onboarding++
    * Sharing works among SET Team’s members
        * チームとしての課題解決力を増やす
        * Slackなどでの即時情報共有
        * ランチや雑談などでの常時状況共有・改善 -> Retrospective
* Poor organization?
    * Increase presence
        * Make presentations about our activities toward organizations
        - Impact Meeting
            - [Four Questions to Fix Low Attendance at Your Sprint Reviews](https://www.mountaingoatsoftware.com/blog/four-questions-to-fix-low-attendance-at-your-sprint-reviews)
    * Milestones as the pointer of conversation
        * User Storyと同じ
        * Mike Cohnさんのブログとのリンクが欲しい
        * 他チームとの交渉材料＆decision makingの武器となる
            * 実例：KR-JP SET Sync
    * 組織論と評価制度
        * https://hageyahhoo.hatenablog.com/entry/2019/05/27/215334
* 判断基準としてのFour Key Metrics
    * Sales/Profit/Employee Satisfaction
    * Profit/Productivity/Market Share
<br />
<br />
<br />



## 5. Lessons Learned
- Beyond Quality Assurance
    - Software Delivery (Performance)
    - Organizational Performance/Culture

- Need to learn a lot
- Expansion
<br />
<br />
<br />



## 6. Next Challenge
* Testable Infrastructure
    * Production-like test environment (with k8s and Containers)
    * Immutable Test Infrastructure (with k8s and Containers)
        * Reduce barriers of testing
    * Container as Mock/Test Harnesses
        * Make testing easier
<br />
<br />
<br />



## 7. Conclusions
<br />
<br />
<br />



## Points
* Solution Platformer -> Transformational Leader Team
    * Work with Developersの比率：縦80%、横20%
        * 縦：施策の効果は早いが、そのサービスに取り込まれて全体的視点を失う恐れもあり
        * 横：具体的施策まで踏み込めない恐れはあるが、全体的視点では動きやすい
    * 究極は、CTOチームとして、DXの改善＆ビジネス価値の提供を実現する
    * "WOW DX”!
* コンサル型ではなく、実際のツール・開発で実践して価値を出し続ける事が肝要ではないか？
    * Scrum@Scale



## Memo（あとでどこかに入れてみる）

（後付けでも）テストスクリプトを書くこと
* 効能
    * 書くことで、コードを理解しやすくなる
        * 読むだけでは、間違いがいくらでも起こり得る（true/falseとか!とか）
    * 動かして確認できるため、安心感を得られる
        * 特定のメソッドを動かすための前提条件（fixtureやメソッド事前呼び出しなど）が分かる
        * ステートレスであれば、失敗しても問題ない
    * 後日プログラムを修正する際の開始点にできる
    * ＼心理的安全性！／
    * テストスクリプトは、コミュニケーションの道具でもある
* Smells
    * これを「TDDに反するから意味がない」という人がいれば、他者を理解する意欲・スキルのない人と判断できる


"Feature Team” だけで十分か？（特に組織論）
* MSAの適用範囲拡大と、そこへの課題認識
    * お互いへの無関心の拡大
    * Microservice自体の技術的難易度の増大
        * テクハラの増加
    * 全体像の把握・全体最適の発想の欠如
* 解決方針
    * Feature Teams を繋げる “Control Plane"
        * 「全体を繋げる場」として扱い、硬直的な上位下達とはしない
    * I/Fの共通化
        * 全体として動くのに必要な情報を共通化し集約する
        * Commensurate: 共通のものさし
        * 全ての詳細な情報把握は無理
    * Feature Team らの自発性を、１つの全体として集約する
* 結論（候補）
    * 個々の技術を追う人間と、全体から「次のアクション」を考えリードする人間とに二分化される
    * 全体を追うという意味でのpracticeを確立していく必要性
    * 「技術で他者を責める」から、「他者を繋いでいく」方向を！



## Misc.
* SET as a LEAN LEADER, communication driver, and Product refiner?
    * Make Product Development Lean with Testing & Test Automation
        * Eliminate Waste
        * Eliminate meetings by reducing adjustment & non-productive communication
    * Adjustment : By automated test
        * SET's main activity is communication
        * Using test scripts is good.
        * Create, show, share vision to proceed with collaboration
        * Many developers and managers are not understanding testing properly.
        * Communication! Communication! Communication!
        * Make friends each other
* 技術は必須、しかし技術によりすぎてもダメ。
    * Necessary to implement product & test properly (to make awesome)
    * Only technology does not solve all issues
    * Use technology as a communication driver is good.
* Gather information from Gemma & know more about each test
    * Know the real problem
    * Based on Test Automation
    * Make product better
    * Developer/Manager が目的・メリットを理解し共感できる程度の詳細さでレポートしよう。
        * Context が不足していることは理解している。それを埋めるためにコミュニケーションを取るための道具として使おう。
* 2017/10/23 (Mon)
    * 技術力はあっても、課題の言語化とその解決方法に目が行かない人ばかり。
        * SET/Agile は、その点で価値がある/価値を示す必要がある。
    * ベンチャーであれば、Technical Excellence のみで乗り切れる部分もあるが、expansion/ongoing では無理がある。
        * 仕組みを作り、それを広める。
        * 課題発見・解決能力を持ち、施策をチームの隔てなくリードする人間が必須。
    * 技術的側面から切り込む必要があるので、技術力も必須。
    * 「SET」という単語にはローカル性がある。
        * Google の SET は、結果としてあの定義になっている。
* Quality Assuranceからの脱却
    * 「品質」→ビジネス価値の向上・ビジネス損失の削減・DXの向上
    * Next Engineering Management
        * 簡潔な説明：エレベーターピッチ・User Story
        * 継続的なインパクト：DX強化？

- persuing "WOW DX" (= Great Developer eXperience for LINERS).
<br />
<br />
<br />



## REFERENCES
- ["Release It!, 2nd Edition: Design and Deploy Production-Ready Software"](http://shop.oreilly.com/product/9781680502398.do%0A) by Michael Nygard
- ["ACCELERATE: The Science of Lean Software and DevOps: Building and Scaling High Performing Technology Organizations"](https://itrevolution.com/book/accelerate/) by Nicole Forsgren, Jez Humble, and Gene Kim
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
