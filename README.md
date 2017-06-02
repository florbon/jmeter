# jmeter

Manage Apache JMeter (distributed) load tests.

<pre>

Prerequitites:
  - Docker & Docker Machine installed: https://docs.docker.com/machine/
  - A test plan definition .jmx file created with JMeter 3.2: http://jmeter.apache.org/

Usage:

jmeter run JMX MACHINE [REMOTE_HOST...]
  Run the given test in non-gui mode, locally or remote, generating
  a dashboard report.
  JMX             Path to the .jmx file.
  MACHINE         The docker-machine that should run the test.
  REMOTE_HOST...  Any number of host names or IP addresses of remote
                  slave servers to use for distributed testing.
                  If unset, the test is run locally.

jmeter server ACTION MACHINE
  Manage remote JMeter slave servers.
  ACTION   Either start, stop, or restart.
  MACHINE  The targeted docker-machine.

jmeter perfmon ACTION MACHINE
  Manage the PerfMon Server Agent on application servers.
  ACTION   Either start, stop, or restart.
  MACHINE  The targeted docker-machine.

jmeter help
  Display this message.

</pre>


