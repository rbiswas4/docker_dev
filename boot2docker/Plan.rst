My Goal
=======

I am working on a project where I would like to be able to simulate and fit SNe and obtain cosmology in a variety of ways. Some of the code that I may need to
   use is hard to install (at least with analysis components). So, the idea is to do this with docker, but not install the entire code together because we can use some
   of the components for other things. 

Steps
-----

1. have a docker image of anaconda python
2. CERN root with pyroot as another docker image which sits on top of the python and links to the python libraries
3. Install SNANA using the cern root libraries

