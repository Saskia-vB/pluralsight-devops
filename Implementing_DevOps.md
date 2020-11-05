# Implementing DevOps in the Real World

## Who cares about DevOps?

### Why DevOps matters

#### Some trands in software development
- Decline in the use of commercial software
- Focus on getting software into production
- Fove away from plan-build-run as separate concerns
- Competitive advantage: fast time to market and constantly experiment

### The challenge of transforming without it
- lack of trust: between business units and IT partners, IT isn't see as business partner but cost centre, not a group to collaborate with for innovation but that you dump projects to
- oppressive tech debt: you made choices that have increased costs later on making it hard to take on new projects
- lack of automation
- competing silo priorities: each silo has a different definitions of DoD - you loose side of the customer and deployment pipeline
- focus on efficiency and local optimisation: sometimes efficiency is done at the cost of flexibility and adaptability which is needed in customer oriented world
- culture doesn't accept risk, change: skillsets are wrong, hard to expect top-down directive to enforce DevOps

### Benefits of a DevOps culture
- defined by outcomes
- cultural norms
- reducing the distance between people, teams and activities and reducing size of work allows you to increase productivity
- look at high performing IT organisations they:
  - 200x more frequent deployments
    - linearly increase number of deployments as they increase number of devops
  - 24x faster recovery from failure
  - 3x lower change failure rate
  - 22% less time on unplanned work
  - 50% less time remediating security issues

### Core DevOps values and characteristics
#### Core values
- Trust
- Empowerment: teams and individuals are empowered to solve problems
- Accountability: can't empower people without making them accountability, when you build and run service you are now accountable for the choices you made
- Continous improvement: always learning, always getting better, always reflecting on what you're doing, and assuming everything is a new experiment
- Data-driven decisions: difficult to improve things you don't measure, you need to measure
- Customer empathy: doing the thing that is going to improve the experience of someone else

#### Characteristics
- optimized for throughput
  - getting things through pipeline
- clear view of entire pipeline
  - think about lifecycle of service
- customer-centric definition of "done"
- small, frequent software releases
  - small debug service, smaller chance of going wrong
- defined feedback loops
  - from customers, from operations to development and vice-versa
- automation-centric
  - use automation to make devops happen, demnstrating you're doing things in a repeatable fashion
- focused on outcomes, not activities

### Changes that come with DevOps
- philosophy changes: do-adapt model, treat code as something that's release quality at all times
- team changes: keeping teams single focused on a service
- tool changes: tools that enable automation, integrating APIs, more open sources software
- satisfaction changes: more likely to recommend place of work

### DevOps objections
- "doesn't scale to companies of our size": not the case, has scaled for some very large companies, it isn't resigned to small companies, it is something that has lots of case studies from large companies
- "we don't have the tech skills that startups do": investing in your own folks, devops is not just a top-down or grassroot directive, there has to be both sides where someone invests financially in devops and the people you already have
- "our executives don't think IT has value and is decreasing their IT investment": IT has some good processes, talents and procedures that can be helped if you streamline it, start building the trust back
- "our compliance needs are too complicated for this": devops increases your security profile, all steps are automated, you don't have log ins, everything can be audited later
- "my company buys commercial software, we don't build anything": there are certain things you always buy (ie database), choosing the right things to build, some of the problems you need to fix nowadays you don't have commercial solutions
- "it's just another fad that we can wait out": this is becoming the new normal, being customer centric, as we become more mogul, you risk being overtaken by someone who is

### Challenges with enterprise-scale DevOps
- devops is going to work differently in an enterprise than it does in startups
- core principles remain the same, but all devops does not look alike
- for enterprises:
  - more stakeholders: more people to keep in the loop, somethign you need to factor in your ceremonies
  - functional silos in place: organisational change management,
  - existing technical debt to manage: existing systems that may not always be ready to change, how you might add proxy layers and not devopsing your main frame
  - specific compliance requirements: feel like you can't do devops unless you do cloud but you can do automation behind the cloud
  - outsourcing arrangements in place

### "Week in the life" viewpoint
- what are the steps
- tips to get started
- core practices
- recognising change management

#### Monday
##### The values of team standups
- what: regularly occured meating talk about blockers, etc
- why: team members, interested parties
- why: transparency, throughput, delivery focus
  - orients everyone, situational awareness to the team
  - drawing attention to important info
  - coming together to remove blockers: figuring it out together
  - facilitate continous improvement
