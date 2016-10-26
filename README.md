# OOAD-WEEK010 Homework
##Sequence Diagram

###Sequence Diagram1
Code
```
@startuml
participant User

User -> System: messsage
System -> User: messsage

@enduml
```
Diagram
<img src="https://github.com/pongsakorn194/OOAD-WEEK10/blob/master/Homework/Sequence%20Diagram01.png?raw=true ">

###Sequence Diagram2
Code
```
@startuml
participant User

User -> task: start
activate task

task -> User: callback
deactivate task

@enduml
```
Diagram
<img src="https://github.com/pongsakorn194/OOAD-WEEK10/blob/master/Homework/Sequence%20Diagram02.png?raw=true">

###Sequence Diagram3
Code
```
@startuml
skinparam sequenceArrowThickness 2
skinparam roundcorner 20
skinparam maxmessagesize 60
skinparam sequenceParticipant underline

actor User
participant "search" as A
participant "webbrowser" as B

User -> A: execute
activate A

A -> B: search
activate B

B --> A: result
deactivate B

A --> User: show
deactivate A

@enduml
```
Diagram
<img src="https://github.com/pongsakorn194/OOAD-WEEK10/blob/master/Homework/Sequence%20Diagram03.png?raw=true">

###Sequence Diagram4
Code
```
@startuml
skinparam sequenceArrowThickness 2
skinparam roundcorner 20
skinparam maxmessagesize 60
skinparam sequenceParticipant underline

actor User
participant "loginpage" as A
participant "logindatabase" as B
participant "usermain" as C

User -> A: insertuser&pass

A -> B: validateinformation

B -> C: success

C --> User: loginsuccessful

@enduml
```
Diagram
<img src="https://github.com/pongsakorn194/OOAD-WEEK10/blob/master/Homework/Sequence%20Diagram04.png?raw=true">

###Sequence Diagram5
Code
```
@startuml
skinparam sequenceArrowThickness 2
skinparam roundcorner 20
skinparam maxmessagesize 60
skinparam sequenceParticipant underline

actor patient
actor officer

box "Hospital Information" #LightBlue
	participant DATA
end box

patient -> officer: Patient registration
officer -> patient: Patient ID
patient --> officer: Patient information
officer --> DATA: create
DATA --> patient : The patient's hospital
@enduml
```
Diagram
<img src="https://github.com/pongsakorn194/OOAD-WEEK10/blob/master/Homework/Sequence%20Diagram05.png?raw=true">

