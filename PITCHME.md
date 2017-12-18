### Tales from the Front Lines
#### Modernizing a Legacy System


---

Mark Ryan

AXS

https://github.com/markwryan

Note:
Who is AXS? Explain role at AXS.

---

## Slides

* Give link to the slides so people can pay attention

---

## A Warning!

* Not here to tell convince you to move your company away from a monolith
* The issues ahead are complicated
* Only here to share my experience and motives that lead to us starting move away from developing inside a monolith
* Continually growing process

Note:
Set the stage and set some expectations. Goal of the talk is not to sell one solution in the best, but to educate around some issues and solutions to the issues.

---

## Life as it is

* A central repository, containing the majority of our apps, websites and libraries
* No internal dependency management, direct references across projects
* Version control in git
* Basic CI
* No tests