- tips: shared calendar with milestones, keep brief, don't force everyone to speak, set an example that asking for help is ok

##### Using on-call engineer rotations
- what: assign on-call engineer
- who: rotating person on the application team
- why: develops empathy, focus on the customer
  - puts the focus on customer and service
  - encourages code instrumentation, improvement
  - helps other team members stay focused
  - record of experiences help the team
- tips: sign up for pager service to have clear notification process, make it easy to find who is on-call, do dry-run exercises to flex the process, add an "executive on-call" to the rotation

##### Planning software sprints
- what: plan next sprint, defined window
- who: whole application team
- why: focus on small batches, delivery pipeline
  - product owner maintains backlog
  - start meeting with retrospective
  - team decides amount of work in sprint
  - sprint scope doesn't change
  - team always ships at the end of a sprint
  - sprint window should keep shrinking
- tips: have a product owner, dedicated to the one project, responsible for product backlog, facilitator with stakeholders, begin with one month sprints, don't use planning session to design, if add work you need to subtract work from sprint, change process regularly to improve
##### How to review new software requests
- what: triage new feature requests
- who: product owner, stakeholders
- why: continual improvement, customer focus
  - do realistic reviews of new requests: if users don't think they're voices are heard they won't continue
  - cross-functional participation: what is useful for one could be for another, a lot of different perspective to properly reflect voice of customer
  - immediately adjust backlog priorities
- tips: triage features and bugs in this meeting, support team and on-call engineers should attend (voice of stakeholders also), reject the majority of requests not because not great but because you won't do them all, be critical, only take in the things that mater the most (data driven decisions) this will keep your team focused, product owner retires old backlog items: at a certain point they will not be done but may inform future decisions

##### Merging and testing code constantly
- what: merge code with the master branch
- who: all engineers
- why: small batches, limited work-in-progress
  - continous integration drives confidence
  - test coverage is key to trusting automation
  - fast-feedback reduces wasted time later on
  - frequent tests mean smaller debugging surface
  - aim for green builds, don't fear red
- tips: source control repository is a must-have, get visual indicators of build status, avoid long-lived feature branches (branches are a sources of waste, the longer teams work in insolation on branches the harder it will be to merge - checking into master every night?), make working code a forcing function

##### Summary
- team standups
- using on-call engineer rotation
- planning software sprints
- how to review new software requests
- merging and testing code constantly

#### Tuesday

##### Handling support tickets

###### Standup
- what: org/team standup - constantly adjusted based on what happened yesterday
- who: team members, interested parties
- why: transparency, throughput, delivery focus

####### Support ticket
- what: handle support ticket
- who: on-call engineers, front-line Support
- why: responsiveness, Accountability
- primary responsibility of on-call engineer that week
- using same ticketing system as support personnel, some may be handed over from previous on-call engineer but you need to track them
- may become a group effort to resolve
- sparks ideas for new features to propose
- tips: consolidate unique ticketing systems, don't assign on-call engineer additional work, have test bed ready to reproduce issues, avoid handing over tickets,

##### Patching infrastructure
- what: patch server clusters
- who: engineers on the application team
- why: consistency, responsiveness, security
- make patching route uneventful:
  - upgrades required up and down stack
  - infrastructure as code
  - multiple approaches possible: puppet, ansible, etc - create containers and push to production to replace existing ones
- tips:
  - do integration testing with infrastructure
  - define a policy to never log into servers, do not touch production servers directly - use immutable servers for example - servers should be something you only touch for automation
  - introduce config management everywhere
  - aim for immutable infrastructure over time

##### Pairing on cross-functional features
- not just having application features but also infrastructure features
- what: pair on infrastructure oriented features
- who: engineers on the application team
- why: cross-training, collaboration
- infrastructure is code too:
  - hire generalists with specialists: cover different things within the team, hopefully will be able to pair and work with engineers in other areas, nice mix of skills
  - all configuration details in source control: make sure you're checking all the configs in the env you set up
  - test rigorously in production-like environment
- tips:
  - make infrastructure work visible
  - pair ops engineers with software engineers: break down barriers
  - test infrastructure just like software

