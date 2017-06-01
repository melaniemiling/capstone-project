# Objectives
* Learn a Programming Language
* Learn MongoDB
* Implement a Capstone Project
* Utilize GitHub and Google Docs

# Learning a Programming Language
* Install Java SE Development Kit
* OOP (abstraction, classification, specialization)
* OOP (encapsulation, inheritance, polymorphism)
* Basic Data Types and Variables
* Classes and Objects
* Console I/O
* Conditional Statements
* Loops
* Arrays

# Learning MongoDB
* SQL vs. NoSQL Databases
* Document Database
* MongoDB Data Hierarchy (databases, collections, documents, and fields)
* Replica Sets, and Sharded Clusters
* Standalone MongoDB Installation
* Overview of the MongoDB Shell
* CRUD Operations with Filters

# Implement a Capstone Project

## Topics to Select From
* Overview of artificial intelligence
* Overview of backtracking algorithms
* Overview of digitization and image recognition
* Overview of computer simulations
* Overview of finite-state automata
* Overview of expert systems
* Overview of data mining

## Final Selection
Combine Computer Simulations and Data Mining

## Newly Added Objectives
* Learn Java random number generator
* Learn JSON
* Learn mongoimport
* Learn MongoDB aggregation pipeline

## My Project
**Goal:** a statistical analysis of the game, “Snakes and Ladders”.

**Method:**
* Implement a simulation of the game in Java
* Run the simulation a million times
* Capture JSON output from each simulation
* Use mongoimport to import the JSON output into local MongoDB instance
* Write aggregation pipeline queries to retrieve the desired information

## How Does the JSON Data Look Like
```
{
    "turnList" : [
        { "die" : 1, "ladder" :  1 },
        { "die" : 2                },
        { "die" : 5                },
        { "die" : 6, "ladder" : 51 },
        { "die" : 4, "ladder" : 71 },
        { "die" : 4, "snake" :  95 },
        { "die" : 5, "ladder" : 80 }
    ]
}
```

## Sample Statistics

**Longest game:**
```
db.snl.aggregate([
    {$project: {count: {$size: '$turnList'}}},
    {$group: {_id: "Summary", count: {$max: '$count'}}}
])
```

**Shortest game:**
```
db.snl.aggregate([
    {$project: {count: {$size: '$turnList'}}},
    {$group: {_id: "Summary", count: {$min: '$count'}}}
])
```

**Average game:**
```
db.snl.aggregate([
    {$project: {count: {$size: '$turnList'}}},
    {$group: {_id: "Summary", count: {$avg: '$count'}}}
])
```

**Find one of the shortest games**
```
db.snl.find({turnList: {$size: 7}}).limit(1)
```

## Snake and Ladder Use

## Chance of Ending a Game in _n_-Rolls

## Chance of Ending a Game in _n_-Rolls or Less

# Achievements/Challenges/Takeaways

## My Achievements
* Met all original objectives
* Met all added objectives
* Learned how to set goals
* Learned that feedback is important to improve quality
* Learned how to plan my study effectively
* Learned how to be an independent learner
* Expanded my professional network

## Challenges and Lessons
* Always keep time constraints in mind
* Programming is hard
* Logic is even harder
* Making the code “pretty” is hard
* Making time to work on my project at home

## Takeaways
* Trial and error is OK
* Neat code is important
* The Internet is your friend if you’re stuck
* It helps to arrive earlier than expected
* Ask questions on anything you don’t understand 100%

# Thank you!!!
