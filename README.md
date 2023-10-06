# Tangible Computing
[BX Coding's](bxcoding.org) tangible computing project aims to make computing more accessible for K-5 learners through a physical brick-based programming language. This page is a living document of the project's research, design, and development.

## Project Goals
1. Make computing more accessible to a young age range (K-5)
2. Make classroom-scale computing education cheaper
3. Inspire young learners to identify with the Maker identity

## Project Status
Currently, this project is in the **research** phase. We are conducting a wide sweep of academic literature on the topic of tangible computing and assessing the potential solution's feasibility. If you have interest in the project please reach out.

# Literature Review

## Motivation
Teaching computing to children is valuable as it provides a new way of thinking, an algorithmic view of the world, as well as potentially an interest in computing program that will translate into further exploration.
However, outfitting an entire class with personal devices is costly, and sharing a handful requires student cooperation, constant teacher attention, and non-computer work in the lesson plan.
Our system wants, ideally, a symbolic physical representation of the programming logic and physical output.
​
If we are focusing on a classroom setting, one of the main benefits as pointed out in a paper describing the AlgoBlocks system, is the ability for many students to collectively feel like they are part of the programming process by crowding around the blocks, as well as being able to more effectively point out issues, as the blocks were larger than text or blocks on a computer screen. It also allowed for collaboration, as non-verbal cues could be used to indicate turn taking.<sup>4</sup>

## Commonalities
The benefit of having a physical output is clear in that younger children who do not have an interest in computing yet can immediately related to the physicality of the robot, and understand what they want it to do, and what it is doing in space.
The earliest versions of this were the turtles that were controlled by languages like LOGO.
They all noted that too much onboarding and explanation would cause the students to disengage.<sup>2,5</sup>
Indicator lights for progress in execution.
Functions were often distinct segments with their own "main block" whatever that happened to be.<sup>1,2</sup>
​
Common things taught:
- Conditionals and branching
- Variables
- Debugging<sup>2,5</sup>
​
## Questions
Is event-based programming a separate concept?
- I feel that it would be more tangible for young learners to immediately have access to event-based, such as sensor input and such, but would it have the potential to confuse the teaching of traditional sequential control flow? Maybe we introduce it one after the other.
Will we have to have each function be its own individually powered block? 
- Storing in sequence with rest of program contiguous with header block seems like it would be confusing for students.
- General trend seems to have functions be separate headers/main blocks.
One of the key limitations as the system as currently envisioned is that the individual blocks cannot give feedback unless plugged in and powered by the source block. For example, if we wanted to have a guided lesson about conditionals, and a student had not yet added in an if statement, perhaps we would wish the if statement to blink, but this could not happen without power.
Do we assume that instructors have any sort of technical experience?
- For the purpose of programming block identities with binary switches or configuring integration with any physical robot output
## Potential Features/Takeaways
One of the papers mentioned a sequence of instructional tools, Tern -> Kibo -> Cubetto that all symbolically represented code in the physical world, which may be worth looking into.
​
One of the weaknesses identified in the Project Bloks paper was easier classroom-wide collaboration and instructor led instruction. We could potentially do this by having a model program to compare against, which could be activated by the instructor to blink red on student blocks that were out of place.
​
In terms of instruction philosophy and curriculum construction, it would probably be helpful to introduce blocks in stages so as to not overwhelm the kids with an influx of new information and logic to work with.<sup>2,5</sup>
Understandability to the children and the ability for them to learn for themselves is a priority (example, TORTIS child losing interest after being instructed on complex memory block, or physical form factor considerations on bloks)
Samuel Papert described turtles as an object-to-think-with:<sup>3</sup> objects in which there is an intersection of cultural presence, embedded knowledge, and the possibility for personal identification.
Value of robot output (proposed Spike integration) is obvious as it gives the output that exists in the realm of physical and spatial intuition that children already have.
I identify the primary added value of the symbolic physical representation (the blocks) as an object-to-think-with is multiple levels, people who do not yet know how to interact with mouse and keyboard based GUIs may find it easier, but more importantly it provides the opportunity for physical input and direct physical involvement in the control flow.
​
In terms of adding more value to physical symbolic representation of code, we could enable physical interaction with conditionals, with touch or light sensors, that allow you to be directly involved in the control flow.
Systems like Tern<sup>6</sup> also have a specific form factor to their conditionals and branching that physically indicate the role of the block, such as a Y shape or a connecting string.
Multiple other input controls other than the current potentiometers to be considered for numerical input, such as: faders, sliders, dials.
Outputs like noise<sup>2</sup> and vibration are also compelling to students.
Representation of numerical status of blocks could be done through seven segment display.
A method of flagging should exist as well (maybe a toggleable indentation on the side of blocks?).<sup>5</sup>
​
One of the greater values of a new programming paradigm is making it more intuitive for younger children:
Debugging Consists of 4 Steps: <sup>5</sup>
1. Compare the goal and the actual outcome
2. Articulate the discrepancy between the two
3. Identify the source of the discrepancy
4. Fix the discrepancy
​
Having an interface that enables each of these steps would enable students to debug more easily and gain confidence with the skill as well as acquire all the benefits that accompany it, such as logical thinking, problem solving, and social interaction.<sup>5</sup>
### References
1. [Project Bloks Position Paper](https://projectbloks.withgoogle.com/static/Project_Bloks_position_paper_June_2016.pdf)
Intention to teach computer programming as a way of thinking, algorithmic view of the world. 
History of tangible programming:
- Cricket
- Pico Cricket
- GoGo Board
- Arduino
- Phidget
- Lilypad: programmable textiles
- Tobopo: program by example
- Tern -> Kibo -> Cubetto: representational tangible programming with blocks equivalent to programming elements.
Expansion of IoT capability greatly expanded the design space and number of hackers able to enter the space.
However, many of these designs are not compatible and have designs that are very specific to their use case and market niche.
One thing that is required is a platform that helps to enable low cost and common standard for tangible computing.
Other motivation is to expand the benefit of tangible computing beyond simply just having a physical representation of programming.
Other gaps include allowing for easier collaboration and easier teacher coordination of lessons. 
Bloks allows for more focus on higher level features like visual, haptic, auditory response and form factor design.
Mentions implementation of functions, recursion, and easy access to sensors and output. 
Mentions faders, buttons, sliders, and dials as input. 
Bloks can be connected in any orientation, horizontal, vertical, or even a grid.
Ran user studies on 5-8 year olds, noted important form factor elements that helped the kids learn without needing an amount of onboarding that would disengage the students. Magnetic snap fitting, form factor matching puck function, lock and key connections to indicate correct order of connection.
Kids had issues with conditionals putting them in the wrong order, etc.
Debugging is a key skill being taught and one of the most difficult, one of the ways that they got around this was red lights to indicate compilation error and green blinking to indicate running. Kids quickly picked up debugging and understanding which block was presenting issues.
Functions were implemented with labelled blocks, which would link to a blok that served essentially as a function header.
​
2. [TORTIS(Toddler's Own Recursive Turtle Interpreter System)](https://files.eric.ed.gov/fulltext/ED118366.pdf)
Controlled a rolling robot with bump sensors, a light, a pen that could go up and down.
The design of the system consisted of 3 button boxes and 2 blox boxes, with a noted intention being to introduce a few concepts at a time so that a child does not become overwhelmed or decide that he is incapable.
Don't give problem that are too hard for them to solve.
Specific topics being taught numbers, breaking down instructions into steps, debugging, recursion, variables, and conditionals.
Mentions expansion to programming music as an important one, as children like noise.
Small commands box: evokes immediate action depending on the button pressed on its face
Commands box: includes a row of numbers in addition to movement commands, as well as an interrupt, introduces repeated sequences
Memory box: start remembering, stop remembering, run, stop, and forget.
	Plugs into commands box and remembers the input
Blox box: has slots for command blocks which have pictoral representations of the commands on them. The slots are pushbuttons which can allow the user to immediately jump to that point in execution, as well as a slot for the number of repeats, a condition (event-based touch sensor), and variables.
Placing a colored block at the beginning of a row names it as a procedure.
Separate variables screen that uses colored shapes to map variables.
Explores the psychology of which environments work best for teaching.
Dedicated adult and not too many other children, as that adds pressure or judgement to the environment.
Pretending to learn alongside, being excited and lighthearted, encouraging them with project suggestions but not forcing them to try new things if they are not yet comfortable.
​
3. [The LOGO Turtle](https://cyberneticzoo.com/cyberneticanimals/1969-the-logo-turtle-seymour-papert-marvin-minsky-et-al-american/)
Lots of photos**
Early educational physical programming tools focused on having a physical output for programming that still occurred on computers. LOGO language used to control tripod pen vehicle which could draw.
Used to teach how to invert a series of operations, teach the concept of functions, which aided later in algebra.
Seymour Papert
"I could use my body knowledge to understand the movement of the robot"
Described as an object-to-think-with: objects in which there is an intersection of cultural presence, embedded knowledge, and the possibility for personal identification.
​
4. [AlgoBlocks](https://www.researchgate.net/publication/242383829_Algoblock_a_tangible_programming_language_a_tool_for_collaborative_learning)
Pedagogical value of programming languages comes from:
1. Easy operation -> promotes trial and error
2. Simultaneous Access
3. Mutual monitoring -> allows you to learn from others
4. Natural turn taking
Computer screen has limited amount of people able to crowd around it, indicating and pointing is harder on a computer screen compared to large blocks.
Argues that the attention provided to tracking when people wanted a turn, passing off computer peripherals detracts from the natural flow of collaboration.
Additionally, natural gestures to take turns emerged, such as simply reaching for blocks.
​
5.  [RoboBlocks](https://www.researchgate.net/publication/239761488_Robo-Blocks_designing_debugging_abilities_in_a_tangible_programming_system_for_early_primary_school_children)
Highlights debugging skills as being important for development of logical thinking, problem solving, and social interaction skills.
Uses intrinsic motivation to teach problem articulation, team work, and persistency.**
Tested on 52 students and noted an increase in ability to identify problems and think of ways to correct them.
Main board onto which command blocks are connected, using seven segment displays to allow the children to visualize the extent to which each motion command is carried out.
Ability to execute the program step-by-step
Debugging Consists of 4 Steps:
1. Compare the goal and the actual outcome
2. Articulate the discrepancy between the two
3. Identify the source of the discrepancy
4. Fix the discrepancy
"Thus, children tend to enjoy the cycle of making rough implementations of their ideas, see how they work, then go back and make adjustments and fix errors. This cycle continues until the goal is accomplished".
Enables rapid prototyping.
Used drawing and maze game as primary motivating examples to teach the children how to use the system, introduce the elements slowly.
Debugging flags were used to allow the children to mark when something had occurred, as many did not like to step through, but instead let the entire program run and forgot where the observed error was.
Implementation:**
Command Block
RS-232 Serial connection for communication
Acrylic laser cut and then bent with heat gun
Microcontroller inside allowed identification etc.
Magnets served as connection points as well as communication channels
Master Block
Similar Microcontroller
Protocol to request the structure of the blocks from all of the connected blocks
Code was actually run all on the master block, with only requests to light LED sent out to the command blocks themselves
Transmit control information to the robot
Robot was constructed one of Lego one of acrylic and non-LEGO motors, controlled through the GoGoBoard robotics kit RF receiver. 
​
6. [Tangible Programming in the Classroom with Tern](http://hci.cs.tufts.edu/tern/inter191-horn.pdf)
Teaching computing is expensive and requires constant adult attention, the syntax of computing languages can be cryptic.
![Screenshot 2023-09-15 at 11 18 00 AM](https://github.com/BX-Coding/tangible-computing/assets/32718462/65d2237e-a2e0-4d33-8be3-65b98c2e7079)
Form matching function:
Y shaped branching, the rope for jump and land
Tern uses blocks with computer vision to compile the code using a camera attached to a normal computer.

# Contact Us
Project lead: Elliot Roe - elliot@bxcoding.org
Developer: Tiger Peng

## Funding
This project is funded by [BX Coding](bxcoding.org)
