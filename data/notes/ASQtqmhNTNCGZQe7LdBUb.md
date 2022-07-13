
- In courses, students are often provided educational problems with clear constraints
  - You immediately know the desired outcome and how to judge it
- A **real-world** problem is typically open-ended and ill-defined
- Types of real-world problems...
  - [[ser222.analysis-design-justification.open-ended]]
  - [[ser222.analysis-design-justification.close-ended]]
  - [[ser222.analysis-design-justification.design-problem]]
    - The design problem is most common in engineering
- Problems can be either [[ill-defined|ser222.analysis-design-justification.ill-defined]], [[well-defined|ser222.analysis-design-justification.well-defined]], or somewhere in-between.
- In homework, we often jump straight into design
  - Really there are two extra steps: [[analysis|ser222.analysis-design-justification.analysis]] and [[justification|ser222.analysis-design-justification.justification]]
## Solving real-world problems
- Basic problems
  - "Where do I start?"
  - "What do I do next?"
  - "Am I done?"
  - "Any others?"
- Not all questions can be answered, but [[analysis|ser222.analysis-design-justification.analysis]] and [[justification|ser222.analysis-design-justification.justification]] can help greatly
- In homework, we tend to jump to *design*
## ADJ
- We want to show that a problem under [[analysis (A)|ser222.analysis-design-justification.analysis]], soundly yields a [[design (D)|ser222.analysis-design-justification.design]], such that the design is an optimal solution to the problem
- The [[justification (J)|ser222.analysis-design-justification.justification]] is a sound argument that the design is the optimal solution for the problem given the analysis
### Soundness
- Parts of our argument build upon each other logically
- Answers must follow from the problem statement
- "`x`, because `y`"
### Process
- When doing engineering, we expect to see some general flavor from process
  - e.g. the difference between Software Engineering and Computer Science
  - There is another aspect as well- control
    - Are we using a process here?
    - Why is using this process good?
    - Why is using this process bad?
    - What would justify the use of this process for problem-solving?
### Definitions
- There are almost always ambiguities - fix them!
- Treat definitions as guideposts
- In general, we need to find places that are under-specified, and then detail them
  - If a problem says "display", we might want to specify as "print each element in the collection exactly once in any order"
  - If a problem says "efficiently", we might want to define it as "run in O(1) if possible"
### Fixing ill-defined problems
- Three things we can think about
  - Making **reasonable** assumptions
  - [[ser222.analysis-design-justification.asking-questions]]
  - [[ser222.analysis-design-justification.performing-experiments]]
### Metrics and measurements
- Before we attempt to do any design work, we need to know what makes a solution good
  - A metric will be a way for us to measure different solutions to the problem
- Ideally, we want
  - Metrics that are useful relative to the problem statement
  - Metrics that are reliable (and if possible can be replicated outside the system)
  - More practically: efficient metrics