## Question 2

I haven't worked on a large software project where I deployed code to production, but I have made mistakes in work that affected other people. One example was submitting a document without checking all the details carefully. After submitting it, I realised that some information was either missing or incorrectly formatted, and I had to spend extra time correcting it.

The biggest lesson for me was that fixing a problem after delivery usually takes more effort than checking it before submission. A simple checklist could have prevented the mistake.

I connect that experience to this assignment. In the construction payroll scenario, a small error like incorrect overtime data or a missing configuration value can affect many workers. The goal of quality engineering is not to blame the person who made the mistake but to build a system that catches common errors before they create bigger problems.

This has changed the way I think about quality. Instead of depending on individuals to remember everything, I think good processes and automated checks help teams work faster and with greater confidence.

## Question 3

If I had to pick one thing for this team, I would introduce a simple automated quality gate before code reaches the main branch.

I chose this because it solves several problems at the same time. The product manager wants to ship faster, the senior developer relies on experience, and the new developer is afraid of breaking existing functionality. A basic quality gate with automated checks helps all three without adding a lot of extra process.

I would start with a small set of high-value checks instead of trying to test everything. For example, the application should build successfully, critical API endpoints should respond correctly, and the main payroll and attendance flows should pass a few fast automated tests. If any of these fail, the code should not be merged.

I believe this is more effective than introducing long manual checklists or a complicated approval process. People naturally follow systems that fit into their daily work. A fast automated check becomes part of the development process instead of an obstacle.

The recent production incidents in this scenario show that small mistakes can have serious consequences for workers and payroll teams. A simple quality gate would have reduced the chances of both incidents reaching production while allowing the team to continue moving quickly.

## Question 4

I would not try to convince the senior developer by giving presentations about the importance of QA. He has worked on the codebase for years and has solved many problems, so I would first try to understand why he prefers his current approach.

In my first week, I would look for one recurring problem that wastes his time. If there is a bug that keeps coming back, I would write a small automated test for that specific issue and show that it prevents the same problem from happening again. The goal would not be to change his workflow overnight but to remove repetitive work from his day.

I would also keep the tests fast. One concern mentioned in the scenario is that long test suites slow development. I would focus on a small number of high-value tests around payroll, attendance, and critical API endpoints. If these tests save the team from production issues without adding noticeable delays, people are more likely to trust them.

I think the best way to build support for quality is through results rather than arguments. If the senior developer sees that automated checks reduce interruptions and help new developers work more confidently, quality becomes a practical tool instead of an additional burden.


## Question 5

One system I have built for myself is the way I prepare for important exams and deadlines. Instead of trying to study everything every day, I divide the work into smaller tasks and track my progress. I focus first on the topics that have the highest impact and review them regularly instead of waiting until the last minute.

Over time, I realised that the best system is not the most complicated one. A simple routine that I can follow consistently works better than a perfect plan that I eventually stop using.

I think the same idea applies to quality engineering. A team is more likely to follow a quality process if it fits naturally into their workflow. A few reliable automated checks that run quickly are more valuable than a huge test suite that developers avoid because it takes too long.

This assignment has reinforced my belief that good systems should help people rather than create extra work. Whether it is personal planning or software quality, the goal is to reduce mistakes, make progress predictable, and allow people to focus on the work that matters most.


