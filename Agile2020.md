# Everything from Scratch: Practical Ideas in an Organization without a Concept of Process Improvement



## Abstract
In this experience report, I present practical ideas to establish a new role, to improve product development teams, and to proceed company-wide problem-solving from scratch in the very strongly technology-oriented and fast-growing company without a concept of process improvement and clear supporters.

LINE Corporation [1] has been growing very rapidly and globally. However, the company had been struggling with increase of outages and they had given negative impacts to users and company's profits simultaneously. Since I joined LINE Corporation as the first member of “SET” (Software Engineer in Test) [2] in 2017, I and our team have been solving a wide variety of problems including reduction of outages, innovation in testing tools, onboarding, and so on by combining technical solutions and Agile methodologies based on my experiences as an Agile Coach. We have been pursuing "best for our users and business" fiercely and relentlessly with a series of experiments. Now, some teams in our company utilize our ideas that we reflected, experimented, and succeeded from scratch.
<br />
<br />
<br />



## 1. INTRODUCTION
"LINE" is a free message, voice calls and video calls service for smartphones that has released since 2011. Our company name is derived from this service [3].

After the first release of “LINE”, LINE Corporation has increased its users and messages transferred rapidly and globally. Especially, its high-quality sound, and the "sticker" feature that we can send a variety of rich emoticons as a message attracted a lot of users.

For adapting to the rapid growth of LINE, we have been improving LINE's architectures and code base iteratively. We chose Microservice Architecture [4] to earn scaling out, independent development, and fast delivery capabilities.

However, increase of Microservices has been causing increase of outages simultaneously. The more we expand business areas like fintech, the more troubles at Integration Points [5] among each Microservice increase. Negative impacts to LINE users and company's profits became measurable in 2017.

LINE Corporation had struggling with solving these critical problems for themselves but failed. Because LINE Corporation was a strongly technology-oriented company and it didn't have a concept and experience of process improvement at that time. There were very few leaders and supporters to improve this situation.

Therefore, LINE Corporation had started looking for proper leaders externally. Evaluated over five years of my experiences and achievements as an Agile Coach and Test Automation engineer, I joined LINE Corporation as the first member of SET in September 2017.
<br />
<br />
<br />



## 2. ESTABLISH SET ROLE BY ATTRACTING DECISION-MAKERS AND COLLEAGUES

### CHALLENGES
After joining LINE Corporation, I faced with tons of challenges to start my work as SET.

The biggest challenge was that a sense of crisis about increase of outages was not shared among employees. Only a few decision-makers were acknowledged and concerned about emergencies to solve negative impacts of outages to LINE users and company's profits as rapidly as possible.

Additionally, there were no clear ideas and solutions for increase of outages in the company. LINE Corporation had not experienced process improvements until then because of its very strongly technology-oriented fashion. Wide adoption to Microservice Architecture became a barrier to consider solutions beyond each service or technical silos.

Moreover, there were no shared understanding and consensus about SET role among decision-makers. LINE Corporation established SET job without clear objective, missions, and responsibilities. The company's intention at that time was very naive that just introducing Test Automation to the company might solve something.
<br />
<br />


### ACTIONS
My focus was to obtain consent from decision-makers and colleagues by discovering their real concerns and providing solutions iteratively and incrementally.

#### 1. SHARE A SENSE OF CRISIS BY VERBALIZING REAL CONCERNS
I thought not only decision-makers and colleagues but also I should know real problems LINE Corporation was facing with in a knowledgeable way. It was time to follow an ancient saying by Sun Tzu: "If you know the enemy and you know yourself, you will have almost 100 battles". From my experiences of Agile, I thought "Product Discovery" [6] might fit well.

Therefore, at first, I talked developers, QA persons, Product Managers, senior managers, and executives to hear their concerns and troubles directly. Through these conversations, I acknowledged that they had lots of non-verbalized problems. Additionally, I got that there were no persons who could verbalize these problems and share with other colleagues.

Next, I focused on helping colleagues to verbalize their concerns and to share them with other colleagues.

I investigated our services and products. I utilized "SonarQube" [7], a static code analysis tool, to know the code coverage and technical debts for each service. I also implemented and run some of unit and integration test scripts to know real behaviors of the products. Test scripts are good for understanding software under test [8] and finding problematic services.

