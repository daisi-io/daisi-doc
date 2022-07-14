# Requirements

Daisi is a hosted Software-as-a-Service platform, so requirements to use it are minimal.

- To use the web UI, you should use the latest version of Chrome, Safari, or
  Firefox
- The PyDaisi client library Python version requirments are published on
  [its PyPI page](https://pypi.org/project/pydaisi/).
- All browser and client connections to the Daisi platform require HTTPS using
  TLS 1.2 (or higher)

# Limits

For now, we are providing limited free usage of the Daisi platform.

- Daisies run under CPython 3.8; this will be updated and other options provided
  from time to time
- Each Daisi function execution may use only a single CPU, though multipe
  executions may run simultaneously
- Each Daisi function execution may use up to 15 GB of memory, subject to
  platform limits; executions that exceed this may be terminated
- The free platform currently is allowed a total of 16 CPUs; executions may run
  more slowly until we increase this limit
- The free platform usage is currently limited to a total 64 GB; executions may
  run slowly or fail until we increase this limit
