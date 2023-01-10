*R for Statistics and Data Visualization - An Introduction for Life Scientists 1*

# Setting up R and RStudio / Getting started with R

###### Elizabeth Oladapo

The aim of this practical is to get you started with installing R and RStudio on your computer, customize RStudio and installing R-libraries/packages

### 1. Install R and RStudio
Download the latest version RStudio Desktop version [here](https://posit.co/download/rstudio-desktop/#download) (You do not have to figure out what version or type of installer to download, the page automatically figures out whats compatible with the operating system you are using).

Download the latest version of R Desktop version from [CRAN](https://cran.r-project.org/), for your operating system.

*** 
Choose the right one for your system 

*** 

__Windows__

Install R by downloading and running the .exe file from CRAN. 
Note that if you have separate user and admin accounts, you should run the installers as administrator (right-click on .exe file and select “Run as administrator” instead of double-clicking). 
Otherwise problems may occur later, for example when installing R packages.

__Mac__

Install R by downloading and running the .pkg file from CRAN. 

__Linux__

Download the binary files for your distribution from CRAN Or use your package manager (e.g. for Debian/Ubuntu run sudo apt-get install r-base and for Fedora run sudo yum install R). 

<br/>

__Note that__ We will always open RStudio to use R

<br/>

### 2. Customizing RStudio
Open RStudio

RStudio has four main panes each in a quadrant of your screen: 
Script Editor, Console, Workspace Environment (and History), and Plots (and Files, Packages, Help). 
Generally, we will want to write programs longer than a few lines.

Navigate to Tools → Global options → Appearance and switch the theme in the Editor Theme option. By default, you will have the Textmate theme activated.

<br/>

### 3. Installing R Packages from the CRAN Repository

The Comprehensive R Archive Network (CRAN) repository stores thousands of stable R packages designed for a variety of data-related tasks. Most often, you will use this repository to install various R packages.

To install an R package from CRAN, we can use the install.packages() function:

```{r}
install.packages('readr')
```
<br/>

We can use the same function to install several R packages at once. For this, we need to apply first the c() function to create a character vector containing all the desired packages for example:

```{r}
install.packages(c('ggplot2', 'dplyr'))
```
Above, we have installed two R packages: ggplot2 (for data visualization) and dplyr (for data manipulation).

***

Alternative Method

***

In an IDE such as RStudio, we can use the menu instead of the install.packages() function to install the necessary modules from the CRAN repository by completing the following steps:

Click Tools → Install Packages

Select Repository (CRAN) in the Install from: slot

Type the package name (or several package names, separated with a white space or comma)

Leave Install dependencies ticked as by default

Click Install

__In addition__, R Packages can be installed from Other Sources such as GitHub, Zip Files downloaded on your local machine as a .zip or tar.gz file, but we will not cover this here.

### 4. Loading R Packages

Once the necessary packages have been installed, the next step is to load each package to start working with them. While we need to install each package only once (i.e., the first time using R on a particular computer), we may have to load each package for every new R session. For this purpose, we use the library() function and pass in the package name, as follows:

```{r}
library(dplyr)
```
__Note that__, in this case, we don’t need to include the package name in quotation marks and we cannot load more than one package at a time.


__Return__ to the main course page:
https://github.com/Lizzydapsy/R-for-Data-Analysis
