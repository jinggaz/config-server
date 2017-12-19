# config-server
Steps need to do.

    Create directory name "backup" under "Desktop"

    Create a file "config-server-client.properties" in "backup" directory.

    Open a GitBash or commnad prompt and go to "backup" directory

    Execute "git init"

    Execute "git add ."

    Execute "git commit -m "init commit"

    Execute setp 4-7 in "Hystrix-Central-Config" and "Hystrix-Client" project also.

**Example of config-server-client.properties" in "backup" directory.

msg=This message is from Central Config

#Fallback option true for "Test1" circuit

hystrix.command.Test1.fallback.enabled=true
hystrix.command.Test1.circuitBreaker.errorThresholdPercentage=50
hystrix.command.Test1.circuitBreaker.requestVolumeThreshold=4
hystrix.command.Test1.circuitBreaker.sleepWindowInMilliseconds=60000
hystrix.command.Test1.metrics.rollingStats.timeInMilliseconds=60000
hystrix.command.Test1.execution.isolation.thread.timeoutInMilliseconds=5000


#Fallback option false for "Test2" circuit

hystrix.command.Test2.fallback.enabled=false
hystrix.command.Test2.circuitBreaker.errorThresholdPercentage=50
hystrix.command.Test2.circuitBreaker.requestVolumeThreshold=4
hystrix.command.Test2.circuitBreaker.sleepWindowInMilliseconds=60000
hystrix.command.Test2.metrics.rollingStats.timeInMilliseconds=10000
hystrix.command.Test2.execution.isolation.thread.timeoutInMilliseconds=5000
