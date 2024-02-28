# nGrinder controller

## Script

## 




## error
1) Java Version 문제
```sh
2024-02-28 10:54:27,980 ERROR Script error - Error while initialize test runner
net.grinder.engine.common.EngineException: Error while initialize test runner
	at net.grinder.scriptengine.groovy.GroovyScriptEngine.<init>(GroovyScriptEngine.java:71)
	at net.grinder.scriptengine.groovy.GroovyScriptEngineService.createScriptEngine(GroovyScriptEngineService.java:87)
	at net.grinder.engine.process.ScriptEngineContainer.getScriptEngine(ScriptEngineContainer.java:105)
	at net.grinder.engine.process.GrinderProcess.run(GrinderProcess.java:345)
	at net.grinder.engine.process.WorkerProcessEntryPoint.run(WorkerProcessEntryPoint.java:87)
	at net.grinder.engine.process.WorkerProcessEntryPoint.main(WorkerProcessEntryPoint.java:60)
Caused by: org.codehaus.groovy.control.MultipleCompilationErrorsException: startup failed:
General error during conversion: Unsupported class file major version 61
```
SpringBoot를 사용하기 위해 Java17 설치가 문제였음.<br>
~/.zshrc 설정을 openjdk-11로 변경 후 작업 완료
