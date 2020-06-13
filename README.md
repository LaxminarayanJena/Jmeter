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
