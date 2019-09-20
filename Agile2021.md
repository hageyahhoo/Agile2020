
# Implementing Test Automation with Experiments（仮）



## Abstract
LINE株式会社では、テスト自動化に関するアイデアが錯綜している。
そのためにSETとして活動している。
全社で使えるガイドラインやreference implementationが必要と、役員らとの話し合いで合意した。
そこで、LINE Shopで始めてみたよ。
<br />
<br />
<br />



## 1. INTRODUCTION

Challenges:
- Increasing outages at/between Microservices
- Struggling with testing [Microservices](https://martinfowler.com/articles/microservices.html)
    - Build quality inが出来ていない
    - Hard to test Microservices!
    - There are little knowledge/patterns for testing Microservices.
- 資料などは提示していたが、いまいち実践にたどり着かない
- 仮にテストを実装できても、自力でプロセス改善できるようにしなければダメ
<br />
<br />
<br />



## 2. START SMALL WITH DESIGN SPRINT
Using [Design Sprint](https://www.thesprintbook.com/)
- Start small
- Experiment every week

- First Round : 2019/07/24
    - Demonstrated test scripts for API with Karate
    - Karateを利用している人はいるが一人だけ。メンバーへの事前共有もなく、納得感がないことがわかった
    - 次の1週間で、JUnit, Kotlin Test, REST Assured, Karateのテストサンプルを作って比較することに
        - 2-3日のアクションですぐにフィードバックを得られるため、作り過ぎてからのやり直しで心が折れる自体は回避

- Second Round : 2019/07/31
    - Compared JUnit, REST Assured, Kotlin Test, and Karate.
        - Decided to use
            - REST Assured for testing RESTful APIs
            - JUnit for testing Thrift APIs

- Third Round : 2019/08/08
    - Implement UT/IT/E2E for interacting database
        - Use them as rules/guidelines for implementing tests
        - Trying to evaluate `Testcontainers` for later `Testable Infrastructure`
    -> Found that they're struggling with `slow test problem` (via working example)
        - Our ideas were accepted!

- 2019/08/15
    - Increase test scripts and solve slow test problem
    - Use Parameterized Test with JUnit5
    - ⭐️Switch (1) Proposal with working example (2) Implement with developers weekly

- 2019/08/22
    - Improved slow test problem dramatically by utilizing Testcontainers and running tests parallel.

- 2019/08/29
    - Applied Testcontainers about 50% only one day!
    - CI Server is facing with performance problem.
        -> Started modifying codes as Mob-Programming style.
        - 66 min -> 41 min

- 2019/09/04
    - Agreed with all members to expand Testcontainers
    - Some members started to improve Jenkins jobs and fell into confusion
        - Try to solve all found problems at once and failed
        - Unclear explanations
        -> We started to help them to divide tasks into smaller ones + report quickly
    - Zarubin-san became a good facilitator & leader
    - Started becoming a self-organized team
        - It means our tasks are decreasing dramatically -> More ScrumMaster-like approach

- 2019/09/11
    - Solved compilation overheads
    - Changed all embed mongo to Testcontainers
    - Next: Apply Testcontainers to Redis and MySQL

- 2019/09/19
    - Members requested to know current status & differences of UT/IT/E2E to improve
<br />
<br />
<br />



## 3. EXPAND SCOPE
- Database
- Call APIs provided by other teams
- Call APIs provided by other organizations
- E2E Testing
- Cover all test environments
- Chaos Engineering
<br />
<br />
<br />



## 4. GROW MEMBERS

### Developers
- Do it theirselves
- Adopt to Agile methodologies

### SET members
- チームとしてのスキルアップ＆現場感の構築・共有



## 5. LESSONS LEARNED
- 若手・中堅のエンジニアはなぜか「ガイドラインを提供して欲しい」「完璧なアイデアを最初から欲しい」と求めがちだが、そんなの無理
- 実体験を積ませ、自分たちで納得してもらわないと、方法論は定着しない
- 小さな実験（Design Sprint）は役立つ
- 育成・アイデアの実験・会社としてのミッション達成は、まとめて実現可能
<br />
<br />
<br />



## 6. WHAT'S NEXT?
- 育成・アイデアの実験・会社としてのミッション達成は、まとめて実現可能
    - そのための方法論・デザインを整理・一般化することが、今後の課題になるだろう。
<br />
<br />
<br />



## 7. CONCLUSIONS
考え中。。。
<br />
<br />
<br />



## REFERENCES
- [Design Sprint](https://www.thesprintbook.com/)
- [Luci] Lucian, Chris, “Growing the Mob” Agile 2017 Conference, Orlando, Florida
    - https://www.agilealliance.org/wp-content/uploads/2017/02/GrowingTheMob.pdf
- [Luci] Lucian, Chris, "Learning to Experiment" Agile 2018 Conference, San Diego, California
    - https://www.agilealliance.org/wp-content/uploads/2018/02/C.Lucian.-Learning-to-Experiment.pdf
- [Ito] Ito, Hiroyuki, "Technology-Driven Development: Using Automation and Development Techniques to Grow an Agile Culture" Agile 2014 Conference, Orlando, Florida
    - https://www.agilealliance.org/wp-content/uploads/2015/12/ExperienceReport.2014.Ito_.pdf
<br />
<br />
<br />
