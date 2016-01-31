# CapstoneProject
Shiny dashboard for visualizing business rates for an electric company.

In order to use the application, please ensure that all files are located within the same
directory (it is suggested that the data file is located in this directory as well). You will need to tell R where your data is located, as well as the name of the data file that will be used.

Open up the RunAPP.R file using R or R Studio.You will see the following code:
####set to appropriate directory with all R files
setwd("C:/Users/Gavin/Desktop/CapstoneProject")

You will need to change the directory to the location where your files are stored. Note that
for Windows users, R uses forward slashes between folders instead of the customary back
slashes used by Windows Explorer.

Next, open the global.R file, and ensure that the name of the file in the following line of code is the same as the file you would like to use:

#read data from csv; make sure file name is correct, and directory is set in RunnApp.r 
read.csv("new_data.csv", header = TRUE)

It is recommended that the data file is located in the same directory as the code; if so, you need only list the name of the file. If the file is located in a different directory, you will need to specify the file location as well as the file name. R natively imports .csv files, so this is the preferred format for data. Packages are available to import .xls and .xlsx files if needed. Once the directory and data file are specified, save the RunApp.R and global.R files. From this point onward, you will not need to repeat the above two steps unless the file directory or data file change locations or names.

To open the app, return to the RunApp.r file and highlight the following lines of code:

#need to run to load shiny package
if(!require(shiny)) install.packages("shiny", dependencies = T)
#initialize app by running this command
runApp()

Hit CTRL + ENTER to execute the code, or click on Code > Run Line(s) to execute the code.
The if(!require(shiny))... code loads the shiny package, or installs the package if it is not currently downloaded. This package needs to be loaded in order to execute the runApp()
command. 

The runApp() command loads the data and required packages from the global.R
file, and proceeds to open the app using the server.r and ui.r code located in your directory.

If you close the app, but leave R open, you need only click the Run App button in the top
right hand corner of the code window to restart the app. If R is closed and reopened, you
will need to highlight and run the above code again.
