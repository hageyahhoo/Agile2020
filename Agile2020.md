# Growing and Expanding Transformational Leaders Team with Experiments



## Abstract
Since I joined LINE Corporation as the first member of `SET (Software Engineer in Test)` in 2017, we have been solving a variety of software and organizational problems.

Through these achievements, we have been adjusting our responsibilities from software quality to software delivery, profitability, and organizational processes.

This report is about why and how we are becoming a team of [Transformational Leaders](https://en.wikipedia.org/wiki/Transformational_leadership) that is responsible for `software delivery performance and organizational culture` (*) based on experiments.
<br />
<br />
<br />
- ⭐️表記揺れチェック<br />
    - Service/Product<br />
    - Decision makers<br />
    - SET team (not SET Team)<br />
- ⭐️時制を念の為確認<br />
- ⭐️Iとweとを使い分けているがどうなんだべ？<br />
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

At first, I analyzed our services and products. I utilized static code analysis tool named [SonarQube](https://www.sonarqube.org/) to know the code coverage and technical debts for each service. I also added simple unit and integration test scripts to know behavior of the products. Test scripts are good for understanding software under test (*).

Next, I focused on analyzing "outage reports". "Outage reports" mean both postmortem meetings and published reports. They are a treasure-trove of information we need to solve. I was able to know causes of outages, impact on sales and profits, and problematic products through those reports. I understood that public APIs provided for external users, and `Sticker Shop` were the most problematic products. Additionally, I found that reducing MTTR (Mean Time to Repair) would be an impactful solution as the first step.

Moreover, I talked stakeholders like developers, QA persons, Product Managers, senior managers, and executives to hear their concerns and troubles directly and beyond silos. Stakeholders' worries are also a treasure-trove of information to improve. Through those conversations, I understood that they had lots of non-verbalized problems. I also learned that verbalizing problems through direct and honest conversations is critical for discovering real needs, shared understanding, and collaborations beyond silos.
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
For achieving our mission, we started working with product development teams deeply to improve their processes. In other words, we started working, learning, and solving essential problems with them.
<br />

#### 1. REFINE FAILURE DETECTION SYSTEM WITH KARATE
For `public APIs`, we started direct conversations with the product development team members to discover their real needs and concerns at first. In other words, we did `Product Discovery` approach again. We talked daily via video conference system. We discussed with the Product Manager if he came to our office.

Through these discussions, we found that test scripts written in JUnit were hard for them. Therefore, we investigated and proposed lots of testing tools to them.

Finally, we chose [Karate](https://github.com/intuit/karate) framework. It provides features specific to API Testing with BDD (Behavior-Driven Development) style and Gherkin format. It was easy to read, implement, and maintain for both developers and the Product Manager. Especially, defining the preferable state was easy to understand for them.

After decision to use Karate framework, we SETs and the product development team members started rewriting test scripts from JUnit to Karate collaboratively. SETs wrote examples at first. SETs guided `Developer Testing` to achieve and expand `Build Quality In` idea by working with developers. SETs supported solving architectural problems of Karate. After 3 months' collaborative work, finally failure detection system with Karate became established in this product development team.
<br />

#### 2. IMPLEMENT NEW PERFORMANCE TESTING TOOLS WITH KOTLIN
For `Sticker Shop`, we did the same approach as `public APIs` to discover their real needs and concerns at first.

We found that improving to use the existing in-house performance testing tool was impractical. It could produce only 10% of loads what we wanted to test. It was not easy to expand and/or modify features. Additionally, most of the product development team's members were familiar with Kotlin language. Implementing test scripts with Groovy was hard for them. Moreover, usage of [Docker](https://www.docker.com/) and [Kubernetes](https://kubernetes.io/) were expanding at that time in our company. We thought it was a good chance to utilize those new tools and approaches to improve our performance testing.

Therefore, we decided to create a new in-house performance testing tool named `Ayaperf`. Ayaperf is a Java wrapper of [Locust](https://locust.io/) that can use Kubernetes to increase loads easily with enough volume. Developers can write test scripts of performance testing with Java and Kotlin. We did iterative and incremental style to implement and improve Ayaperf with `Sticker Shop` developers. After 3 months' collaborative work, finally Ayaperf became stable. Developers started detecting performance issues with it before release. Additionally, they could correct issues by themselves without hurting production code. They found and solved 3 hidden performance issues by utilizing Ayaperf.
<br />

#### 3. IMPROVE PRODUCT DEVELOPMENT PROCESSES AS A HABIT
At `public APIs` and `Sticker Shop`, we found the effectiveness of working with product development teams to find their real needs and solve them. This approach worked well. However, I thought it was not enough and sufficient. I saw that lots of teams stopped solving problems by themselves after coaches left teams. It is a failure if improvements don't continue after coaches' left. Therefore, I expanded our activities to making product development process improvement as a habit especially at `public APIs`.

We had found and solved issues as homework every week. We had continued applying new Karate features and refactoring test scripts. Additionally, we had implemented a notification mechanism via slack to reduce MTTR. Moreover, we had asked product development team members for clarifying objectives, quantitative values they will provide to users, and rough milestones of each task every week. We utilized the idea of Scrum framework to make continuous improvement as a habit of the team. We had continued those activities for about 3 months.

After that, the product development team became able to clarify quarterly milestones, prioritize tasks based on business values, and improve test scripts and the failure detection system by their own. They started decreasing outages dramatically (⭐️定量情報が欲しい). They really became the self-organized team. Finally, we stopped supporting the team.
<br />
<br />


### RETROSPECTIVE
We could solve essential problems and improve processes of each product development team by working collaboratively and deeply with them. We SET and product development teams implemented Test Automation and related techniques based on the idea of `Product Discovery`. Additionally, each team becomes sophisticated. For example, the Product Manager of `public APIs` writes test scripts with Karate routinely. He often says that the Product Manager may disturb the team by writing production codes, but can contribute to the team by writing test scripts! He is utilizing test scripts to understand behavior of the product deeply, to clarify next actions and goals of the product and the team, and to guide team members doing `Developer Testing` for `Build Quality In`.

Additionally, we learned a lot of things to improve our approaches through working with them. The consulting-style approach is useful to keep the whole image of activities, however, we cannot approach essential problems. On the other hand, the working-together approach is effective to discover and solve essential problems quickly, but we may loose the whole image of activities because of too focusing on one product development team. Therefore, we should utilize both style based on the phase of activities.

The English word "compassion" derives from Latin's "compati", which means "suffer with". We think this is the point of leading and guiding new things like Agile. We SETs and product development teams had been suffering from the same problems by working together. We had considered solutions and solved problems one by one together. Those series of activities had constructed real collaborative relationships. Moreover, those relationships had become boosters for adapting to new Test Automation tools and process improvements.
<br />
<br />
<br />



## 4. BECOME TRANSFORMATIONAL LEADERS

### CHALLENGES
We had been solving a lot of technical and process issues of each product by working together with each product development team's members. Those activities and achievements have been recognized as huge successes by executives. However, those successes had led us SET team to the next level of challenges.

The first challenge was the company-wide strategic and management problems. A lot of product development teams could not show their own missions, goals, plans, and milestones to `decision makers` like senior managers and executives beforehand. Additionally, those teams couldn't share their current status and problems in a timely manner. `Decision makers` had been frustrating that they couldn't make decisions properly and precisely. On the other hand, we SET team had been showing that information timely from the beginning of all activities. Therefore, `decision makers` requested us SET team to teach product development teams to express that information properly.

The second challenge was about onboarding. In July 2019, our team had 4 members and we hired one recent graduate and one mid-career employee simultaneously as new SETs. To proceed our activities smoothly, we needed to make onboarding as the top priority task.

The third one was a doubt about testing and quality assurance. LINE Corporation hires Test Engineers and Quality Assurance Engineers. However, most of them had only been doing End-to-end testing manually via client applications. In the era of Microservices, I thought it is not practical to detect bugs and solve them beforehand with those activities. Additionally, most of them didn't care about deployment, release, and contribution of our business. They were just interested in doing their own tasks by developer's requests. Such behavior was not what we SET aimed to do. On the other hand, we named our role as "Software Engineer in Test". The word "Test" made our colleagues misunderstand that we SET were the same as Test Engineers and Quality Assurance Engineers. The notion of testing and quality assurance were just a burden and a constraint that narrowed our activities to improve services and products. Therefore, I thought we needed different approaches to change those assumptions drastically.
<br />
<br />


### ACTIONS
For solving those totally different challenges, we started lots of actions
including not only Test Automation and technical ones, but also engineering management, education, innovation, and so forth.
<br />

#### 1. LEAD ENGINEERING MANAGEMENT IMPROVEMENT
For solving the company-wide strategic and management problems, we had started showing our activities and installing our ways into other teams. In other words, we had started leading engineering management improvement based on decision makers' demands.

At first, we shared our milestones with other teams over and over again as an example of engineering management strategy and planning. Additionally, we held workshops for those teams to support their planning, defining mission, reporting, and so forth. For example, I held [the Drucker Exercise](https://agilewarrior.wordpress.com/2009/11/27/the-drucker-exercise/) and [the User Story Mapping](⭐️) workshops to one team for teaching the idea of product ownership. After those activities, some teams started defining their own milestones and sharing them to decision makers in a timely manner.

On the other hand, we attended other teams' meetings to improve. If the meeting was full of verbose and meaningless reporting without any decision making and productive communication, we proposed rules like reporting only necessary for decision making and applying timeboxing. We often utilized the idea of [Impact Meeting](https://www.mountaingoatsoftware.com/blog/four-questions-to-fix-low-attendance-at-your-sprint-reviews) by Mike Cohn. Moreover, we stopped some meetings that couldn't provide any value. Clarified mission and milestones were useful to distinguish whether the meeting was valuable or not. We could use clear mission and milestones as the pointer of conversation as the same as the User Story.
<br />

#### 2. LEARNING SESSION
For proceeding our onboarding smoothly, I decided to utilize the idea of "Learning Session". Learning Session is a way of study sessions during business hours taught by Chris Lucian at [Agile2017](https://www.agilealliance.org/wp-content/uploads/2017/02/GrowingTheMob.pdf).

Here are basic rules. We have been holding Learning Session basically for 30 to 60 minutes everyday during business hours as a work. We can choose any topics we assume it's necessary for our daily work. Anyone can speak and facilitate it with Mob Programming way with a fun and without criticism.

Through a series of Learning Sessions, we have been learning a wide variety of tools, techniques, process improvements, and so forth. We learned Karate framework. All team members can set up it, write test scripts, run tests, and teach them to other persons. We became accustomed to shortcut keys of IntelliJ IDEA, JIRA, and Confluence. We often review programs via GitHub's Pull Requests together. We refactor test scripts with learning test and architectural design techniques. We frequently demonstrate our work-in-progress tasks to get feedbacks quickly. Moreover, we experiment process improvements like Scrum, Kanban, the Drucker Exercise, and so on.

As a result, we smoothly finished onboarding for two newcomers. They could write programs, pass reviews, and deploy their programs within 3 days. They could adapt to our team's rules and culture, like demonstrating their results to users very frequently for getting fast feedbacks, focusing on release, and experimental work style, very quickly. They became contributing to our products and services within 1 or 2 months.

Moreover, we found that Learning Session gave 3 additional impacts to our team.

The first impact was the growth of our team, not only of newcomers. We often shared each work among team members. We frequently solved each member's problem together. As a result, all team members could substitute other's works. We can say we have been doing "handover" everyday. We could increase the "truck number" coined by Jim Coplien and enhance our team's capabilities to solve problems.

The second impact was the psychological one. We were accustomed to show work-in-progress tasks and get feedbacks. It made us easier to ask questions and discuss solutions. We could propose, accept, and try new ideas without fear. Additionally, we often drilled trouble shootings and recovering services as Learning Session to acquire skills of "psychological safety". We have been reducing psychological pressures by atmosphere, mechanisms, and skills.

The third and last impact was for evaluation. We could reduce the burden of personnel evaluation dramatically for both an evaluator and a member to be evaluated. On one hand, I, an evaluator, can touch members' activities, achievements, and impediments directly everyday through Learning Sessions. Therefore, I can evaluate each member quickly, easily, and properly everyday. On the other hand, members can appeal their achievements to me very easily. Additionally, we can adjust behavior each other through daily observations and feedbacks to meet the team's objective. We didn't need to set evaluation meetings at once around the evaluation period and it saved our time and resources. We can say it as an Agile way of evaluation and human resource management.
<br />

#### 3. TEST AUTOMATION FOR RESILIENCE
For overcoming the limitation of testing and quality assurance in the era of Microservices, we decided to shift our focus to resilience, deployment, and release rather than detecting bugs and solve them beforehand.

At first, we started combining Karate framework with [Zipkin](https://zipkin.io/), a distributed tracing system. Our failure detection system with Karate was good at fast detection of failures and outages. However, it could not pinpoint a root cause in a fleet of Microservices. This was an emerging problem for Product Managers at that time. Therefore, we aimed to make our failure detection system more intelligent.

Our approach was to show tracing information of each Microservice on our test report by adding Zipkin's trace ids to call APIs to test. This test report could pinpoint which Microservice failed by utilizing Zipkin's trace ids. It means that we can pinpoint a Product Manager who is responsible for failed Microservice. Additionally, it can reduce MTTR more and save other Product Managers' time. Our approach was utilizing the idea of observability and monitoring via Test Automation. We named this report as `Sebas Report`. (The name "Sebas" is derived from a famous butler like Jenkins.)

After the release of Sebas Report, we started promoting Karate and Sebas Report company-wide. Additionally, we started recommending to each product development team to utilize not only reducing MTTR, but reducing lead time for changes, and increasing deployment frequency as KPIs to measure improvement and productivity. I utilized the idea of [Four Key Metrics](https://www.thoughtworks.com/radar/techniques/four-key-metrics) as a way of contribution of our business. After those activities, some teams stopped blindly relying on Quality Assurance Engineers and enhanced the ratio of Developer Testing.
<br />
<br />


### RETROSPECTIVE
We expanded our activities toward engineering management improvement based on decision makers' demands. Additionally, we experimented new ideas like Learning Session and utilizing Test Automation for resiliency. Through those activities, we have been redefining our goals and responsibilities based on continuous experiments to contribute to our business. We can say we transformed us as a team of `Transformational Leaders`.
<br />
<br />
<br />



## 5. LESSONS LEARNED
Throught those series of activities, we learned three new ideas.

At first, Agile methodologies worked for starting up new roles and teams. Product Discovery, Iterative and Incremental Consensus, and showing results iteratively attracted colleagues and decision makers. It helped SET team's starting up a lot.

Second, working closely with product development teams was very effective for improving processes and achieving missions. Just providing guidelines and references to product development teams didn't work. Showing working examples enriched communication. Technical excellence was a necessary piece to provide examples and solutions properly. We utilized technology as a communication driver, however, only technology was not enough. We should leverage communication with both technical excellence and Agile methodologies.

Third, it was necessary to change our responsibilities continuously. We have been changing and expanding our responsibilities from Test Automation, engineering management improvement, innovations, to Transformational Leaders. Those actions are for contributing to our business based on continuous experiments.

⭐️Summary
Tons of problems have been there.

There are a lot of persons who has technical skills but not enough problem solving skills
- 技術力はあっても、課題の言語化とその解決方法に目が行かない人ばかり。

Microservices is useful for independent developability and deployability
but expansion of Microservices strengthen apathy each other
only feature team didn't work
Hard to test, recover, and so on.
So Need whole image


- Beyond Quality Assurance
Build quality in is becoming common for some services/products.
Make testing Microservices easier by tools (Karate), process improvements, new KPIs, and so on.
`Productivity Engineers`.
    - Organizational Performance/Culture
    - 「品質」→ビジネス価値の向上・ビジネス損失の削減・DXの向上
- 継続的なインパクト：DX強化？
- Team of Transformational Leaders
    - 究極は、CTOチームとして、DXの改善＆ビジネス価値の提供を実現する
    - "WOW DX”!
        - persuing "WOW DX" (= Great Developer eXperience for LINERS).
    - コンサル型では機能しなかった。実際のツール・開発で実践して価値を出し続ける事が肝要ではないか？
    - Quality Assuranceからの脱却


- SET/Agile は、その点で価値がある/価値を示す必要がある。
    - 仕組みを作り、それを広める。
    - 課題発見・解決能力を持ち、施策をチームの隔てなくリードする人間が必須。
- 人材・文化の変更
    - 個々の技術を追う人間と、全体から「次のアクション」を考えリードする人間とに二分化される
    - 全体を追うという意味でのpracticeを確立していく必要性
    - 「技術で他者を責める」から、「他者を繋いでいく」方向へシフトさせていく
- We can say we transformed us as a team of `Transformational Leaders`.
<br />
<br />
<br />



## 6. WHAT'S NEXT?
⭐️
The first one is building `Testable Infrastructure`!
- Production-like test environment (with k8s and Containers)
- Immutable Test Infrastructure (with k8s and Containers)
    - Reduce barriers of testing
- Container as Mock/Test Harnesses
    - Make testing easier

We are investigating [Testcontainers](https://www.testcontainers.org/):
- [Immutable and disposable RDBMS for testing](https://www.testcontainers.org/modules/databases/)
- [E2E Testing with WebDriver](https://www.testcontainers.org/modules/webdriver_containers/)

⭐️
The second is to organize testing ideas, terminologies, and techniques.
- There are confusion among test automation not only for Microservices.

⭐️
The last one is to adopt to` Design Sprint` for Technical Problems
- Agile2021で話す予定なので軽めに
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

Business Agility in practice.
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
- [Diffusion of Innovation](https://www.infoq.com/presentations/process-evolution-flat-structure/)
- Honeymoon number: [AntiPractices: AntiPatterns for XP Practices](https://www.ime.usp.br/~ale/xpAntipatterns.pdf)
- [Ito] Ito, Hiroyuki, "Technology-Driven Development: Using Automation and Development Techniques to Grow an Agile Culture" Agile 2014 Conference, Orlando, Florida
    - https://www.agilealliance.org/wp-content/uploads/2015/12/ExperienceReport.2014.Ito_.pdf
<br />
<br />
<br />



# レビュアー向け補足
- Markdownでの見易さを考慮して、文ではなく意味の単位で改行しています。
    - 後日、Wordでリリース版を作成する際、これらの改行は削除します。
