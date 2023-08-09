# Software Development Notes

## General

<details>
    <summary>
        What is Agile in regards to software development
    </summary>
    <br>
    <blockquote>
        <p>
            <h5>
                <b>Summary:</b>
            </h5>
            Agile is a structured and iterative approach to project management and product development. It recognizes the volatility of product development, and provides a methodology for self-organizing teams to respond to change without going off the rails.
        </p>
        <br>
        <p>
            <h5>
                <b>More Information:</b>
            </h5>
            <h6>
                [<a href="https://www.atlassian.com/agile/kanban/kanban-vs-scrum">Atlassian</a>]
            </h6>
        </p>
        <p>
            When it comes to implementing <b>Agile</b> and <b>DevOps</b>, <b>kanban</b> and <b>scrum</b> provide different ways to do so.
        </P>
        <p>
            It's easy to point out the differences between scrum practices and kanban practices, but that's just at the <b>surface level</b>. 
            While the practices differ, the principles are largely the same. Both frameworks will help you build better products (and services) with fewer headaches. 
        </p>
        <p>
            <b>Agile</b> is a structured and iterative approach to project management and product development. It recognizes the volatility of product development, and provides a methodology for self-organizing teams to respond to change without going off the rails. 
        </p>
    </blockquote>
</details>

<details>
    <summary>
        What is Kanban
    </summary>
    <br>
    <blockquote>
        <p>
            <b>Kanban</b> is all about visualizing your work, limiting work in progress, and maximizing efficiency (or flow). Kanban teams focus on <b>reducing the time</b> a project takes (or user story) from start to finish. They do this by using a kanban board and continuously improving their flow of work. 
        </p>
        <p>
            Kanban helps visualize your work, limit work-in-progress (WIP) and quickly move work from "Doing" to "Done.".
            Kanban is great for teams that have lots of incoming requests that vary in priority and size. Whereas scrum processes require high control over what is in scope, kanban let’s you go with the flow. Let’s take a look at the same five considerations to help you decide.  
        </p>
        <p>
            <b>
                Kanban cadence
            </b>
            Kanban is based on a continuous workflow structure that keeps teams nimble and ready to adapt to changing priorities. Work items—represented by cards— are organized on a kanban board where they flow from one stage of the workflow(column) to the next. Common workflow stages are To Do, In Progress, In Review, Blocked, and Done. But that’s boring.
            The best part of kanban is making custom columns for how your team works. My team ships content, so our columns(simplified) go from Backlog, to Prioritized, to Outlines Ready, to Writing, Designing, Technical Review, and Shipped. Our board helped us learn that we ship about one piece of content per week, and where our bottlenecks are (looking at the Technical Review!).
        </p>
        <p>
            <b>
                Release methodology
            </b>
            In kanban, updates are released whenever they are ready, without a regular schedule or predetermined due dates.
            In theory, kanban does not prescribe a fixed time to deliver a task. If the task gets completed earlier (or later), it can be released as needed without having to wait for a release milestone like sprint review. 
        </p>
        <p>
            <b>
                Kanban roles
            </b>
            The whole team owns the kanban board. Some teams enlist an agile coach but, unlike scrum, there is no single “kanban master” who keeps everything running smoothly. It’s the collective responsibility of the entire team to collaborate on and deliver the tasks on the board.
        </p>
        <p>
            <b>
                Key metrics
            </b>
            Lead time and cycle time are important metrics for kanban teams. The deal with the average amount of time that it takes for a task to move from start to finish. Improving cycle times indicates the success of kanban teams.
            The Cumulative Flow Diagram (CFD) is another analytical tool used by kanban teams to understand the number of work items in each state. CFDs help identify specific bottlenecks that need to be resolved for better throughput.
            Another way to deal with bottlenecks is through Work In Progress (WIP) limits. A WIP limit caps the number of cards that can be in any one column at one time. When you reach your WIP limit, a tool like Jira Software caps that column, and the team swarms on those items to move them forward.
        </p>
        <p>
            <b>
                Change philosophy
            </b>
            A kanban workflow can change at any time. New work items can get added to the backlog and existing cards can get blocked or removed based on prioritization. Also, if the team capacity changes, WIP limit can be recalibrated and work items adjusted accordingly. It’s all about being flexible in kanban.
        </p>
    </blockquote>
</details>

