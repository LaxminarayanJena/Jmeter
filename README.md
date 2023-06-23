# Jmeter
![jmeter](https://user-images.githubusercontent.com/24494133/42121906-0ef6e378-7c56-11e8-80ef-b28dc22c618a.png)



1)sampler-http,ftp,jdbc request,,beanshell sampler,debug sampler</br>
2)logic controller-if,loop,while,random,recording,simple</br>
3) assertions-response,size,xpath,duration,beanshell</br>
4)timer-constant,gaussian randome timer</br>
5) preprocessor-regex user parameter,jdbc ,html link,,beanshell
6)postprocessor-json extractor,regular expression,beanshell,xpath extractor</br>
7)config-csv data config,http cookie manager,http header manager</br>
8) listener-view results table,tree,sumamry,perfmon metrics collector</br>
</br>
#### Execution flow of different elements
config element -preprocessor- timers-samplers-post processors-assertions-listeners

#### APM Tools
APPDynamics,Dynatrace,New Relic,

```
Think Time- represents the delay between consecutive requests within a single user session.
Pacing - controls the rate at which virtual users are executed in a test plan.
Ramp-Up Time- determines how quickly new threads are started in a test.
Delay- introduces a pause before starting a test or a specific request.
```

Application ,server,browser.mobile,avalaibility monitoring
web transaction time, apdex score,throughput ,transaction ,error rate

4 servers 
apdex,resp time,throughput,error rate,cpu usage,memory
```
Go into JMeter’s bin folder
Enter following command, jmeter -n –t test.jmx -l testresults.jtl
-n: It specifies JMeter is to run in non-gui mode
-t: Name of JMX file that contains the Test Plan
-l: Name of JTL(JMeter text logs) file to log results
```

#### Distrubuted Testing
```
master - slave1 
         slave2  -  your site 
         slave 3 
 
 pre config -master and slave should have same jmeter version
             No firewall ,antivirus blocking
             system should be as similar as possible-same os,directory tree etc
             otherwise connection error
 
 Slave machine configuration
    1)bin->jmeter.properties- 
                server.rmi.ssl.disable=true 
    2) start jmeter server    (copy the ip address)       
  
  Master machine configuration
    1)bin->jmeter.properties- 
                server.rmi.ssl.disable=true 
    2)Remote_hosts=paste the slave ip address  192.168.1.0,192.168.1.12
    3)Restart jmeter
    Run-Remote Start all
    See the result in master listener
    
    
 ```
  #### Load,Stress,Spike Endurance Testing              
 ```
load testing -100 users
stress testing  -150 users to find breaking point
spike testing- sudden increase tatkal -irctc
endurance testing-8 hrs ,1 day testing -issues related to memory leaks
jp@gc-Ultimate Thread Group
download jmeter plugin manager and put it in lib/ext directory
install custom thread group
jp@gc Ultimate Thread group
 ```
![spike testing](https://user-images.githubusercontent.com/24494133/89702423-ce543600-d95e-11ea-81df-6680702459c4.PNG)
