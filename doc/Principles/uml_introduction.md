# UML

## Component Diagram  
It is about high-level structure.  
Components are defined as independnet, encapsulated units within a system.

- Identify Main objects
- Relevant libraries  
  If the third party library is used, remember to denote it.
- Relationship

## Package Diagram  
See how class interacts.
Package gourps number of classes together based on dada, usertasks classes, functionalities  

## Deployment Diagram
Seperate libraries, Executable, installer, configuration files, other different pieces  
Artifact: the result of software development, or, in short, executable, installer, libraries, data   
- Specification diagram  
    it gives an overview of artifacts and deployment targets, without referencing specific details like machine names. It focuses on a general overview of your deployment rather than the specifics.
- Instance level diagram  
    it is a much more specific approach, which can map a specific artifact to a specific deployment target. In particular, the instance level diagram can identify specific machines and hardware devices. Most commonly, this approach is used to highlight the differences in deployments among development, staging and release builds.  
**elements in diagram:**: Artifacts, libraries, main components, Machines, Devices, OS, execution environment...  

## Activaty Diagram  
It captures dynamic behavior of system to know how to control fron activity to another.  i.e. Concurrency 
**Partitions** divide activities up into different categories, such as where it occurs, or the user role involved. For example, all of video game activities concerning level can be grouped in one partrition, and all of the player activities could be grouped in another partrition.  