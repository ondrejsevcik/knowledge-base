# An Elegant Puzzle: Systems of Engineering Management

> There’s a saying that people don’t leave companies, they leave managers.

## Introduction

This book is for managers.

## Organizations

- Managers should support six to eight engineers
- Managers of managers should support four to six managers
- Fewer than four people is not a team 
    - Doesn’t abstract the indifiduals enough
- Keep the innovation and maintenance together
    - The team that’s doing maintenance should be also the one that innovates, otherwise there will be burnout, higher morale, culture of learning and you avoid creating two separate tier-class system
- Ideal size of team is six to eight people
- Four states of team
    - 1. Falling behind - can’t even fix the bugs
        - Fix - Hire more people
    - 2. Trading water - can fix bugs, but no innovation
        - Fix - consolidate teams effort, limit work in progress
    - 3. Repaying debt - fix bugs, and fix tech-debt
        - Fix - add time, the team needs to fix the tech-debt
    - 4. Innovating - Majority of work is satisfying customer needs
        - How to sustain - maintain enough slack so the team can build quality to their work
- High performing teams = sustainable productivity
- Moving members from high-performing teams to low performing is not recommended
    - Now you have two low performing teams
    - People have to create new bonds
    - It is better to move work from one team to the other
- Hiring have to be steady
    - Otherwise existing engineers spend all their time on interviews and training new engineers

## Tools

### Developers velocity

1. Delivery lead time - time from code to production
2. Deployment frequency
3. Change fail rate - how frequently changes fail
4. Time to restore service - time spent recovering from defects

Feedback loop
- Pull requests -> ready commits (Code review rate)
- Ready commits -> Deployed commits (Deploy rate)
- Deplyed commits -> Incidents (Defect rate)
- Incidents -> Reverted commits (Recovery rate)
- Reverted commits -> Pull requests (Debug rate)

### Product management - exploration, selection, validation

1. Problem discovery
2. Problem selection
3. Solution validation

### Visions and strategies

- as the organization grows beyond 50 people, you will add third layer of management
    - no way you can control everything anymore
- create strategy and vision
- Strategy
    - document that explains trade-offs and actions that will be taken to address a specific challenge
- Vision
    - Aspirational document that enable individuals who don’t work together closely to make decisions that fit together closely

### Metrics and baselines 

- After some time, discussion shift from projects to goals
    - Goals let you define "what", not "how"
- Defining clear goals takes a practice

1. a **target** states wher you want to reach
2. a **baseline** identifies where you are today**
3. a **trend** describes the current velocity
4. a **time frame** sets bounds for the change
        
> Example: In Q3, we will reduce time to render our frontpage from 600ms to 300ms. In Q2, render time increased from 500ms to 600ms.

