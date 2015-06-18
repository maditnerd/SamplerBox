SamplerBox
==========

Install on Windows (Mostly Portable)

A lot of dependencies can't be directly installed with pip on Windows (unfortunately).

I will assume you will generate your samplerBox inside **c:\virtualenv\samplerBox**

You can also skip using an virtualenv and install dependencies globally but you won't be able to install samplerBox everywhere easily!

** For advanced users only! download the premade version here **

[Generate a Virtual Environnement](#Generate a Virtual Environnement)
----
1. Install Python 2.7  
https://www.python.org/ftp/python/2.7/python-2.7.msi

2. Install virtualenv
~~~
c:\Python27\Scripts\pip.exe install virtualenv
~~~

3. Generate your virtualenv for samplerBox
~~~
c:\Python27\Scripts\virtualenv.exe c:\virtualenv\samplerBox\Python
~~~

4. Activate your virtualenv
~~~
c:\virtualenv\samplerBox\Python\
Scripts\activate
~~~

[Clone samplerBox](#Clone samplerBox)
----
I used Git-Shell from GitHub for windows to do this task.
~~~
git clone https://github.com/josephernest/SamplerBox C:\virtualenv\samplerBox\samplerBox
~~~

[Dependencies](#Dependencies)
---
Let's install the dependencies.
** Verify you are inside your virtualenv before doing theses commands! **
1. numpy
~~~
pip install numpy
~~~
For some reason it takes some times... don't panic and wait.

2. pyaudio

  * Download pyaudio wheel (**PyAudio‑0.2.8‑cp27‑none‑win_amd64.whl**)
  http://www.lfd.uci.edu/~gohlke/pythonlibs/#pyaudio

  * Install it with pip
  ~~~
  pip install PyAudio-0.2.8-cp27-none-win_amd64.whl
  ~~~

3. rtmidi-python
  ~~~
  pip install rtmidi_python
  ~~~

4. cython
  ~~~
  pip install cython
  ~~~


[Build samplerBox_audio](#Build samplerBox_audio)
---
* Install Microsoft Visual C++ Compiler for Python 2.7  
  https://www.microsoft.com/en-us/download/details.aspx?id=44266

  ~~~
  "C:\Program Files (x86)\Microsoft Visual Studio 12.0\VC\bin\x86_amd64\vcvarsx86_amd64.bat"
  SET VS90COMNTOOLS=%VS120COMNTOOLS%
  cd c:\virtualenv\samplerBox\SamplerBox
  python setup.py build_ext --inplace
  ~~~

[Add Bat files](#Add Bat files)
---
  