##### Detecting and responding to outages
- service interruptions will happen but devops teams don't fear them, you've got processes and procedures to handle this
- what: detect service interruptions
- who: support staff, on-call engineer
- why: responsiveness, accountability
- disciplined approach to problem solving:
  - upfront instrument pays off
  - use facts to figure out causation: mean time to recovery is faster
  - communication is key: don't be scared to tell people that server is down, much worse if customers are surprised by disruption
  - over-alerting causes fatigue: constantly continuously improve alerting internally to make sure you're not over-alerting with false positives etc.
- tips:
  - identify core metrics that measure availability
  - add tech for inside-out, outside-in tests
  - make dashboards visible, proactive
  - have unified way to communicate status

##### Communicating with stakeholders
- what: send status update to executives, being visible, what are key problems, metrics, status health, etc.
- who: team leaders - to adjust mindset also in terms of planning, finance etc.
- why: transparency, trust
- communicate and iterate
  - DevOps is a cultural change, and requires transparency: evangelising a lot, demonstrate success
  - share more core business metrics: show technical things, up coming release, change success rate, list out priorities and risks - make them visible
  - build momentum through demonstrated progress: continue to be visible and demonstrate success
- tips:
  - choose handful of core metrics to share: keep it succinct otherwise it won't be read
  - maintain regular rhythm: everybody should be well informed
  - show good and bad news to build trust: demonstrate bad even within DevOps teams, comfortable to say things aren't going well
  - keep refining based on feedback: ask stakeholders what matters and keep refining the metrics and reports accordingly

##### Summary
- handling support tickets
- patching infrastructure
- pairing on cross-functional features
- detecting and responding to outages: no where to zero in on a and fix something and be data driven
- communicating with stakeholders: demonstrating progress, business impact


#### Wednesday

##### Org/team standup
- what: org/team standup
- who: team members, interested parties
- why: transparency

##### Onboarding new team members
- what: onboard new engineer - you may be rotating, have people come in to learn and bring back to their team
- who: application team and any stakeholders rotating people through
- why: cross-training, customer focus - make something that is organisational wide
- speed to productivity:
  - learn from source control, deployment, pipeline, wiki: dispense knowledge through these sources, understand what the team is going through and what matters in the system
  - good opportunity to test deployment pipeline: do proper code scanning so even new incomers can push code as of first day
  - pairing accelerates readiness: sit with someone, learn new languages and frameworks that are being used on the team and get up to speed
- tips:
  - new team members pair with existing ones
  - encourage use of application itself: be a consumer of what you're actually building, understand user experience, get empathy right away
  - add to on-call rotation quickly: intimidating but great way to learn and instantly understand application (within first 6 weeks)
  - iterate onboarding docs based on feedback

##### Establishing monthly operations review
- what: attend monthly operations review
- who: application team leaders, executives
- why: customer focus, continuous improvement
- accountability breeds focus
  - remain focused on customer metrics: teams should be loosely coupled, collectively delivering an experience
  - leverage collective knowledge: you don't want local optimisations to screw up global concerns - it's a chance to have a global context, share info metric wise, getting together and making sure you're using your peers
  - improves situational awareness for executives: have executives know what's going on, giving them an active view of data, chances for executives to give good context to DevOps teams
  - not a problem solving session: not an eight hour meeting, this is chance to mention key concerns and then follow on conversations if need be later on
- tips:
  - ensure each app team defines success and has own metrics: iterate on this, see what other teams do, other people may provide feedback, good chance for continuous improvement
  - schedule a monthly review: keep it consistent, it's a regular occurence
  - lead by example and mention challenges: set a precedent, start with transparency and mention issues, if someone brings up a negative issue -> you should show enthusiasm
  - actively follow up on problem areas: action items but do not use meeting to do this

##### Conduct retros after incident
- what: conduct incident retrospective/postmortem
- who: on-call engineer, stakeholders
- why: continuous improvement, transparency
- culture is revealed during retrospectives:
  - not about assigning blame: when accidents and failures occur, instead of looking for human error look at how to redesign system to prevent it from happening it again
  - assemble timeline: showing timeline of things to happen, good telemetry, someone should think of this during problem
  - use facts to review what happened: what you actually did,
  - explain what worked, what didn't: adding things to shared doc/record, shows focused on continuous Learning
  - develop action plan and assign owners: turn it into an action plan, going back to the system, to backlog etc.
  - put record into discoverable place: what have you learned and put it as public as possible (with customers and internally)
