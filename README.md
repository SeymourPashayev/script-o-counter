# ----
# Author: Seymour Pashayev
# SeymourP@solution-source.net
# github: gordonsamh@gmail.com
# ----
# script-o-counter - a script to parse 1.0 and 2.x SuiteScript files and collect code statistics.
# ----
# This script parses through the SuiteScript files is the given directory and categorizes them between
# 1.0 script files and 2.x script files. It collects and sums up the number of lines of code for respective categories.
# This script calculates the correct values for 2.x code, since it is a lot easier to find 2.x code indiactors that would
# yield an almost definite match. 1.0 code values would be slightly overestimated due to the fact that some non-SuiteCloud code looks like 1.0 code.
# This counter also treats regular javascript/typescript as 1.0 code. All of that is due to the lack of consistency in 1.0 code indicators and more.

# Running the script:
# The script is a simple bash script with no dependencies. Just save the script in the desired directory and run it from the directory where the calculations are to be performed.
#
# Example Structure:
# 
# Script Directory
# script-o-counter/counter
#
# SuiteScript Projet Directory
# Project/SuiteScripts
#
# You would call script-o-counter from Projects/SuiteScripts like this:
# $script-o-counter/counter

# Usage Flags:
# -h calls the help window that explains the usage of the script
# -t outputs the scan results into a text file created in the same directory where the parsing was performed
# -r swithes to a recursive parsing mode (the files inside directories within the specified directory will be scanned as well as the root directory itself)