<details>
    <summary>
        What is Scrum
    </summary>
    <br>
    <blockquote>
        <p>
            <b>Scrum</b> teams commit to completing an increment of work, which is potentially shippable, through set intervals called sprints. Their goal is to create learning loops to quickly gather and integrate customer feedback. Scrum teams <b>adopt specific roles, create special artifacts, and hold regular ceremonies</b> to keep things moving forward. Scrum is best defined in <b>The Scrum Guide</b>.
        </p>
        <p>
            With scrum, your team promises to ship some valuable increment of work by the end of each sprint. Scrum is built on empiricism, focusing on small increments of work that will help you learn from your customers and better inform what you do next. Here's how it breaks down: 
        </p>
        <p>
            <b>
                Scrum cadence:
            </b>
            Scrum moves fast, with sprints that usually last between one to four weeks, which have clear start and finish dates. The short time frame forces complex tasks to be split into smaller stories and help your team learn quickly. A key question is this: Can your team ship useable code that fast?
            Sprints are punctuated by sprint planning, sprint review, and retrospective meetings and peppered with daily scrum (standup) meetings. These scrum ceremonies are lightweight and run on a continuous basis.
        </p>
        <p>
            <b>
                Scrum roles:
            </b>
            Scrum has three clearly defined roles.
            <ul>
                <li>
                    The product owner advocates for the customer, manages the product backlog, and helps prioritize the work done by the development team.
                </li>
                <li>
                    The scrum master helps the team stay grounded in the scrum principles.
                </li>
                <li>
                    The development team chooses the work to be done, delivers increments, and demonstrates collective accountability.
                </li>
            </ul>  
            Who manages the scrum team? Well, nobody. Scrum teams are self-organizing and everyone is equal, despite having different responsibilities. The team is united by the goal of shipping value to customers.
        </p>
        <p>
            <b>
                Common metrics:
            </b>
            Scrum metrics are data points scrum teams can use to improve efficiency and effectiveness. They can inform decision-making and help teams become more efficient in planning and execution. During the sprint planning phase, teams can use metrics such as sprint goals, team velocity, team capacity, and type of work. During stand-ups, teams can also benefit from measuring progress towards sprint goals, reviewing a sprint burndown, understanding workload distribution, and more.
        </p>
        <p>
            <b>
                Change philosophy:
            </b>
            Teams strive to understand how much they can accomplish within their sprint time boundaries. They commit to its delivery within a sprint. However, scrum teams can receive customer feedback that encourages them to pivot and change the sprint to deliver the most customer value. During the sprint retrospective, scrum teams should discuss how to limit change in the future, as changes put the potentially shippable increment at risk. If a team frequently changes scope mid-sprint, it may signify work was selected that isn’t adequately understood. It could also mean the team has operational/unplannable work that interferes with the plan.
        </p>
    </blockquote>
</details>

<details>
    <summary>
        Kanban VS Scrum Comparison
    </summary>
    <br>
    <blockquote>
    <p>
        <ul>
            <li>
                Kanban is continuous, fluid and visualized process whereas Scrum is short and structured, where work is shipped during fixed intervals known as sprints.
            </li>
            <li>
                Kanban is less structured compared to other frameworks like Scrum.
            </li>
            <li>
                Kanban is more visualized way of managing the development process
            </li>
            <li>
                Kanban has fewer meetings and formal roles compared to other frameworks like Scrum.
            </li>
            <li>
                Scrum is suggested for larger team for better management, while Kanban is suggested for smalled developer teams.
            </li>
        </ul>
    </p>
    </blockquote>
</details>

## Programming

<details>
    <summary>
        What are static typed(or simply typed) programming languages?
    </summary>
    <br>
    <blockquote>
        <p>
            In static typed languages the variable type is know at compilation time instead of run time.
        </p>
        <p>
            Some examples of static programming languages:
        </p>
        <ul>
            <li>
                C
            </li>
            <li>
                C++
            </li>
            <li>
                Java
            </li>
        </ul>
    </blockquote>
</details>

<details>
    <summary>
        Expressions and Statements
    </summary>
    <br>
    <blockquote>
        <p>
            Expressions
        </p>
        <p>
            An expression is anything that results in a value(even if the value is None). Basically, any sequence of literals so, you can say that a string, integer, list, etc. are all expressions.
        </p>
        <p>
            Statements
        </p>
        <p>
            Statements are instructions executed by the interpreter like variable assignments, for loops and conditionals (if-else).
        </p>
    </blockquote>
</details>

<details>
    <summary>
        What is Object Oriented Programming?
    </summary>
    <br>
    <blockquote>
        <p>
            Object-Oriented Programming (OOP) is a programming paradigm in computer science that relies on the concept of classes and objects.It is used to structure a software program into simple, reusable pieces of code blueprints (usually called classes), which are used to create individual instances of objects. There are many object-oriented programming languages, including JavaScript, C++, Java, and Python.
        </p>
        <p>
            A class is an abstract blueprint that creates more specific, concrete objects. Classes often represent broad categories, like Car or Dog that share attributes. These classes define what attributes an instance of this type will have, like color, but not the value of those attributes for a specific object.
        </p>
        <p>
            Classes can also contain functions called methods that are available only to objects of that type. These functions are defined within the class and perform some action helpful to that specific object type.
        </p>
        <p>
            Class templates are used as a blueprint to create individual objects. These represent specific examples of the abstract class, like myCar or goldenRetriever. Each object can have unique values to the properties defined in the class.
        </p>
        <p>
            Benefits of OOP for software engineering
        </p>
        <p>
            <ul>
                <li>
                    OOP models complex things as reproducible, simple structures.
                </li>
                <li>
                    Reusable, OPP objects can be used across programs.
                </li>
                <li>
                    Polymorphism allows for class-specific behaviour.
                </li>
                <li>
                    Easier to debug, classes often contain all applicable information to them.
                </li>
                <li>
                    Securely protects sensitive information through encapsulation.
                </li>
            </ul>
        </p>
        <details>
            <summary>
                Source
            </summary>
            <blockquote>
                <a href="https://www.educative.io/blog/object-oriented-programming">educative.io - Object Oriented Programming</a>
            </blockquote>
        </details>
    </blockquote>
