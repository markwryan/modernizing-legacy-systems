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

A single project/solution/repository which contains multiple products as well as their shared dependencies.

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

* a tangible project (desktop app, web app)
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
### packaging

+++
Flexibility

Note:
Versioning each component separately, no longer forced to release everything all at once

+++
Clarity

Note:
Clearly defined relationships between packages. Allows for each package to be first class citizens, with its own set of documentation, CI, tests, and releases.

+++

Reenforce Contracts

Note:
More obvious the contracts between pieces and how important they are to be clearly visibile and managed. The differences between method visibility, information sharing, APIs should be more clear between the internal components

+++

Limiting Scope

Note:
In a monolith, a single change can immediately impact all of the applications. Versioning and packaging each component allows changes to be rolled out in a controlled fashion instead of immediately consumed.

+++

Testing

Note:
Smaller, more concise packages are less intimidating to start adding in tests. The increased time and complexity to make a change, build a package and locally deploy and test it will also push developers to write more automated tests that can test and validate changes without having to go through the entire build and deployment lifecycle.

---

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

### paket

---

### circular references

---
### internal dependency tiers

---
### in flight changes

+++
updating with changes from the monolith

```
cd monolith
git pull origin master
git subtree split --prefix src/Libs/Utilities -b split-utilities
git push origin split-utilities
cd ../Utilities
git pull monolith split-utilities
git push origin master
```
+++


---
### git knowledge gaps

Note:
Talk about how difficult it was for people to take over and deal with moving in packages

---
### too much of a good thing

Note:
Talk about how tempting it was to use the packages more than just in the single app. We started using them
for more projects because they were readily available. Problem was that the documentation and knowledge around
the process to update and manage the packages didn't yet exist.

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



