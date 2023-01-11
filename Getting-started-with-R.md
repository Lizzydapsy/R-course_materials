*R for Statistics and Data Visualization - An Introduction for Life
Scientists 1*

# Setting up R and RStudio / Getting started with R

###### Elizabeth Oladapo

The aim of this practical is to get you started with installing R and
RStudio on your computer, customize RStudio and installing
R-libraries/packages

### 1. Install R and RStudio

Download the latest version RStudio Desktop version
[here](https://posit.co/download/rstudio-desktop/#download) (You do not
have to figure out what version or type of installer to download, the
page automatically figures out what is compatible with the operating
system you are using).

Download the latest version of R Desktop version from
[CRAN](https://cran.r-project.org/), for your operating system.

------------------------------------------------------------------------

Choose the right one for your system

------------------------------------------------------------------------

**Windows**

Install R by downloading and running the .exe file from CRAN. Note that
if you have separate user and admin accounts, you should run the
installers as administrator (right-click on .exe file and select “Run as
administrator” instead of double-clicking). Otherwise problems may occur
later, for example when installing R packages.

**Mac**

Install R by downloading and running the .pkg file from CRAN.

**Linux**

Download the binary files for your distribution from CRAN Or use your
package manager (e.g. for Debian/Ubuntu run sudo apt-get install r-base
and for Fedora run sudo yum install R).

<br/>

**Note that** We will always open RStudio to use R

<br/>

### 2. Customizing RStudio

Open RStudio

RStudio has four main panes each in a quadrant of your screen: Script
Editor, Console, Workspace Environment (and History), and Plots (and
Files, Packages, Help). Generally, we will want to write programs longer
than a few lines.

Navigate to Tools → Global options → Appearance and switch the theme in
the Editor Theme option. By default, you will have the Textmate theme
activated.

<br/>

### 3. Installing R Packages

We will be installing some extra R packages required for the training as
we proceed. However, there are R functions that can check whether a
package is currently installed. For example, the find.package function:

    find.package("MASS")

    ## [1] "C:/Program Files/R/R-4.2.2/library/MASS"

The Comprehensive R Archive Network (CRAN) repository stores thousands
of stable R packages designed for a variety of data-related tasks. Most
often, you will use this repository to install various R packages.

To install an R package from CRAN, we can use the install.packages()
function:

    install.packages('readr')

<br/>

We can use the same function to install several R packages at once. For
this, we need to apply first the c() function to create a character
vector containing all the desired packages for example:

    install.packages(c('ggplot2', 'dplyr'))

Above, we have installed two R packages: ggplot2 (for data
visualization) and dplyr (for data manipulation).

------------------------------------------------------------------------

Alternative Method

------------------------------------------------------------------------

In an IDE such as RStudio, we can use the menu instead of the
install.packages() function to install the necessary modules from the
CRAN repository by completing the following steps:

Click Tools → Install Packages

Select Repository (CRAN) in the Install from: slot

Type the package name (or several package names, separated with a white
space or comma)

Leave Install dependencies ticked as by default

Click Install

**In addition**, R Packages can be installed from Other Sources such as
GitHub, Zip Files downloaded on your local machine as a .zip or tar.gz
file, but we will not cover this here.

<br/>

### 4. Loading R Packages

Once the necessary packages have been installed, the next step is to
load each package to start working with them. While we need to install
each package only once (i.e., the first time using R on a particular
computer), we may have to load each package for every new R session. For
this purpose, we use the library() function and pass in the package
name, as follows:

    library(dplyr)

**Note that**, in this case, we don’t need to include the package name
in quotation marks and we cannot load more than one package at a time.

<br/>

### 5. Setup an RStudio project

Rstudio project is an R analysis structure that makes it easy and
straightforward to divide your projects into multiple contexts, each
with their own working directory, environment, history, and source
documents… creating a very clean working environment.

Using RStudio projects eliminates so much of the early-stage hassles and
confusions around reading in and exporting data. Setting up a working
directory properly also helps build up good habits that are conducive to
reproducible analysis (Can be shared with collaborators to have access
to your work space, data and scripts in one go).

------------------------------------------------------------------------

Create your project directory/folder

------------------------------------------------------------------------

Navigate to your file explorer window

File explorer window -&gt; Document folder or Google drive folder -&gt;
Make a new folder called “R - training” (Parent directory) -&gt; Make
two offspring folders: Data and Scripts

Now, Open up RStudio and create an RStudio project using the menu File
-&gt; New Project -&gt; Existing Directory and browse to the directory
that you named “R- training” -&gt; Create Project

Rstudio will refresh so that the working directory corresponds to the
course data folder, “R-training”.

Quit your RStudio, navigate to your R-training folder double click your
project to open up RStudio which now contains your data folder and
scripts folder in your files pane.

<br/>

### 6. Working at the RStudio script pane

R is used interactively - you type an instruction to “do something” and
the instruction will be interpreted when you hit the Enter key.

Let’s briefly see use shortcut keys:

ctrl/cmd + enter: Run R code line/block in R console

ctrl+shift+C : Comment out line

ctrl+shift+R - Insert section break (useful with outline enabled)

alt+M+-

alt+-

alt+- Inserts the &lt;- (Used to assign stuffs to variables/objects)

ctrl+shift+M: Inserts the pipe operator %&gt;% (very useful shortcut)

ctrl+D: Deletes entire line

<br/> Let’s try simple arithmetic with R.

Type 1 + 3 at the scripting pane and hit Ctrl+Enter keys:

    1+13

    ## [1] 14

The answer is shown at the console with a \[1\] in front of it. The 1
inside the square brackets signifies how many values were in the answer
(in this case only one).

<br/>

**Thumbs up! for getting it done, we are now ready for the data
importing and analysis**

**Return** to the main course page:
<https://github.com/Lizzydapsy/R-for-Data-Analysis>