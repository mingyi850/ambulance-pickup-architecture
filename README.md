
# Ambulance Pickup Problem

## Description:

The ambulance planning real-time problem is to rescue as many people as possible following a disaster. The problem statement identifies the locations of people and the time they have to live. You can also establish mobile hospitals at the beginning of the problem. The problem is to get as many people to the hospitals on time as possible.

In our case, the graph is the Manhattan grid with every street going both ways. It takes a minute to go one block either north-south or east-west. Each hospital has an (x,y) location that you can determine when you see the distribution of victims. The ambulances need not return to the hospital where they begin. Each ambulance can carry up to four people. It takes one minute to load a person and one minute to unload up to four people. Each person will have a rescue time which is the number of minutes from now when the person should be unloaded in the hospital to survive. By the way, this problem is very similar to the vehicle routing problem about which there is an enormous literature and nice code like "jsprit" which was used in 2015 to great effect.

The data will be in the form:
```angular2html
person(xloc, yloc, rescuetime)
hospital(numambulance)
```

## Contact:

```angular2html
Mingyi Lim
Email: ml9027@nyu.edu
```

## Notes:

   1. You are responsible to check for the order in which the ambulances are departed. 
i.e. if A has 3 ambulances, there is a path B -> A making 4 total at A, 
you will need to print the result B -> A before departing the 4th ambulance from A.
   2. If you run into any format issues, the program will only leave an error output, but NOT stop the execution.
Even if your output is being validated, it may have some errors printed (Sample output has few such errors displayed)
   3. If you find any bugs in the code, feel free to let us know, and we'll fix it for you.
   4. Kindly make your submissions (even if a skeleton with proper but non-optimized output) by end of Wednesday (Oct 5, 2022). 
This gives us a buffer to get back to you incase there is any error in compiling your code.

## Usage (Python):

Place your logic in `my_solution()` on line 277 and the code should do the rest for you.

If you do not want to mess with the validator file, you are free to follow the approach below (for other languages)
and you should be fine with using another file.

NOTE: The `read_data()` returns the list of **objects** and not a dictionary. 
You can use `object.prettify()` to get the dictionary instead, or add another function as per your requirements.

## For Languages other than python:

**Input:** The data will be in the `input_data.txt` file.

The given format is:

```angular2html
person(xloc,yloc,rescuetime)
1,1,10
...
...
2,2,20

hospital(numambulance)
1
2
3
```

**Output:** Once you calculate your results, generate a `[team_name].txt` file under `Outputs` folder with the following format

```angular2html
H1:x_coordinate,y_coordinate
...
H3:x_coordinate,y_coordinate

Start_Time H1 P1 P2 ... PN H2  
...
Start_Time H3 P1 P3 ... PN H2
```
You can refer to the `sample_result.txt` to get the idea. The sample result is NOT optimal by any means. `bad_result.txt` shows examples of lines with bad format. 

**Validation:** Once done with your code, you can then validate the result using the following:

`python3 validator.py`
         OR
`python3 validator.py input_data.txt Outputs/[team_name].txt`

Check Submission section on what files to submit. After you create the makefile, you can also validate your code with:

`python3 driver.py`


## Submission

Create a makefile for running your code. Your code would be copied to `Solutions` folder. Make sure your makefile includes that path to run the code and prints the result in the `Outputs` folder.

Submit your code file titled `[team_name]_algorithm.extension` and the makefile `[team_name].mk`.
