# Docker
## What you need to know 
* Atleast 3 months of programming experience & You should have built atlest 1 aaplication. So you should know concepts like __backend__, __frontend__, __API__ and __database__.
* Basic git commands like __cloning__, __commiting__, __pushing__ and __pulling__.
## In this section
### __What is Docker?__
    
    A platfrom for building, running and shipping applications in a consistant manner. So if your application works on your development machine it can run and function the same way other machines.
    
        If you have been developing software application for a while you've probably come across this situation where your application works on you development machinebut doesn't somewhere else can you think of three reasons, why?
        
        This can happen because of 3 reasons:
        1. One or more files are missing
        2. Software version mismatch   // If the target machine is running a different vresion of some software that your application needs. Let's say your application needs node version 14 but the target machine is running node version 9.
        3. Different configuration settings // The environment variables
__`Packages needed - Node 14, Mongo 14, App`__

If someone joins you team they don't have to spend their time in setting up a new machine to run your application they don't have to install and configure all these dependencies they simple tell docker to bring up your application and docker itself will automatically run these dependencies inside an isolated environment called a __container__. This isolated environment allows multiple applications use different versions of some software side by side. So, one application may user node version 14 another may use node version 9. Both these applications can run side by sidewithout messing with each other. So, this is how __docker__ allows us to consistently run an application on different machines.

```bash
    docker-compose up
```
And there is one more benefit, when we're done with one of the applications and don't want to work on it anymore we can remove the appliaction and all its dependencies in one go. 

As we work on different projects our development machine gets cluttered with so many libraries and tools that are used by different applications and after a while don't know if we can remove one ore more of these tools because we are always afraid that we would mess up with some application with docker we don't have to worry about this becauseeach application runs with its dependencies inside an isolated environment we can safely remove an application with all its dependencies to clean up our machine.

```bash
    docker-compose down --rmi all
```

### __Virtual Machine vs Containers__



### __Architecture of Docker__


### __Installing Docker__


### __Development Workflow__

