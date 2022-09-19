# Pinball-MPF
 Pinball-MPF


 door Dorus

----------------------------------------------------------------------------------------
flash Boards:

install python2.7

install pyserial:
c:\Python27\Python.exe -m pip install pyserial

cd C:\Users\dorus\OneDrive\Documents\Pinball\OPP\Python OOP\cyflash
c:\Python27\Python.exe -m cyflash.__main__ --serial COM7 --serial_baudrate 115200 ..\..\Creator\Gen2Images\Gen2.rev0.2.0.0.cyacd


now upload config:
cd C:\Users\dorus\OneDrive\Documents\Pinball\OPP\Python OOP\Gen2Test
c:\Python27\Python.exe -m Gen2Test.py -port=COM7

c:\Python27\Python.exe -m Gen2Test.py -port=COM7 -saveCfg -loadCfg=2sol2switch.py

c:\Python27\Python.exe -m Gen2Test.py -port=COM7 -eraseCfg

c:\Python27\Python.exe -m Gen2Test.py -port=COM7 -saveCfg -loadCfg=1led3inp.py




--------------------------------------------------------------------------------
# versions
#   MPF v0.55.0
#   Python 3.8.10
#   Mission Pinball Framework 0.55 Documentation

# Instruction
#   Install python 3.8.10
#   pip install pip setuptools --upgrade
#       pip                     22.2.2
#       setuptools              64.0.3
#   pip3 uninstall kivy.deps.sdl2 kivy.deps.sdl2_dev kivy.deps.glew kivy.deps.gstreamer
#   pip install mpf[all] mpf-mc
#       if needed:
#           pip install mpf[all]==0.55.0
#           pip install mpf-mc==0.55.0



How MPF installs itself
This guide explains what happens when MPF is installed.

MPF contains a setup.py file in the root of the MPF repository. This is the file that’s called by pip when MPF is installed. (You can also install MPF without using pip by running python3 setup.py from the root folder.)

Dependencies
MPF requires Python 3.4 or newer. In our installation instructions, we also recommend that users install/update the following Python packages to their latest versions:

pip
setuptools (for Linux & Mac)
Cython 0.24.1 (for Linux & Mac)
The additional packages for Linux & Mac are used because MPF-MC is actually compiled on built on those platforms. For Windows we have pre-built wheels, so compiling is not necessary.

MPF has the following additional dependencies which are specified in the setup.py file and automatically installed when MPF is installed.

ruamel.yaml >=0.10,<0.11: Used for reading & writing YAML files.
pyserial >= 3.2.0: Used for serial communication with several types of hardware
pyserial-asyncio >= 0.3: Also used for serial communication
typing Used for type-checking & type hinting.
Note that some of these dependencies will install their own dependencies.

The setup.py file also specifies a console_scripts entry point called mpf. This is what lets the user type mpf from the command environment to launch MPF.



------------------------------------


how to run:

cd C:\pinball\mpfv1
C:\Users\dorus\AppData\Local\Programs\Python\Python38\python.exe -m mpf both
