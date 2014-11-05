Deployment success tests
========================
These will render the string 'SUCCESS', without the quotes, when you browse to the site.

PythonDjangoSkipStatic
----------------------
Makes sure the user can opt out of django collect static files step.  In case we incorrectly guess it should be done, or if the user wants to handle the static collection.

PythonDjangoStatic
------------------
Makes sure that the django collect static step occurs for a django app.

PythonNoRootFiles
-----------------
Makes sure that the site is detected as Python, when no .py file is at the root (requirements.txt + runtime.txt with any ‘python’ triggers detection).

PythonRuntime27
---------------
Makes sure that a runtime.txt that specifies ‘python-2.7’ is deployed correctly.

PythonRuntime34
---------------
Makes sure that a runtime.txt that specifies ‘python-3.4’ is deployed correctly.

PythonRuntimeDefault
--------------------
Makes sure that the default of Python 2.7 is used when the optional runtime.txt doesn’t exist.

PythonSkip
----------
Makes sure that the user can disable all python specific steps during deployment.


Deployment failure tests
========================
These will fail to deploy.

PythonFailDeployPipError
------------------------
Makes sure that there is proper error propagation when pip install fails.

PythonFailDeployRuntimeInvalid
------------------------------
Makes sure that there is proper error when the version of python specified in runtime.txt is not supported/invalid.