Additionally, I focused on "outage reports". "Outage report" is a term which means both a published report and a postmortem meeting in our company. From these reports, I acknowledged that 1) reports were too technical to know impact on sales and profits, 2) reports didn't consider clear goals and actions to prevent the outages, and 3) "Channel Gateway", an aggregation service of our APIs towards external users, was the most problematic products.

After investigating services and outage reports, I could verbalize colleagues' concerns as follows: 1) increase of Channel Gateway's outages was the most critical issue that was giving negative impacts to external users, 2) failure detection of Channel Gateway took an average of 1 week and it was not acceptable for a Product Manager, and 3) testing APIs was insufficient in almost all of services because few persons knew how to test APIs programmatically. I shared these verbalized ones and agreed them with colleagues, managers and executives.
<br />

#### 2. GIVING IMPACTS CONTINUOUSLY TO INCREASE SUPPORTERS
For getting support from colleagues and decision makers to proceed with radically new actions, I tried to "give impacts" [9] constantly to them.

From the first week I joined LINE Corporation, I achieved something and shared them with coworkers and decision makers every week. Especially, I focused on providing working software, executable ones, and quantitative information.

Here is a list of achievements for my first 10 weeks.

| Week    | Achievements                                                     |
| ------- | ---------------------------------------------------------------- |
| Week 1  | Started writing test scripts to understand services/products     |
| Week 2  | Proposed first idea of SET activities to decision makers         |
| Week 3  | Built mechanism to run and report static code analysis regularly |
| Week 4  | Shared with developers how to build static code analysis         |
| Week 5  | Proposed milestones of activities to decision makers             |
| Week 6  | Agreed with proposals/milestones with decision makers            |
| Week 7  | Collected information and tools of QA/Tests in one place         |
| Week 8  | Implemented failure detection for public APIs                    |
| Week 9  | Guided to start regular meetings with developers and QAs         |
| Week 10 | Started solving problems by developers step by step              |

When I gave impacts, I utilized "3 KPIs"; Sales, Profit, and Employee Satisfaction. It is that my former supervisor told me as a way to measure every business. For example, my first proposal of SET activities to decision makers included reducing MTTR (Mean Time To Repair) of Channel Gateway by implementing proper failure detection mechanism for reducing negative impacts to external users. Additionally, I not only reported results of static code analysis, but also shared with developers how to build static code analysis mechanism from Employee Satisfaction aspect.

As a result, many developers started using my "impacts" like static code analysis mechanism and giving me concrete advices about problematic points of architectural design, operational difficulties, and so on. Their advices became good information sources to communicate with decision makers. Additionally, decision makers started taking time to define SET role with me. They couldn't ignore my "impacts" and developers' supports to SET.
<br />

#### 3. ITERATIVE AND INCREMENTAL CONSENSUS
⭐️In parallel with "giving impacts", 
- I tried to consensus with them constantly
- for obtaining consent from from colleagues and decision makers to go ahead.

At the end of the first week I joined LINE Corporation, I built the first rough ideas of SET including objective, missions, responsibilities, solutions, and milestones based on gathered information I mentioned above. Additionally, I proposed them to "decision makers" like senior managers and executives.

I don't think that I can build the perfect solutions and agree on them with decision makers at once. I supposed that it would be preferable not only me but decision makers to continue proposing ideas, getting feedbacks, and improving proposal. Additionally, there were few persons who could lead "strategy formulation" in LINE Corporation at that time. Leading decision-making gave impacts to decision makers and it was good for attracting their interests in SET. Therefore, I chose to iterate build-propose-learn cycle weekly as "Iterative and Incremental Consensus" approach.

My first proposal was focusing on improving Sticker Shop due to frequency of outages, however I didn't define milestones. Through this approach, rough milestones were enough useful for decision makers to understand tasks, plan, and due date easily and quickly. Additionally, they also said that it was OK to update milestones if we knew additional information. Moreover, they taught me that public APIs were more important than Sticker Shop at that time from business perspective. On the other hand, they agreed on my idea that utilizing Test Automation for making failure detection faster and reducing MTTR was valuable as SET's responsibility. Through this approach, I could improve my proposal step by step. Finally, we agreed on the first solution and milestone within 45 days since I joined LINE Corporation.

