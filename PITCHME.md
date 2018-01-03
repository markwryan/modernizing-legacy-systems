### tales from the front lines
#### modernizing a legacy system


---

Mark Ryan

AXS

https://github.com/markwryan/modernizing-legacy-systems

Note:
What is AXS? Explain role at AXS.

---
## moving away from a monolith

+++

## why?

Note:
In a perfect world, we shouldn't touch the repo and leave it as is. Lay out why not doing that might be the right choice under certain cirumstances.

+++

## issues

Note:
Issues abound -- both from a technical and non-technical perspective.

+++

## workarounds

Note:
Talk about how to overcome the issues at hand, both for the technical problems, as well as business and people problems that are involved in the process.

+++

## process

Note:
Go through some tools and workflows that were helpful

+++

## lessons learned

Note:
Things we could have done differently

---
# @fa[exclamation-triangle]

+++

## not selling anything

Note:
Not trying to convince anyone this is the only way. If a monolith works for your company, great!

+++

## continually growing process

Note:
Set the stage and set some expectations. Goal of the talk is not to sell one solution in the best, but to educate around some issues and solutions to the issues.

---
## monoliths

```
A single project/solution/repository which contains multiple products as well as their shared dependencies.
```

---
### motivations

+++

structured, automated releases

+++

separate releases

+++

limit immediate scope of library changes

+++

moving into the cloud

---

### a starting point

* central repository
* multiple websites, desktop apps, tasks and libraries
* no internal dependency management
* git
* ci
* minimal test coverage :(

---

### picking a target

* a tangible project (desktop app, web app, scheduled task)
* being worked on by a single team
* lesson learned: the more self-contained the better

Note:
How we decided on a subject to first try and split out. Note that having a single team working on the project makes things easier, also talk about how picking a more self-contained, or one with few internal dependencies might be easier

---

### moving to a new repo
+++

created a new repository

+++

copied the project to the root directory

+++

pushed to new remote

### splitting up with git
* move project to it's own separate repository
* keep history

---
### dev life improvements

the smaller project lead to faster load times and better overall performance in our IDE compared to loading the entire monolith

---
### splitting out libraries

---
### in flight changes

---
### packaging

+++

Building library releases off tags

+++

Building a dependency graph

+++

Hosting packages

+++
Issues when packaging 
multiple builds of the same version


---
### developing with packages

---
### git knowledge gaps

---
## versioning

useful semantic versioning


---

### building


---

### deploying

---
### deploying libraries

---
### deploying apps

---
### feedback from team

---
### points of improvement


---
### summary

---
### questions



