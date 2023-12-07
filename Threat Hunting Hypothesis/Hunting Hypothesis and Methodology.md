# Hunting Hypothesis and Methodology

Every hunt begins by defininf a hypothesis. It consists of the following: 
- identify the specific behavior we want to hunt for
- understand the attack technique behind it
- identify what data (and from which source) we need to detect it

To achieve this, there is a 5-step process: 
1. Pick a tactic and technique
2. Identify associated procedure(s)
3. Perform an attack simulation
4. Identify evidence to collect
5. Set scope

### 1. Pick a tactic and technique
Review attack sources and pick a technique. 
Utilize the MITRE ATT&CK framework. 

Example: selecting technique T1502 - Parent PID Spoofing under "Privilege Escalation" 
https://attack.mitre.org/techniques/T1134/004/

### 2. Identify Associated Procedure(s)
ATT&CK will provide procedures for the technique. 

Perform research to identify all implementations of the technique and understand the procedures, including their prerquisites, requirements, and outcome if succesfully executed. 

### 3. Perform an Attack Simulation
This step replicates the procedure(s) of the technique. 
During the replication process, you can observe what data and logs are generated, and in the next step, build your detection based on the identified behaviors. 

### 4. Identify Evidence to Collect
Once executed in our controlled environment, we should start investigating places that may contain artifacts of interest; this could be on-disk, in-memory, network traffic, registry, etc. 

The goal of this step is to identify behaviors we can use to detect that activity in the future. 

Some of the things to look for are:
- deviations from baselines
- attempts to appear normal (e.g., svchost.exe running from user directory)
- unexpected encryption
- odd frequency of occurrence (e.g, too many connections oor user activity at an abnormal time)

### 5. Set Scope
Now that we know everything about the technique and its procedure(s) and having identified behaviors after the simulation, we are almost ready to begin proving/disproving our hypothesis of whether a specific activity has occurred or not. 

Main things that should be defined in the scope are: 
- Hunt Duration
- What data and where to collect from

Usually the duration of a hunt is at least a week. 

In some hunts, you may want to focus only on Business-Critical Systems, while on others only on certain data sources. 

For example, PPID Spoofing, defined as: 
- Time: 1 week
- Collection: all windows devics sending Event Tracing for Windows (ETW) logs. 