⭐️
requested me to propose goals and milestones. They were what decision makers wanted.

As a result
Quick agreement on the first solution and milestones of SET was a good sign.
<br />
<br />


### RETROSPECTIVE
The idea of "Product Discovery" worked for clarifying responsibilities and activities of SET. Additionally, "Iterative and Incremental Consensus" was useful for collaborating with decision makers and agreeing with them quickly. Moreover, "managing impacts with 3 KPIs" attracted lots of colleagues from business perspectives, not only from technical ones.
<br />
<br />
<br />



## 3. INNOVATE SOLUTIONS BY EXPERIENCING HARDSHIPS TOGETHER

### CHALLENGES
After clarifying responsibilities and activities of SET, getting decision makers' supports and colleagues' interests, I started actions as SET. Additionally, LINE hired new employees and formed a team of SET. I thought we could proceed our activities more quickly and widely. However, we faced with new obstacles.

At first, we implemented a failure detection system for public APIs, however, it didn't become established in the product development team. We implemented test scripts for these APIs, called them via CI servers periodically, and notified errors and failures to the product development team quickly. We utilized Test Automation and CI as a failure detection system. We also used the common technologies like JUnit, Spring Boot, Jenkins, and so on for the product development team. Failure detection worked partially and some developers started implementing them. Although, test scripts written in JUnit were hard to read, implement, and maintain for the Product Manager and most of developers. Additionally, SET team and the product development team have been working at different offices. Our communications weren't sufficient to proceed improvements.

Other obstacle was that performance problems at Sticker Shop had emerged. They had been using one in-house performance testing tool. However, it couldn't provide enough capabilities to detect emerging issues. Moreover, they need to write test scripts with groovy, an unaccustomed programming language for them. Therefore, writing test scripts was not fast and effective.

Another challenge was that consulting-style approach didn't work. We often provided guidelines, ideas how to design good test scenarios, and test script examples widely. However, most of colleagues didn't utilize them to improve their testing problems. We needed to find ways to expand ideas and to improve their work more effectively.
<br />
<br />


### ACTIONS
For achieving our mission, we started working with product development teams deeply to improve their processes. In other words, we started working, learning, and solving essential problems with them.
<br />

#### 1. REFINE FAILURE DETECTION SYSTEM WITH KARATE
For public APIs, we started direct conversations with the product development team members to discover their real needs and concerns at first. In other words, we did "Product Discovery" approach again. We talked daily via video conference system. We discussed with the Product Manager if he came to our office.

Through these discussions, we found that test scripts written in JUnit were hard for them. Therefore, we investigated and proposed lots of testing tools to them.

Finally, we chose Karate [9] framework. It provides features specific to API Testing with BDD (Behavior-Driven Development) style and Gherkin format. It was easy to read, implement, and maintain for both developers and the Product Manager. Especially, defining the preferable state was easy to understand for them.

After decision to use Karate framework, we SETs and the product development team members started rewriting test scripts from JUnit to Karate collaboratively. SETs wrote examples at first. SETs guided "Developer Testing" to achieve and expand "Build Quality In" idea by working with developers. SETs supported solving architectural problems of Karate. After 3 months' collaborative work, finally failure detection system with Karate became established in this product development team.
<br />

#### 2. IMPLEMENT NEW PERFORMANCE TESTING TOOLS WITH KOTLIN
For Sticker Shop, we did the same approach as public APIs to discover their real needs and concerns at first.

We found that improving to use the existing in-house performance testing tool was impractical. It could produce only 10% of loads what we wanted to test. It was not easy to expand and/or modify features. Additionally, most of the product development team's members were familiar with Kotlin language. Implementing test scripts with Groovy was hard for them. Moreover, usage of Docker [10] and Kubernetes [11] were expanding at that time in our company. We thought it was a good chance to utilize these new tools and approaches to improve our performance testing.

Therefore, we decided to create a new in-house performance testing tool named "Ayaperf". Ayaperf is a Java wrapper of Locust [12] that can use Kubernetes to increase loads easily with enough volume. Developers can write test scripts of performance testing with Java and Kotlin. We did iterative and incremental style to implement and improve Ayaperf with Sticker Shop developers. After 3 months' collaborative work, finally Ayaperf became stable. Developers started detecting performance issues with it before release. Additionally, they could correct issues by themselves without hurting production code. They found and solved 3 hidden performance issues by utilizing Ayaperf.
<br />

