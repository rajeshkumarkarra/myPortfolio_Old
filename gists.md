---
layout: default
title: "Gists"
---

{% if site.show_excerpts %}
  {% include gists.html %}
{% else %}
  {% include archive2.html title="Gists" %}
{% endif %}



## FORTRAN for Physics
<script src="https://gist.github.com/rajeshkumarkarra/e86202a9839c81d5bf1210192b04afae.js"></script>


## FORTRAN with CUDA
To install Fortran in Google Colab, you can follow these steps:

1. Open a new notebook in Google Colab.

2. Run the following command in a code cell to install the GNU Fortran compiler:
```!apt-get install gfortran
```
3. Test the Fortran installation by running the following command in a code cell:
```
%%writefile test.f90
program hello
   print *, 'Hello, world!'
end program hello
```
```
!gfortran test.f90 -o test
!./test
```
- This should create a file called 'test.f90' containing a simple Fortran program that prints 
"Hello, world!" to the console. The next two lines compile the program and run it.

- The program should output "Hello, world!" in the output cell.
That's it! You have now installed Fortran in Google Colab and tested it with a simple program.

## FORTRAN with CUDA
<script src="https://gist.github.com/rajeshkumarkarra/ab2b8160cad0a8c7acc72690e2e90e2f.js"></script>


## ROOT turorial using Google Colab
    
ROOT Data Analysis Framework
https://root.cern
ROOT: analyzing petabytes of data, scientifically. An open-source data analysis framework used by high energy physics and others.

* To install the ROOT framework in Google Colab, you can follow these steps:

1. Open a new notebook in Google Colab.

2. Run the following command in a code cell to install ROOT dependencies:

```
!sudo apt-get install libx11-dev libxpm-dev libxft-dev libxext-dev
```
3. Download the ROOT installation script by running the following command in a code cell:

```
!wget https://root.cern/download/root_v6.22.06.Linux-ubuntu20-x86_64-gcc9.3.tar.gz
```
- Note: The above command downloads ROOT version 6.22.06 for Ubuntu 20.04 and x86_64 architecture. 
If you need a different version or architecture, you can find the download link on the ROOT website.

4. Extract the downloaded file by running the following command in a code cell:

```
!tar -xzvf root_v6.22.06.Linux-ubuntu20-x86_64-gcc9.3.tar.gz
```
5. Configure the environment variables by running the following commands in a code cell:


```
import os

os.environ['ROOTSYS'] = '/content/root_v6.22.06'
os.environ['LD_LIBRARY_PATH'] = os.path.join(os.environ['ROOTSYS'], 'lib')

```
- Note: Replace the path '/content/root_v6.22.06' with the path where you extracted the ROOT installation files in step 4.

6. Test the ROOT installation by running the following commands in a code cell:

```
import ROOT

hist = ROOT.TH1F("hist", "Histogram", 100, -3, 3)
for i in range(10000):
    hist.Fill(ROOT.gRandom.Gaus())
hist.Draw()

```
- This should create a Gaussian distribution histogram in the output cell.

- That's it! You have now installed the ROOT framework in Google Colab.

## ROOT turorial using Google Colab
<script src="https://gist.github.com/rajeshkumarkarra/f460725814bc0ceb85beb086f7605970.js"></script>









