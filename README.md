# recipe-app-api

Error message: 
                       
 > [6/6] RUN python -m venv /py &&     /py/bin/pip install --upgrade pip &&     /py/bin/pip install -r /tmp/requirements.txt &&     /py/bin/pip install psycopg2-binary &&    apk add --update --no-cache postgresql-client &&     apk add --update --no-cache --virtual .tmp-build-deps        build-base postgresql-dev musl-dev &&    if [ true = "true" ];         then /py/bin/pip install -r /tmp/requirements.dev.txt;     fi &&     rm -rf /tmp &&     apk del .tmp-build-deps &&     adduser         --disabled-password         --no-create-home         django-user:                                                                                                                              
#10 5.637 Requirement already satisfied: pip in /py/lib/python3.9/site-packages (21.2.4)
#10 7.357 Collecting pip
#10 10.36   Downloading pip-23.1.2-py3-none-any.whl (2.1 MB)
#10 21.97 Installing collected packages: pip
#10 21.97   Attempting uninstall: pip
#10 21.97     Found existing installation: pip 21.2.4
#10 22.12     Uninstalling pip-21.2.4:
#10 22.13       Successfully uninstalled pip-21.2.4
#10 23.82 Successfully installed pip-23.1.2
#10 28.87 Collecting Django<3.3,>=3.2.4 (from -r /tmp/requirements.txt (line 1))
#10 31.85   Downloading Django-3.2.19-py3-none-any.whl (7.9 MB)
#10 74.03      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 7.9/7.9 MB 187.3 kB/s eta 0:00:00
#10 74.94 Collecting djangorestframework<3.13,>=3.12.4 (from -r /tmp/requirements.txt (line 2))
#10 75.40   Downloading djangorestframework-3.12.4-py3-none-any.whl (957 kB)
#10 80.11      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 957.7/957.7 kB 200.0 kB/s eta 0:00:00
#10 81.25 Collecting psycopg2-binary<2.8.0,>=2.7.5 (from -r /tmp/requirements.txt (line 3))
#10 81.68   Downloading psycopg2-binary-2.7.7.tar.gz (428 kB)
#10 83.78      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 428.8/428.8 kB 199.3 kB/s eta 0:00:00
#10 83.89   Installing build dependencies: started
#10 97.41   Installing build dependencies: finished with status 'done'
#10 97.41   Getting requirements to build wheel: started
#10 97.68   Getting requirements to build wheel: finished with status 'error'
#10 97.69   error: subprocess-exited-with-error
#10 97.69   
#10 97.69   × Getting requirements to build wheel did not run successfully.
#10 97.69   │ exit code: 1
#10 97.69   ╰─> [47 lines of output]
#10 97.69       /tmp/pip-build-env-gjxqy0vu/overlay/lib/python3.9/site-packages/setuptools/config/setupcfg.py:293: _DeprecatedConfig: Deprecated config in `setup.cfg`
#10 97.69       !!
#10 97.69       
#10 97.69               ********************************************************************************
#10 97.69               The license_file parameter is deprecated, use license_files instead.
#10 97.69       
#10 97.69               By 2023-Oct-30, you need to update your project and remove deprecated calls
#10 97.69               or your builds will no longer be supported.
#10 97.69       
#10 97.69               See https://setuptools.pypa.io/en/latest/userguide/declarative_config.html for details.
#10 97.69               ********************************************************************************
#10 97.69       
#10 97.69       !!
#10 97.69         parsed = self.parsers.get(option_name, lambda x: x)(value)
#10 97.69       running egg_info
#10 97.69       writing psycopg2_binary.egg-info/PKG-INFO
#10 97.69       writing dependency_links to psycopg2_binary.egg-info/dependency_links.txt
#10 97.69       writing top-level names to psycopg2_binary.egg-info/top_level.txt
#10 97.69       /tmp/pip-build-env-gjxqy0vu/overlay/lib/python3.9/site-packages/setuptools/command/sdist.py:117: SetuptoolsDeprecationWarning: `build_py` command does not inherit from setuptools' `build_py`.
#10 97.69       !!
#10 97.69       
#10 97.69               ********************************************************************************
#10 97.69               Custom 'build_py' does not implement 'get_data_files_without_manifest'.
#10 97.69               Please extend command classes from setuptools instead of distutils.
#10 97.69       
#10 97.69               See https://peps.python.org/pep-0632/ for details.
#10 97.69               ********************************************************************************
#10 97.69       
#10 97.69       !!
#10 97.69         self._add_data_files(self._safe_data_files(build_py))
#10 97.69       
#10 97.69       Error: pg_config executable not found.
#10 97.69       
#10 97.69       pg_config is required to build psycopg2 from source.  Please add the directory
#10 97.69       containing pg_config to the $PATH or specify the full executable path with the
#10 97.69       option:
#10 97.69       
#10 97.69           python setup.py build_ext --pg-config /path/to/pg_config build ...
#10 97.69       
#10 97.69       or with the pg_config option in 'setup.cfg'.
#10 97.69       
#10 97.69       If you prefer to avoid building psycopg2 from source, please install the PyPI
#10 97.69       'psycopg2-binary' package instead.
#10 97.69       
#10 97.69       For further information please check the 'doc/src/install.rst' file (also at
#10 97.69       <http://initd.org/psycopg/docs/install.html>).
#10 97.69       
#10 97.69       [end of output]
#10 97.69   
#10 97.69   note: This error originates from a subprocess, and is likely not a problem with pip.
#10 97.69 error: subprocess-exited-with-error
#10 97.69 
#10 97.69 × Getting requirements to build wheel did not run successfully.
#10 97.69 │ exit code: 1
#10 97.69 ╰─> See above for output.
#10 97.69 
#10 97.69 note: This error originates from a subprocess, and is likely not a problem with pip.
------
executor failed running [/bin/sh -c python -m venv /py &&     /py/bin/pip install --upgrade pip &&     /py/bin/pip install -r /tmp/requirements.txt &&     /py/bin/pip install psycopg2-binary &&    apk add --update --no-cache postgresql-client &&     apk add --update --no-cache --virtual .tmp-build-deps        build-base postgresql-dev musl-dev &&    if [ $DEV = "true" ];         then /py/bin/pip install -r /tmp/requirements.dev.txt;     fi &&     rm -rf /tmp &&     apk del .tmp-build-deps &&     adduser         --disabled-password         --no-create-home         django-user]: exit code: 1
ERROR: Service 'app' failed to build : Build failed