#### 3. IMPROVE PRODUCT DEVELOPMENT PROCESSES AS A HABIT
At public APIs and Sticker Shop, we found the effectiveness of working with product development teams to find their real needs and solve them. This approach worked well. However, I thought it was not enough and sufficient. I saw that lots of teams stopped solving problems by themselves after coaches left teams. It is a failure if improvements don't continue after coaches' left. Therefore, I expanded our activities to making product development process improvement as a habit especially at public APIs.

We had found and solved issues as homework every week. We had continued applying new Karate features and refactoring test scripts. Additionally, we had implemented a notification mechanism via slack to reduce MTTR. Moreover, we had asked product development team members for clarifying objectives, quantitative values they will provide to users, and rough milestones of each task every week. We utilized the idea of Scrum framework to make continuous improvement as a habit of the team. We had continued these activities for about 3 months.

After that, the product development team became able to clarify quarterly milestones, prioritize tasks based on business values, and improve test scripts and the failure detection system by their own. They started decreasing outages dramatically. They really became the self-organized team. Finally, we stopped supporting the team.
<br />
<br />


### RETROSPECTIVE
We could solve essential problems and improve processes of each product development team by working collaboratively and deeply with them. We SET and product development teams implemented Test Automation and related techniques based on the idea of "Product Discovery". Additionally, each team becomes sophisticated. For example, the Product Manager of public APIs writes test scripts with Karate routinely. He often says that the Product Manager may disturb the team by writing production codes, but can contribute to the team by writing test scripts! He is utilizing test scripts to understand behavior of the product deeply, to clarify next actions and goals of the product and the team, and to guide team members doing "Developer Testing" for "Build Quality In".

Additionally, we learned a lot of things to improve our approaches through working with them. The consulting-style approach is useful to keep the whole image of activities, however, we cannot approach essential problems. On the other hand, the working-together approach is effective to discover and solve essential problems quickly, but we may lose the whole image of activities because of too focusing on one product development team. Therefore, we should utilize both styles based on the phase of activities.

The English word "compassion" derives from Latin's "compati", which means "suffer with". We think this is the point of leading and guiding new things like Agile. We SETs and product development teams had been suffering from the same problems by working together. We had considered solutions and solved problems one by one together. These series of activities had constructed real collaborative relationships. Moreover, these relationships had become boosters for adapting to new Test Automation tools and process improvements.
<br />
<br />
<br />



## 4. PROCEED COMPANY-WIDE PROBLEM-SOLVING AS TRANSFORMATIONAL LEADERS

### CHALLENGES
We had been solving a lot of technical and process issues of each product by working together with each product development team's members. These activities and achievements have been recognized as huge successes by executives. However, these successes had led us SET team to the next level of challenges.

The first challenge was the company-wide strategic and management problems. A lot of product development teams could not show their own missions, goals, plans, and milestones to decision makers like senior managers and executives beforehand. Additionally, these teams couldn't share their current status and problems in a timely manner. Decision makers had been frustrating that they couldn't make decisions properly and precisely. On the other hand, we SET team had been showing that information timely from the beginning of all activities. Therefore, decision makers requested us SET team to teach product development teams to express that information properly.

The second challenge was about onboarding. In July 2019, our team had 4 members and we hired one recent graduate and one mid-career employee simultaneously as new SETs. To proceed our activities smoothly, we needed to make onboarding as the top priority task.

The third one was a doubt about testing and quality assurance. LINE Corporation hires Test Engineers and Quality Assurance Engineers. However, most of them had only been doing End-to-end testing manually via client applications. In the era of Microservices, I thought it is not practical to detect bugs and solve them beforehand with these activities. Additionally, most of them didn't care about deployment, release, and contribution of our business. They were just interested in doing their own tasks by developer's requests. Such behavior was not what we SET aimed to do. On the other hand, we named our role as "Software Engineer in Test". The word "Test" made our colleagues misunderstand that we SET were the same as Test Engineers and Quality Assurance Engineers. The notion of testing and quality assurance were just a burden and a constraint that narrowed our activities to improve services and products. Therefore, I thought we needed different approaches to change these assumptions drastically.
<br />
<br />


