### tales from the front lines
#### modernizing a legacy system


---

Mark Ryan

AXS

https://github.com/markwryan

Note:
What is AXS? Explain role at AXS.

---

###### https://github.com/markwryan/modernizing-legacy-systems

---
# @fa[exclamation-triangle]

+++

##### not selling anything

Note:
Not trying to convince anyone this is the only way. If a monolith works for your company, great!

+++

##### the issues ahead are complicated

Note:
Not feasible to cover everything in 45 minutes, the road ahead is not black and white. It is important to continually reflect and take time to consider options as changes are made.

+++

##### continually growing process

Note:
Set the stage and set some expectations. Goal of the talk is not to sell one solution in the best, but to educate around some issues and solutions to the issues.

---
#### moving away from a monolith

+++

##### why?

Note:
In a perfect world, we shouldn't touch the repo and leave it as is. Lay out why not doing that might be the right choice under certain cirumstances.

+++

##### issues

Note:
Issues abound -- both from a technical and non-technical perspective.

+++

##### workarounds

Note:
Talk about how to overcome the issues at hand, both for the technical problems, as well as business and people problems that are involved in the process.

+++

##### process

Note:
Go through some tools and workflows that were helpful
---
#### monoliths

A single project/solution/repository which contains multiple products as well as their shared dependencies.

---
#### motivations

* structured, automated releases
* separate releases
* limit immediate scope of library changes
* moving into the cloud

---
#### a starting point

* central repository
* no internal dependency management
* git
* ci
* minimal test coverage :(

---
#### a subject

* a tangible project (desktop app, web app, scheduled task)
* being worked on by a single team
* lesson learned: the more self-contained the better

Note:
How we decided on a subject to first try and split out. Note that having a single team working on the project makes things easier, also talk about how picking a more self-contained, or one with few internal dependencies might be easier

---
#### splitting up with git
* move project to it's own separate repository
* keep history

---
#### splitting out libraries


---
#### packaging


---












