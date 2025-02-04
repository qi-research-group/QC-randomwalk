# QC-randomwalk
Use the behavioural data (choices, response times) to model reliability ratings with QRW model, according to the paper.

In short, the experiment entails 20 blocks, after which the human agent rates how well they trust the assessments of the AI. The rating
is with a visual-analog-scale ranging from 0% to 100%.


## Participant Data
The participants have a number ranging from 001 to 036, but some number are missing due to issues with data recording.
The history_files contain all the relevant raw data.
These are:
 - history_0XX.txt
 - times_0XX.txt
 - ratings_0XX.txt

### history:
The history files contain codes. The codes relate to what happened during the experiment.
During the block, there are 28 trials, during which three main things can happen:
 - 4; HRAIR; the human things it's a real face; the AI confirms (also real)
 - 5; HRAIF; the human things it's a real face; the AI disagrees (says it's fake)
 - 6; HRAIF; the human things it's a fake face; the AI confirms (says it's real)
 - 7; HRAIF; the human things it's a fake face; the AI disagrees (says it's fake)
The human has 2 seconds to press the button; if this didn't happen, then it is a missed trial (coded by the number 3).
There are also codes such as 104, 105, etc; these code similar events during the (single) practice run.

### times:
The times are the response times matching the events coded in the history_XX files.

### ratings:
These record the ratings the participants gave during the experiment. There are 22 ratings total. 1 rating before the pratice block; 1 rating after the practice block; 20 ratings after each of the experimental blocks.

## Relevant Scripts
The main script that runs all the simulations is: ```x1_model_behavior.m```. This script calls all of the other relevant functions and creates the figures.

## Relevant figures
See the figure subfolder to inspect the QRW model outcome when it applied to the behavioral data of each of our 34 participants.

# System requirements
To run the sumulations clone this repository, and run it with Matlab. We used Matlab R2018a to run these simulations, but newer matlab versions should also accomodate.
Bioinformatics Toolbox                                Version 4.10        (R2018a)
Global Optimization Toolbox                           Version 3.4.4       (R2018a)
Image Processing Toolbox                              Version 10.2        (R2018a)
Optimization Toolbox                                  Version 8.1         (R2018a)
Parallel Computing Toolbox                            Version 6.12        (R2018a)
Signal Processing Toolbox                             Version 8.0         (R2018a)
Statistics and Machine Learning Toolbox               Version 11.3        (R2018a)