### ACTIONS
For solving these totally different challenges, we started lots of actions including not only Test Automation and technical ones, but also engineering management, education, innovation, and so forth.
<br />

#### 1. LEAD ENGINEERING MANAGEMENT IMPROVEMENT
For solving the company-wide strategic and management problems, we had started showing our activities and installing our ways into other teams. In other words, we had started leading engineering management improvement based on decision makers' demands.

At first, we shared our milestones with other teams over and over again as an example of engineering management strategy and planning. Additionally, we held workshops for these teams to support their planning, defining mission, reporting, and so forth. For example, I held the Drucker Exercise [13] and the User Story Mapping [14] workshops to one team for teaching the idea of product ownership. After these activities, some teams started defining their own milestones and sharing them to decision makers in a timely manner.

On the other hand, we attended other teams' meetings to improve. If the meeting was full of verbose and meaningless reporting without any decision making and productive communication, we proposed rules like reporting only necessary for decision making and applying timeboxing. We often utilized the idea of Impact Meeting [15] by Mike Cohn. Moreover, we stopped some meetings that couldn't provide any value. Clarified mission and milestones were useful to distinguish whether the meeting was valuable or not. We could use clear mission and milestones as the pointer of conversation as the same as the User Story.
<br />

#### 2. LEARNING SESSION
For proceeding our onboarding smoothly, I decided to utilize the idea of "Learning Session". Learning Session is a way of study sessions during business hours taught by Chris Lucian at Agile2017 [16].

Here are basic rules. We have been holding Learning Session basically for 30 to 60 minutes every day during business hours as a work. We can choose any topics we assume it's necessary for our daily work. Anyone can speak and facilitate it with Mob Programming way with a fun and without criticism.

Through a series of Learning Sessions, we have been learning a wide variety of tools, techniques, process improvements, and so forth. We learned Karate framework. All team members can set up it, write test scripts, run tests, and teach them to other persons. We became accustomed to shortcut keys of IntelliJ IDEA, JIRA, and Confluence. We often review programs via GitHub's Pull Requests together. We refactor test scripts with learning test and architectural design techniques. We frequently demonstrate our work-in-progress tasks to get feedbacks quickly. Moreover, we experiment process improvements like Scrum, Kanban, the Drucker Exercise, and so on.

As a result, we smoothly finished onboarding for two newcomers. They could write programs, pass reviews, and deploy their programs within 3 days. They could adapt to our team's rules and culture, like demonstrating their results to users very frequently for getting fast feedbacks, focusing on release, and experimental work style, very quickly. They became contributing to our products and services within 1 or 2 months.

Moreover, we found that Learning Session gave 3 additional impacts to our team.

The first impact was the growth of our team, not only of newcomers. We often shared each work among team members. We frequently solved each member's problem together. As a result, all team members could substitute other's works. We can say we have been doing "handover" every day. We could increase the "truck number" coined by Jim Coplien and enhance our team's capabilities to solve problems.

The second impact was the psychological one. We were accustomed to show work-in-progress tasks and get feedbacks. It made us easier to ask questions and discuss solutions. We could propose, accept, and try new ideas without fear. Additionally, we often drilled trouble shootings and recovering services as Learning Session to acquire skills of "psychological safety". We have been reducing psychological pressures by atmosphere, mechanisms, and skills.

The third and last impact was for evaluation. We could reduce the burden of personnel evaluation dramatically for both an evaluator and a member to be evaluated. On one hand, I, an evaluator, can touch members' activities, achievements, and impediments directly everyday through Learning Sessions. Therefore, I can evaluate each member quickly, easily, and properly every day. On the other hand, members can appeal their achievements to me very easily. Additionally, we can adjust behavior each other through daily observations and feedbacks to meet the team's objective. We didn't need to set evaluation meetings at once around the evaluation period and it saved our time and resources. We can say it as an Agile way of evaluation and human resource management.
<br />

#### 3. TEST AUTOMATION FOR RESILIENCE
For overcoming the limitation of testing and quality assurance in the era of Microservices, we decided to shift our focus to resilience, deployment, and release rather than detecting bugs and solve them beforehand.

At first, we started combining Karate framework with Zipkin [17], a distributed tracing system. Our failure detection system with Karate was good at fast detection of failures and outages. However, it could not pinpoint a root cause in a fleet of Microservices. This was an emerging problem for Product Managers at that time. Therefore, we aimed to make our failure detection system more intelligent.

