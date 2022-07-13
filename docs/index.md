# Getting started

**Daisi** [(app.daisi.io)](https://app.daisi.io) is a scientific Cloud Computing platform running Python serverless functions, named *Daisies*.  

With Daisi you can:  

* create web services, automate tasks, host apps… orders of magnitude easier and faster than traditional cloud platforms.  
* parallelize compute intensive workloads by scaling up instantly to thousands of processes on demand.  
* share your code and discover thousands of ready-to-call functions and apps !  

Daisi brings the power of cloud computing into the hands of every developer, scientist, engineer by automatically deploying and creating endpoints for any function of a Python code, which can
then be invoked seamlessly from any environment.  

Any regular Python code can be turned into a *Daisi* by simply registering its Github repository in the Daisi platform, with **no need to write any specific code**.

!!! note

    This project is under active development

## Quick start with the `#!python pydaisi` Python package

### Calling "Hello World !"  

1. Install pydaisi (**requires Python 3.8+**)

    ```python
    pip install --upgrade pydaisi
    ```

2. Call the "Print Hello" Daisi and invoke the ``hello()`` endpoint

    ```python
    import pydaisi as pyd

    greeting_daisi = pyd.Daisi("exampledaisies/Print Hello")
    greeting_daisi.hello(name = "Daisi user").value

    ```

Check the code of this Daisi on app.daisi.io: ["Print Hello"](https://app.daisi.io/daisies/c8907e10-f562-4c5f-a26d-ff37afd9de42/info).  
And browse [app.daisi.io](https://app.daisi.io) to more discover Daisies !

### What just happened ? Cloud Computing made easy !

We have instantiated a Daisi object and passed the name of a serverless function from the Daisi platform in argument.
This is how you can call any available Daisi. The pattern to call a Daisi is `#!python "username/daisiname"`, except if the Daisi is
public and its name is unique, in which case you can ommit `#!python "username"`.

A Daisi can have multiple endpoints. Endpoints are created automatically for every fuction
in the main script of your code. They are simply invoked as a method of the Daisi object, with
the method name being the name of the function. In this example, we have invoked the `#!python hello` endpoint
of the `#!python Print Hello` Daisi.  

With `#!python pydaisi` you can send and receive arbitrary Python objects, as if you were passing arguments
to a local function. No need to serialize / deserialize, `#!python pydaisi` handles it automatically.

Invoking a Daisi endpoint returns a `#!python DaisiExecution` object. The value returned can be simply
retrieved by querying its `#!python .value` attribute.

!!! note
    Public Daisies can be called without being authentified. Private Daisies shared within a team require authentication (see the [Authentication](1.authentication.md) section)

### Daisies can also be apps !

You can give a nice front end to your Daisies, and the platform currently supports Streamlit (more frameworks to come).
And convert your Daisi into a fully deployed app with an API for
computer access....

Check this Daisi: ["Print Hello App"](https://app.daisi.io/daisies/b8adce0f-5f3e-4885-953f-01ddcbb12e66/info)