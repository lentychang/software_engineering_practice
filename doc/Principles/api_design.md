# API Design Process
## Before design
1. Whate is the goal?
    - Languages
    - Protocals
    - Plateform
    - Formats
2. Who is the customer?
    - Versioning
    - Licensing
    - Authentication


## Process
1. Start with short specification
2. Solicit feedback  
    Check if the specification fit customers' need  
3. Concrte Prototype  
    Create three clients API for finding a good api design  
4. Document  
    How API is use in specific scenario  
5. Iterate back and forth  


## Usibility  
    how long it taskes for users to learn to us API  
    how many actions do they need for a task  
    error rate

    - Prioritize the important part of API  
        Easy for developer to understand and find the corresponding methods without going into documentation line by line  
    - Make it hard to misuse API  
    - i.e.  
        instead of using string, use Enumeration.
        **Bad**: item.sort("clearance");
        **Good**: items.sort(Filter.CLEARANCE);
    - More descriptive name of method name  
        **Bad**: store.get(pid:string)  
        **Good**: Store.getProduct(pid:string)   
    - Adequate abstration to map the level that user thinks about the task
        What method, varialbe should we export to or hide from API users  
        **Bad**: store.getDepartemnt(did:string).getShelf(sid:string).getProduct(pid:string)  
        **Good**: Store.getProduct(pid:string)  
        API user don't care about department, shelf, better to hide these operations    
    - return type
        **Bad**: store.getProduct(pid:string):any
        **Good**: store.getProduct(pid:string):Product
    - Feedback
        let users know the misuse API  
        item.sort("clearamce"), show error: unknown type