Our approach was to show tracing information of each Microservice on our test report by adding Zipkin's trace ids to call APIs to test. This test report could pinpoint which Microservice failed by utilizing Zipkin's trace ids. It means that we can pinpoint a Product Manager who is responsible for failed Microservice. Additionally, it can reduce MTTR more and save other Product Managers' time. Our approach was utilizing the idea of observability and monitoring via Test Automation. We named this report as "Sebas Report". (The name "Sebas" is derived from a famous butler like Jenkins.)

After the release of Sebas Report, we started promoting Karate and Sebas Report company-wide. Additionally, we started recommending to each product development team to utilize not only reducing MTTR, but reducing lead time for changes, and increasing deployment frequency as KPIs to measure improvement and productivity. I utilized the idea of "Four Key Metrics" [18] as a way of contribution of our business. After these activities, some teams stopped blindly relying on Quality Assurance Engineers and enhanced the ratio of Developer Testing.
<br />
<br />


### RETROSPECTIVE
We expanded our activities toward engineering management improvement based on decision makers' demands. Additionally, we experimented new ideas like Learning Session and utilizing Test Automation for resiliency. Through these activities, we have been redefining our goals and responsibilities based on continuous experiments to contribute to our business. We can say we transformed us as a team of "Transformational Leaders".
<br />
<br />
<br />



## 5. LESSONS LEARNED
Through these series of activities, we learned three new ideas.

At first, Agile methodologies worked for starting up new roles and teams. Product Discovery, Iterative and Incremental Consensus, and showing results iteratively attracted colleagues and decision makers. It helped SET team's starting up a lot.

Second, working closely with product development teams was very effective for improving processes and achieving missions. Just providing guidelines and references to product development teams didn't work. Showing working examples enriched communication. Technical excellence was a necessary piece to provide examples and solutions properly. We utilized technology as a communication driver, however, only technology was not enough. We should leverage communication with both technical excellence and Agile methodologies.

Third, it was necessary to change our responsibilities continuously. We have been changing and expanding our responsibilities from Test Automation, engineering management improvement, innovations, to Transformational Leaders. These actions are for contributing to our business based on continuous experiments.

We SET team have been finding and solving problems gradually and extensively by combining technical excellence and Agile methodologies, and adjusting our responsibilities for our business.
<br />
<br />
<br />



## 6. WHAT'S NEXT?
Currently, we have been trying and investigating the following ideas for further improvements.

The first one is building "Testable and Disposable Infrastructure". Currently, we don't have enough production-like test environments. It makes us hard to test enough to detect bugs and reproduce outages quickly without fear for operation miss and misconfiguration. It becomes a huge barrier for testing. Therefore, we have been trying to build production-like test environments with Container and its orchestration mechanism with Docker and Kubernetes for making testing easier without fear. We are aiming to provide immutable and disposable containers, and a way of building their relationships easily. We named this idea and mechanism as "Testable and Disposable Infrastructure". As a preparation, we are adapting to Testcontainers [19] for testing persistence layer like RDBMS and NoSQL.

The second one is to organize ideas, terminology, and techniques of Test Automation. There are lots of confusion about the difference among Unit Testing, Integration Testing, API Testing, End-to-end Testing, and so on. It is more than Microservices. Therefore, we started summing up these points as a guideline and reference implementations. We clarified how to distinguish Test Levels and design each test as a guideline. Additionally, we implemented and shared reference implementations of them company-wide. Moreover, we held Hackathon events for teaching Karate. At the first event, attendees could implement tests for their product's APIs within 2 hours.

The last one is experimenting "Design Sprint" [20] for solving complex technical problems at a brownfield product. We have been working with one product development team which develops and operates mature product. There are lots of problems, ideas to solve them, and huge confusion. To clarify each problem, prioritize each idea, and experiment whether the idea is valuable or not, we started utilizing an idea named Design Sprint. We try new ideas within 1-week cycle. We gather feedbacks and decide whether to proceed the idea or switch to other one within this short cycle. We continue this inspection and adaptation approach until solving problems. Currently, this team is adapting to Testcontainers and "Testable and Disposable Infrastructure" with this approach.
<br />
<br />
<br />



