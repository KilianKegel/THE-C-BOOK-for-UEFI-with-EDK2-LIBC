# THE C BOOK — reloaded with [EDK2](https://github.com/tianocore/edk2?tab=readme-ov-file#edk-ii-project) and [EDK2-LIBC](https://github.com/tianocore/edk2-libc?tab=readme-ov-file#edk-ii-libc-project)

Build sample programs from my first C book, [THE C BOOK](https://publications.gbdirect.co.uk/c_book/) by 
[Mike Banahan](https://www.linkedin.com/in/mike-banahan-60a548/), [Declan Brady](https://www.linkedin.com/in/declantbrady/), and [Mark Doran](https://www.linkedin.com/in/mark-doran-81ba3281/).

The book was published in 1991 and is now [available for free](https://publications.gbdirect.co.uk/c_book/copyright.html).<br>

<p align="center">
	<img src="https://github.com/KilianKegel/4KPages-THECBOOK/blob/main/images/THECBOOK_FFF.jpg" width="300" height="439">
</p>

[Full copy of the original book is here.](https://github.com/KilianKegel/4KPages-THECBOOK/blob/main/README.md#4kpages-thecbook)

## Occasion
***Tianocore community*** doesn't provide an easy to use **EDK2-LIBC** build environment.

**AppPkg** and **StdLib** was suddenly removed from the **EDK2** source code tree, [without any comment](https://github.com/tianocore/edk2/releases/tag/edk2-stable201905).

The latest available **EDK2-Release** that offers the required packages is 
[**edk2-stable201903**](https://github.com/tianocore/edk2/releases/tag/edk2-stable201903)

## Intention
Demonstrate, howto insert **THE C BOOK** sample programs into **EDK2/EDK2-LIBC** environment and build it.

## Approach
Provide an easy *getting started* with latest available ***Tianocore community*** 
[**EDK2**](https://github.com/tianocore/edk2/releases?page=1) and **EDK2-LIBC**.

Provide **EDK2-LIBC** / **AppPkg** / **StdLib** build process with the complete set of all 
required build tools for Windows 10/11 machines running the AMD64 instruction set:

* **Microsoft EWDK 1703** [EnterpriseWDK_rs2_release_15063_20170317-1834.zip](https://go.microsoft.com/fwlink/p/?LinkID=846038)
* **Python 3.10.11** [python-3.10.11-embed-amd64.zip](https://www.python.org/ftp/python/3.10.11/python-3.10.11-embed-amd64.zip)
* **NASM 2.16.01** [nasm-2.16.01-win64.zip](https://www.nasm.us/pub/nasm/releasebuilds/2.16.01/win64/nasm-2.16.01-win64.zip)

***The above tool set is automatically downloaded, extracted and set up during **LAUNCH.BAT** project start.***<br>
***No need to install build tools separately!***


To speed up repeated installations (avoid repeated downloads of huge tool images),
the images may be –initially– stored permanently in local folder/share, beyond an environment variable
**MYDOWNLOADS**.

To do so follow [Preparation for upcoming portable projects](https://github.com/KilianKegel/Howto-setup-a-UEFI-Development-PC?tab=readme-ov-file#preparation-for-upcoming-portable-projects)

### Using the Enterprise WDK
https://learn.microsoft.com/en-us/windows-hardware/drivers/develop/using-the-enterprise-wdk

The Enterprise Windows Driver Kit (Enterprise WDK) is a command-line build environment that does not require any installation prior to use. Once you have downloaded the EWDK, you can manage it with version control software or you can zip the files and copy as needed. A .zip file created with the Enterprise WDK contains all the necessary compilers, linkers, build tools, headers and libs to build Visual Studio-based driver projects.

The Enterprise WDK contains the necessary elements to build drivers and basic Win32 driver test applications. Use your favorite code editor to modify source code and project files. Because it is command-line based, the Enterprise WDK does lack some of the features incorporated into Visual Studio, such as an IDE, driver deployment and driver testing.

## Howto
0. download project recursively<br>
	**NOTE:** MAKE SURE THAT ROOT DIRECTORY HAS A SHORT PATH, e.g. **`C:\DEMO`**, otherwise download will fail: **Filename too long**
1. run `LAUNCH.BAT` to start the session
2. run `BUILD` (build.cmd), to run the traditional EDK2 build


## Revision history
### 20240228
* initial version