- tips:
  - set up a retro day after next incident
  - choose an interface for collecting feedback: people can interact with live during meeting
  - define crisp action items: proper counter measures, have actual real action items
  - assign someone to keep and share minutes:

##### Collaborate across Teams
- what: collaborate across teams
- who: application team leads, engineers
- why: removed bottlenecks, improve flow
- collaboration in an across teams:
  - no team should be entirely independent: share technology
  - think locally, act globally: make sure your team is successfully and optimising independence
  - create systems for quick collaboration and decision-making: help people quickly collaborate maybe with chat room, whiteboards so ppl can just stop and plan something, not require formality and make it quick
- tips:
  - invest in chat room technology: great way to quickly collaborate, share information, box for checkins - interactive, lively environment
  - set up loose boundaries and guidance for commonalities: shouldn't have teams using different tools (tickets, chat, etc.) - you want to give teams freedom but not hurt the organisation as a whole using so many independent things and increasing cost
  - foster cross-team communication through hackathons: excuse to get together and build stuff, taking the time for teams to work together, foster cross-team relationships over things that don't feel like work

##### Summary
- onboarding new team members
- establishing monthly operations review
- conduct retros after incidents: representative of your culture
- collaborate across teams: almost impossible to have dependencies across-teams, how are you working together

#### Thursday
##### Standup
- what: org/team standuo
- who: team members, interested parties
- why: transparency

##### Change team processes
- what: replace team process following retro - more consistent and faster experience to shrink mean to time recovery
- who: team leaders
- why: continual improvement
- DevOps is about improving flow
  - hard to improve what you're not measuring -> have data and metrics then you can improve on them
  - act on broken processes, bottlenecks: key to improving flow, focus on increasing throughput, identify weakest link and not go around it
  - automation is often but not always the answer: sometimes it is about training, improving how we bring the team together
  - experiment and measure: small batches, continuous improvement, feedback loop - try new things and collect data so if it isn't working well you know
- tips:
  - solicit feedback from entire team
  - listen to calls to stop at "good enough" - sometimes you can go over a certain level of throughput so make sure you just maximise your throughput
  - only buy products/services with APIs: create automation around those things, create consistent processes that don't expose themselves to human errors
  - evangelize to other teams: other people can get better based on what you learn

##### Create content about releases
- what: write knowledge base articles, release notes
- who: application team, others in company
- why: knowledge sharing, throughput
- faster delivery means more frequent explanations
  - as velocity increases, harder for users to track changes: smth to consider -> what is the impact on your user on a continuous changing system? how are they staying informed?
  - content must be easy to create, edit and find: democratising the content creation, make it easy to contribute information to team knowledge base or company knowledge base
  - change log and broadcast engine are important: git based repos, you can't assume people are always reading documentation so need to push information/notifications to keep people updated
- tips:
  - set up an open content system
  - still have 'owners' but many contributors
  - define a light review process - pull requests work well!
  - open up to those outside the team

##### Update the deployment pipeline
- what: upgrade deployment pipeline
- who: application team
- why: increased automation
- deployment pipelines grow into a system of record
  - build a better audit trail over time: good chance you'll be more compliant, easy to audit the whole thing, doing a security fix
  - first CI/CD attempt may be lightweight
  - partner with groups like InfoSec and Compliance: their automation pipeline calls apis to create tickets
  - cross-functional skills come in handy
- tips:
  - do value stream mapping with cross-functional team: get stakeholders involved, focus on customer experience
  - test changes repeatedly in non-prod environments: cloud is beneficially because you can spin up production like environment
  - use or create APIs to integration with existing audit-visible systems

##### Right-size the engineering teams
- what: right-size team rosters so that stakeholders and funders know that these are not static, times where it grows and shrinks
- who: executives and team leaders - making smart choices
- why: responsiveness - reacting and responding business needs
- fluid teams support adaptable strategies:
  - application teams aren't of fixed size - funding products not projects, also want to demonstrate as engineers you are making business driven decisions
  - engineer count may swell during key periods, contract after: preempt high needs, you need a structure that allows you to add people without slowing down throughput
  - rotate operations, security expertise throughout
  - offers maximum flexibility to respond to changing business: show that you are also responsive to what matters the most to business
