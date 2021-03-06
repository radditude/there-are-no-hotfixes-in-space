layout: true 
class: center, middle, inverse
---

# There Are No Hotfixes In Space

A partial history of the development process involved in creating the computers & software used in early manned spaceflight.

Made with [Remark](https://github.com/gnab/remark#remark) and [Remarker](https://github.com/kt3k/remarker).

???
- Disclaimer: this presentation contains nothing of immediate use to our work.

---

# Project Mercury

## 1958 - 1963

???
- This was the first manned spaceflight program.
- Includes famous names like Alan Shepard & John Glenn.

---
layout: false
class: inverse

.left-column[

## AKA the Flying Tin Can

].right-column[

- no onboard guidance system
- relatively rudimentary controls
- a radio

]

???
- The flight needs of Project Mercury were pretty straightforward:
  - Ascent, controlled by the angle of the rocket used at launch.
	- Descent, controlled by small positional thrusters.
	- Parachute & water landing.

---
layout: false
class: inverse

.left-column[

## How It Worked

].right-column[

#### Control Centers in Maryland and Florida

- calculated orbital/re-entry trajectories
- determined what instructions to send the astronaut
- relayed instructions and received data from tracking stations

#### Worldwide Tracking Network

- chain of 18 stations around the equator
- responsible for communications
- as the spacecraft passed in range overhead, each station had a few minutes to get readings from the spacecraft, receive any communications from the astronaut, and relay instructions from the Control Center

#### Total: ~18,000 support personnel for each Mercury flight

- about 3,000 of these were in the control centers/tracking stations

]

???
- ...which is the only way this system could have possibly worked.
- It was basically a very well-coordinated global relay race.
- Trivia note for _Hidden Figures_ fans: Katherine Johnson, one of the key figures in the book and a mathematician famed for accuracy, would have been at the command center calculating trajectories during Mercury flights.

---
layout: true 
class: center, middle, inverse
---

# Project Gemini

## 1961 - 1966

???
- Needed to make a successful rendezvous with an upper-stage rocket, which would give it much more maneuvering capability.
- This more complex flight pattern demanded finer control and automation of some of the things that had been calculated manually during Mercury missions.

---
layout: false
class: inverse

.left-column[

## Gemini Computer Specs

].right-column[

- custom built by IBM
- weighed 60 pounds
- took 420 ms to multiply two numbers
- tape system to store additional programs and expand the tiny memory
	- loading each new program took 6 minutes

]

???
- Subject to various issues from the vibrations of takeoff and re-entry
- For reliability, there was a 3-way voting system.

---
layout: false
class: inverse

.left-column[

## Software Design

].right-column[

- written in a variant of assembly language
- originally conceived as a single enormous program and each new mission would be a new unique program
	- programmers quickly realized that this was a lot of unnecessary work
	- introduced a module system
	- also useful because once they started actually writing software they promptly ran out of memory
- three levels of testing
	1. "unit tests" - verifying the equations
	2. man-in-the-loop simulation to pinpoint input/output
	3. "integration tests" - testing with the full crew interfaces 

]

???
- Hardware was king at this point in computing history.
- Software was a very young discipline, just beginning to be considered more than admin work.
- Fortran had only been around for a few years and was considered too inefficient for this application.
- The tape system was added because of the memory issue.

---
layout: true 
class: center, middle, inverse
---

# The Apollo Program

## 1961 - 1972

???
- includes Apollo 11, otherwise known as the moon landing

---
layout: false
class: inverse

.left-column[

## Apollo Guidance Computer Hardware

].right-column[

- built by MIT
- weighed 70 pounds
- utilized read-only core rope memory and a small amount of read-write ferrite core memory
- total memory was ~72kb (rough estimation in modern units)

]

???
- MIT took the job before seeing any specs or requirements and apparently regretted it because the project dragged on much longer than it was supposed to.
- Had to increase the memory 18 times while developing the software because they kept running out of space.

---
layout: false
class: inverse

.left-column[

## Software Design

].right-column[

- Read-only core rope memory was a huge challenge
- The iteration was as follows:
	1. Engineer codes part of the guidance software in AGC assembly language
	2. AGC assembly language was compiled into binary
	3. The binary was sent off to a factory, where workers hand-wove it into rope memory
	4. The rope memory was tested and a bug or manufacturing flaw was found
	5. Repeat ad nauseam for about 3 years

]

???
- The core rope memory was chosen because it was extremely able to withstand power fluctuations and the vibrations of takeoff and landing
- AGC assembly language was specially developed for the project because of memory constraints
	- sacrificed some speed for the need to fit more information in a small space
- Developers could not develop with the actual flight hardware

---
layout: true 
class: center, middle, inverse
---

.center[![Margaret Hamilton](./assets/image.jpg)]

???
- Margaret Hamilton with all the code that she and her team wrote in the course of the Apollo missions

---
layout: false
class: inverse

.left-column[

## Further Reading

].right-column[

1. _Computers in Spaceflight: The NASA Experience_
	- by James E. Tomayko
	- the book that inspired this here presentation
	- [full text available online](https://history.nasa.gov/computers/contents.html)
0. The Apollo 11 code on Github
	- [https://github.com/chrislgarry/Apollo-11](https://github.com/chrislgarry/Apollo-11)
0. An online simulator of the inputs and outputs of the Apollo Guidance Computer
	- [http://svtsim.com/moonjs/agc.html](http://svtsim.com/moonjs/agc.html)
0. More info about [core rope memory](https://www.youtube.com/watch?v=P12r8DKHsak)
0. Colin Fulton's 2017 RubyConf talk, [_Bugs In Space!_](http://confreaks.tv/videos/rubyconf2017-buuuuugs-iiiiin-spaaaaace)

]

???
- Yes, the title is a reference to George Lucas telling 19-year-old Carrie Fisher that there is no underwear in space. I'm a nerd.

---
layout: true 
class: center, middle, inverse
---

Made with [Remark](https://github.com/gnab/remark#remark) and [Remarker](https://github.com/kt3k/remarker).