</details>

<details>
    <summary>
        Object Oriented Programming - Classes
    </summary>
    <br>
    <blockquote>
        <p>
            In a nutshell, classes are essentially user-defined data types. Classes are where we create a blueprint for the structure of methods and attributes. Individual objects are instantiated from this blueprint.
        </p>    
        <p>
            Classes contain fields for attributes and methods for behaviors. In our Dog class example, attributes include name & birthday, while methods include bark() and updateAttendance().
        </p>
    </blockquote>
</details>

<details>
    <summary>
        Object Oriented Programming - Objects
    </summary>
    <br>
    <blockquote>
        <p>
            Objects are, unsurprisingly, a huge part of OOP! Objects are instances of a class created with specific data.
        </p>    
    </blockquote>
</details>

<details>
    <summary>
        Object Oriented Programming - Attributes
    </summary>
    <br>
    <blockquote>
        <p>
            Attributes are the information that is stored. Attributes are defined in the Class template. When objects are instantiated, individual objects contain data stored in the Attributes field.
        </p>    
        <p>
            The state of an object is defined by the data in the object’s attributes fields. For example, a puppy and a dog might be treated differently at a pet camp. The birthday could define the state of an object and allow the software to handle dogs of different ages differently.
        </p>
    </blockquote>
</details>

<details>
    <summary>
        Object Oriented Programming - Methods
    </summary>
    <br>
    <blockquote>
        <p>
            Methods represent behaviors. Methods perform actions; methods might return information about an object or update an object’s data. The method’s code is defined in the class definition.
        </p>    
        <p>
            When individual objects are instantiated, these objects can call the methods defined in the class. In the code snippet below, the bark method is defined in the Dog class, and the bark() method is called on the Rufus object.
        </p>
        <p>
           Methods often modify, update or delete data. Methods don’t have to update data though. For example, the bark() method doesn’t update any data because barking doesn’t modify any of the attributes of the Dog class: name or birthday. 
        </p>
        <p>
            The updateAttendance() method adds a day the Dog attended the pet-sitting camp. The attendance attribute is important to keep track of for billing Owners at the end of the month.
        </p>
        <p>
            Methods are how programmers promote reusability and keep functionality encapsulated inside an object. This reusability is a great benefit when debugging. If there’s an error, there’s only one place to find it and fix it instead of many.
        </p>
        <p>
            The underscore in _attendance denotes that the variable is protected and shouldn’t be modified directly. The updateAttendance() method changes _attendance.
        </p>
    </blockquote>
</details>

<details>
    <summary>
        Four Principles of OOP
    </summary>
    <br>
    <blockquote>
        <p>
            The four pillars of object-oriented programming are:
        </p>
        <ul>
            <li>
                <b>Inheritance:</b> child classes inherit data and behaviours from the parent class.
            </li>
            <li>
                <b>Encapsulation:</b> containing information in an object, exposing only selected information.
            </li>
            <li>
                <b>Abstraction:</b> only exposing high-level public methods for accessing an object.
            </li>
            <li>
                <b>Polymorphism:</b> many methods can do the same task.
            </li>
        </ul>
    </blockquote>
</details>

<details>
    <summary>
        Inheritance
    </summary>
    <br>
    <blockquote>
        <p>
            Inheritance allows classes to inherit features of other classes. Put another way, parent classes extend attributes and behaviors to child classes. Inheritance supports reusability.
        </p>
        <p>
            If basic attributes and behaviors are defined in a parent class, child classes can be created, extending the functionality of the parent class and adding additional attributes and behaviors.
        </p>
        <p>
            For example, herding dogs have the unique ability to herd animals. In other words, all herding dogs are dogs, but not all dogs are herding dogs. We represent this difference by creating a child class HerdingDog from the parent class Dog, and then adding the unique herd() behavior.
        </p>
        <p>
            The benefits of inheritance are programs can create a generic parent class and then create more specific child classes as needed. This simplifies programming because instead of recreating the structure of the Dog class multiple times, child classes automatically gain access to functionalities within their parent class.
        </p>
        <blockquote>
            <b>Note:</b> Parent classes are also known as superclasses or base classes. The child class can also be called a subclass, derived class, or extended class.
        </blockquote>
        <p>
            In JavaScript, inheritance is also known as prototyping. A prototype object is a template for another object to inherit properties and behaviors. There can be multiple prototype object templates, creating a prototype chain.
            This is the same concept as the parent/child inheritance. Inheritance is from parent to child. In our example, all three dogs can bark, but only Maisel and Fluffy can herd.
            The herd() method is defined in the child HerdingDog class, so the two objects, Maisel and Fluffy, instantiated from the HerdingDog class have access to the herd() method.
            Rufus is an object instantiated from the parent class Dog, so Rufus only has access to the bark() method.
        </p>
    </blockquote>
</details>