- tips:
  - create culture of rotating opportunity: make it feel like a natural not a punishment
  - use data to make decisions: which teams need help, what the impact may be, what is the benefit, how did you arrive at that number
  - avoid over-adjusting: don't do this every week, too much uncertainty and angst that will be counter productive
  - define tech standards that reduce transition time for engineers

##### Summary
- change team processes
- create content about releases: now with increased velocity the content become stale much faster so you need to increase velocity of documentation to match
- update the deployment pipeline
- right-size the engineering Teams: make it part of your culture

#### Friday

##### Stand up
- what: org/team standup
- who: team members, iinterested parties
- why: transparenc, throughput, delivery focus

##### Package code for software release
- what: package code for release
- who: CI process, on-call engineer
- why: fast flow
- packaging must be repeatable, comprehensive:
  - package is the result of a successful CI pipeline: CI pipeline is constantly in green state, so code is ready to be delivered, always have a god state
  - multiple ways to package an application: different needs for different apps, could be binaries, raw code or a container
  - packages should include all pieces needed to deploy: need infrastructure code, smoke test components, are there some third parties for log collection? different environment variables? overall deployment script as well. - this should all be in source control
  - ensure that packages can be recreated: the same package should go through all different environments in the same way
- tips:
  - document current process to find non-automated steps
  - consider investing in package repository
  - only use containers as output of CI not as input - create container files as output, pulled as part of CI process and then you have a great image at the end of it

##### Deploy the application to production
- what: deploy app update to production
- who: deployment pipeline, on-call engineer
- why: last part of delivery pipeline
- ship often for better outcomes:
  - should be so heavily produced that it becomes boring: you want deployment that even the newest person on team can do without being freaked out
  - multiple techniques available to minimize downtime: switch all the traffic between two environments, canary releases: reduces risks to slowly make changes by making it just regional first for instance, feature flags; ship the codes constantly but marketing can choose when to flip the switch
  - have telemetry in place to measure impact(positive or negative of release): maybe everything technically is fine but business metrics also allows you to see user side
- tips:
  - try automated deployments with individual services before moving to entire systems: move up to data intensive systems
  - blue/green deployment may be easiest way to start: two identical environments to switch between
  - closely watch system and business metrics after deployment: make sure health of business is good and hopefully improving with software you're deploying

##### Attend team lunch
- what: attend team lunch
- who: everyone
- why: team-building, sense of unity
- trust is a foundation of DevOps:
  - build relationships within and across teams: focused on long live support, you will depend on them when their's outage, you'll get tickets from them when there is a problem, just have mutual respect for each other
  - these connections are important in a crisis or during retrospective: people to trust each other
  - meet-ups should be planned by team and executives: investment in building team unity
- tips:
  - buy lunch once a week for teams
  - for meetings, use video conferencing: actually looking at each other if you have a remote team, seeing a reaction
  - don't force group socialization but also encourage 1:1 opportunities

##### Cross-teams function
- what: cross-train teams
- who: anyone in the organisation
- why: continual learning, transparency
- share local learnings more broadly:
  - "show and tell" to train, educate: not just for software engineers but maybe infrastructure features or a new bot or a new product management technique
  - particularly useful for front-line support engineers: understand the new system, defects that might pop up
  - spark ideas within other teams: avoid duplication, no reason for every team to do the same thing
  - share results of experiments with new technology: demonstrate the new thing, maybe it becomes part of the system or maybe it doesn't but encourage feeling on constant learning
- tips:
  - ask teams to demo after they ship
  - invite broad audience outside application Teams
  - record for playbook and archive

##### Summary
- package code for software release
- deploy the application for production
- attend team function
- cross-team function

### Characteristics of a DevOps environment
- optimized for throughput
- clear view of entire deployment pipeline
- customer-centric definition of "done"
- small, frequent software releases
- defined feedback loops
- automation centric
- focused on outcomes, not activities 

### Learning resources
#### Books:
- The Phoenix project
- DevOps Handbook
- Starting and Scaling DevOps in the enterprise
- Lean Enterprise
- The Goal
- Team of Teams
- American icon
- Creativity, Inc
- Designing Delivery


### Summary
- Why devops matters
- challenges of transforming without it: tech debt
- benefits of devops culture: lower failure rate, less randomisation
- core devops values and characteristics
- changes that come with DevOps
- devops objections
- challenges with enterprise-scale DevOps
