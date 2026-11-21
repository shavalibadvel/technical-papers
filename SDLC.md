# SDLC - Software Development Life Cycle

SDLC is the process followed by the software industry to complete a project/product .

                              Requirements
                                   |
                                   |
                                 Design  
                                   |
                                   |
                              Implementation
                                   |
                                   |
                                 Testing
                                   |
                                   |
                               Deployement
  
These are the five phases that will be followed by the every software development life-cycle models based on this some models come.

They are 
- Waterfall model
- Spiral Model
- V-model

lets start with water fall model
## 1.Waterfall model
Is is the basic and old sdlc model used previously where one phase depends on another phase without it there is no output.

    Requirements
           |
    _______|_________                    
                    |
                    |
                SoftwareDesign 
                        |
                ________|______ 
                              |
                              |
                        Implementation
                               |
                        _______|________
                                        |
                                        |
                                      Testing
                                         |
                                    _____|_____
                                              |
                                              |
                                          Deployement
                                               | 
                                          _____|_______
                                                    |
                                                    | 
                                                Maintainance
here each phase depends directly on upper phase to give output
normally these models used for long term project/project

Advantages: 
1.quality of product is good
2.requirment changes not allowed like once started it will not have no modifications in middle
3.initial investment is less , like each phase has different team.
4. prefer for small projects like no changes needed

Disadvantages:
1. requirement changes is not allowed.
2. if there is mistake continues to next phases
3. total investment is more, like time takes to rework everythig whenever something needs to modify
4. testing is only after coding.

## 2.Spiral model
it helps the Disadvantages of Waterfall model to this models
this model have 4 parts
  - palnning - requirement analysis
  - risk analysis
  - engineering and ecexution
  - evaluation

it will go like cycles , first cycle gives prototype and tests and followed the next requirements after cycle.like versions with new features.
it is used by most of the product based companies uses

1. It is iterative model
2. Requirements can be added again
3. whenever there is dependency on previous modules we use spiral model
4. it will give new software will be given to customer for every cycle

Advantages:
  - testing done at every cycle
  - customer can use the software for every model changes
  - requirement changes allowed after every cycle.

Disadvantages:
 - requirements not allowed in middle of cycle
 - every cycle looks waterfall model
 - there is no testing in planning and design phase

 ## 3. V-Model
 It is looks like V shape ,one side is verification,another side is validation
here we do testing in every phase.

  - BRS/URS/CRS(Customer requirements stage) uses - User acceptance Testing- document testing
  - SRS(system requirement stage) - system testing by Black box testing technique
  - HLD && LLD - Integration Testing by white box 
  - Coding - Unit Testing by white box

  review ,walkthrough,inspections in everyphase= static testing
  unit,integration,remaining testings = dynamic testing

  Advantages:
  testing is done at every phase

  Disadvantages:
  more documentation
  more initital investment
