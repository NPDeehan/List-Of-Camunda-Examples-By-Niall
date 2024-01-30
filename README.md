# List of My Camunda Platform 7 Examples
 This is a list showing the most useful of the examples for Camunda Plaform 7 that I've created. 
 
⚠ *You should be aware that if you're using Camunda Platorm 8 a lot of what I demonstrate here won't apply* ⚠

 They aim to show common solutions and demonstrate Interesting patterners.


## Dynamically Calling a DMN table form BPMN
If you have trouble picking a movie to watch on netflix and you really would love to know who a BPMN process can dynamically call a DMN table - this is the project for you. Why not create a pull request with your movie recommendation? 

[Source Code Here](https://github.com/NPDeehan/Dynamic-DMN-Example)

![Dynamic-DMN](https://raw.githubusercontent.com/NPDeehan/Dynamic-DMN-Example/main/images/DMNGermany.png)

## Saga Pattern using Camunda & BPMN
This is an example of how to model the Saga Pattern by taking a distributed group of micro services and have them orchestrated asynchronously using Camunda and BPMN. 

[Source Code Here](https://github.com/NPDeehan/CamundaSagaPatternExample)

![Saga Pattern](https://raw.githubusercontent.com/NPDeehan/CamundaSagaPatternExample/main/Models/BookHolidaySagaPatternV2.png)

## Generic Error and returned

 An example of throwing a BPMN from any point in the process and returning back to that point after the problem has been resolved.

[Source Code Here](https://github.com/NPDeehan/GenericErrorAndReturn)

 ![Error-Return-Process](https://raw.githubusercontent.com/NPDeehan/GenericErrorAndReturn/master/src/main/resources/genericErrorAndReturn.png)

## Idempotent Camunda Process

A Pattern for creating process that will only start one instance per request. So that if an external system sends multiple identical requests it will not start any new processes if one has been successfully started.

[Source Code Here](https://github.com/NPDeehan/idempotent-process-example)

![idempotent-camunda-process](https://raw.githubusercontent.com/NPDeehan/idempotent-process-example/master/img/complete-process.png)

## Multi-instance Messaging between processes.
This demonstrates a way in which you can asynchronously start lots of instances of another process and be able to wait for each to return with results.

[Source Code Here](https://github.com/NPDeehan/multi-instance-messages)

![message-between-process](https://raw.githubusercontent.com/NPDeehan/multi-instance-messages/master/src/main/resources/image/MessageFlow.png)

## Compensating Multi-Instance Sub processes
When you start lots of sub processes from a parent and then decided you want to shut things down, you need to ``undo`` or ``compensate`` what has already been completed and cancel the  instances that have not yet done anything. This examples show s a nice way of doing that.

[Source Code Here](https://github.com/NPDeehan/CompensateMulti-InstanceSubprocessExample)

![compensate](https://raw.githubusercontent.com/NPDeehan/CompensateMulti-InstanceSubprocessExample/master/screenshots/SubProcessCockpit.png)

## Suspend a process
An example of how a process can be made to suspend itself under a specific condition

[Full Source Code Here](https://github.com/NPDeehan/SusupendInstanceExample)
```Java

        execution.getProcessEngineServices()
                .getRuntimeService()
                .updateProcessInstanceSuspensionState()
                .byProcessInstanceId(execution.getProcessInstanceId())
                .suspend();

```