## 7. CONCLUSIONS
There have been lots of problems. Microservice Architecture is useful for independent develop-ability and deployability, however, it tends to strengthen apathy toward other teams and services/products. Additionally, there are short of leaders who can find and solve problems beyond silos and teams. Moreover, quality assurance approach is not proper for solving outages of Microservices.

We SET team have been solving these problems as follows.

At first, we aim to overcome limitations of feature teams for Microservice Architecture. Many Agile enthusiasts and practitioners insist of the importance of a feature team rather than a component team. However, only applying for a feature team cannot tame Microservice Architecture. Therefore, SET team behaves to tie each product development team, service, and product with providing a whole image of business, and ways to test and recover each service.

Second, we train and nurture leaders who can find problems and solve them beyond teams and silos. LINE Corporation has lots of excellent software engineers. However, there are few leaders. Only technical excellence cannot tame complexity of Microservice Architecture and our business. SET team is effective for nurturing these leaders by utilizing both technical skills and Agile methodologies.

Third, we have been building and expanding tools, process improvements, and new KPIs to get over limitations of quality assurance. The combination of Karate framework and Sebas Report makes testing and recovering Microservices easier. Additionally, the idea of "build quality in" is becoming common for some services/products. Focusing on profitability and MTTR rather than the number of bug detection before releases works now in organizational performance and culture perspective.

SET is derived from Google. This role is responsible for enhancing productivity of engineers by utilizing test automation, automation infrastructure, and process improvements in Google. SET in LINE Corporation tried to start from this definition. However, we have been changing responsibilities continuously for pursuing contribution to our company's business performance. We have been expanding our responsibility from Test Automation to company-wide process improvements with continuous impacts to stakeholders.

Currently, we are transforming ourselves as a team of Transformational Leaders. Our latest mission is "WOW DX" [21], achieving a great Developer eXperience for all of product development team members and stakeholders in LINE Corporation with automation techniques and Agile methodologies. We continue to pursue improving all of our business relentlessly.
<br />
<br />
<br />



## REFERENCES
[1] LINE. https://linecorp.com/en/.
[2] Whittaker, J. Arbon, J., & Carollo, J. 2012. How Google Tests Software. Addison-Wesley Professional.

[1] Transformational leadership. https://en.wikipedia.org/wiki/Transformational_leadership.
[2] Forsgren, N. Humble, J., & Kim, G. 2018. Accelerate: The Science of Lean Software and DevOps: Building and Scaling High Performing Technology Organizations. IT Revolution Press.

[3] Fowler, M. 2014. Microservices. https://martinfowler.com/articles/microservices.html.
[4] Nygard, M. 2018. Release It!: Design and Deploy Production-Ready Software 2nd Edition. Pragmatic Bookshelf.
[5] Hussman, D. 2015. Product Discovery On A Single Page. http://productdiscoverycanvas.com/tag/david-hussman/.
[6] SonarQube. https://www.sonarqube.org/.
[7] Whittaker, J. Arbon, J., & Carollo, J. 2012. How Google Tests Software. Addison-Wesley Professional.
[8] Whittaker, J. Arbon, J., & Carollo, J. 2012. How Google Tests Software. Addison-Wesley Professional.
[9] Karate. https://github.com/intuit/karate.
[10] Docker. https://www.docker.com/.
[11] Kubernetes. https://kubernetes.io/.
[12] Locust. https://locust.io/.
[13] The Agile Warrior. https://agilewarrior.wordpress.com/2009/11/27/the-drucker-exercise/.
[14] Jeff Patton & Associates. https://www.jpattonassociates.com/user-story-mapping/.
[15] Mountain Goat Software. https://www.mountaingoatsoftware.com/blog/four-questions-to-fix-low-attendance-at-your-sprint-reviews.
[16] Lucian, C. 2017. Growing the Mob. https://www.agilealliance.org/wp-content/uploads/2017/02/GrowingTheMob.pdf.
[17] Zipkin. https://zipkin.io/.
[18] ThoughtWorks. https://www.thoughtworks.com/radar/techniques/four-key-metrics.
[19] Testcontainers. https://www.testcontainers.org/.
[20] GV. https://www.gv.com/sprint/.
[21] LINE. https://linecorp.com/en/company/mission.
