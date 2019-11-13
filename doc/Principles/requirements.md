# Requirements 
## Introduction 
### Type
- Functional  
    Descibe what does the system do
- Non-functional
    - Usaibility
    - Performance
    - Scalibility
    - Reliablity
    - Complexity
    - Testablily
    - ...
- Design constraints  
- Environmental constraints  
- Preferences  

### Kruchten's 4+1 Model
- Logical View  
    It focuses mostly on achieving the functional requirements of a system. The context is the services that should be provided to end users.  
    Tool: Class diagram  
- Process view  
    It focuses on non-functional requirements which specified desired quality, i.e. performance and availibility or the order of execution.
    Tool: Sequence Diagram, activity diagram
- Development View  
    It focuses on programming languages, libraries, toolsets. Besides code it also works on schduling, budgets, work assignments and project management.  
- Physical View  
    Tool: deployment diagram  
- Scenario
    It describes the sequences of interactions that how objects and processes interact.  
### Properties
- Complete  
    no information missed  
- Consistent  
    no controdictary requiremnts  
- Precise  
- Concise  

### Process
- Elicitation
- Analysis  
    with customer, which are harder to achieve or not possible, etc.  
- Reification  
    make requirement concrete. i.e. User story, use cases  
- Validation  
    with customer  

### Example - Validating Requirements
Especially the non-functional requirement need quantitized descriptions.
- Performance
    - Time
        - Reponsetime
        - Throughput
            - Peak
            - Off-peak
    - Space
        - Memory
        - Disk

---
## User stories  
Takes about two weeks  
- Role-Goal-Benefit  
    role can be non-human  
- Limitations of feature  
- Definition of Done  
- Engineering Tasks  
- Effort estimate  
    to think about the value of a feature, wheather it is worthy to do it  

### User Story Guideline Invest
- Independent user stories  
- Negotiable  
    extra feature might come or more detail
- Valueable 
    the store should provide value to the product. If the requirement changes, some feature might not be needed. Then it doesn't make any sense to develop this abandoned feature in the user stories  
- Estimatable  
    break feature into smaller and estimatable features  
- Small  
- Testable  


### User Story Example  
- Role-Goal-Benefit
    As a __professor__, I want to __create repositories__ so __students can work__
- Limitation of feature  
    Need: repositoy names, students IDs
- Definition of Done  
    - runabe as single command
    - automated test cases
    - programmatically verifiable
- Engineering Task  
    - Should use github manager  
- 1.5 Units (i.e. Days)

---
## Decomposing user stories  
Feature -> user story -> 

Role: Player  
Goal: Move Mario
Benefit: Dodge/attack enemy
Limitations: Keyboard input  
Notes: Use existing class: level  
Cost:  
    +1 keycontrol   
    +1 heandling movement  
    +1 collisions  

Definition of Done:  
    Key input controls Mario's movement  
    Mario is able to move through the level  
    when Mario ~~attack/hits~~ enemy, one of the should be ~~hurt~~  
New DoD
    Collisions between Mario and enemies shold be hits  

**INVEST**
I x  
N v  
V v  
E v  
S x  
T v  

### Procedure of decomposition
- Find Entities  
**Key** input controls **Mario's** movement  
**Mario** is able to move through the **level**
Collisions between **Mario** and **enemies** shold be hits  
-> **Enenmy** and **Mario** are **Figures** within **Level**  
- Link entities  
    Mario, Enemy -|> Figure <- Level <- Key  
Bind Actions
    Key input **controls** Mario's movement  
    Mario is able to **move** through the level
    **Collisions** between Mario and enemies shold be **hits**  
    Mario(collide), Enemy -- Figure(move,hit) -- Level(input,update) -- Key(Keypress)  

Prototype
    Key input **controls** Mario's movement  
    Mario is able to **move** through the level
    **Collisions** between Mario and enemies shold be **hits**  
    Mario(~~collide~~), Enemy -|> Figure(move,hit,collide) <- Level(input,update) <- Key(Keypress)
Formalize  
    Using UML class diagram  
Implementation