# Mini Hogwarts System - Digital Logic Design

**Course:** CSE 4206 : Digital Logic Design Lab at Islamic University of Technology (IUT)

## Overview

This project is a digital logic-based student management and academic information system designed around the fictional Hogwarts School of Witchcraft and Wizardry. The system takes the student's Year as an external input and randomly sorts the student into a house. Implemented as a digital circuit in Proteus, the system utilizes combinational and sequential logic to handle student registration, house and year identification, academic statistics, eligibility tracking, course information, a graduation countdown, and a basic grading display.

## Key Features

* **House Sorting & Registration:** The system randomly generates a House state using JK flip-flops, which is then captured and stored by D flip-flops when the student presses the "Register" button.


* **House Identification Indicators:** A 2-to-4 decoder decodes the stored 2-bit House code to light up a corresponding LED: 00 for Gryffindor (Red), 01 for Hufflepuff (Yellow), 10 for Ravenclaw (Blue), and 11 for Slytherin (Green).


* **Live Statistics:** Every successful registration increments the specific house and year counters, maintaining a live numerical tally of the student population on 7-segment displays.


* **Library Eligibility (Restricted Area Access):** The system restricts access based on the student's year, illuminating a Red LED (Access Denied) for Years 1 through 4, and a Green LED (Eligible to Access) for Years 5 through 7.


* **Year-Based Academic Eligibility:** A 3-to-8 decoder determines extracurricular and academic paths: Year 1 activates Flying Lessons; Year 5 activates Prefect and Head Boy/Girl; Year 6 activates Prefect and N.E.W.T.; and Year 7 activates O.W.L., Prefect, and N.E.W.T..


* **Course Count:** Multiplexers use the registered Year as a selection input to display predefined Available Course Counts and Minimum Required Course Counts.


* **Graduation Countdown:** A subtractor computes the years remaining until Year 7 (7 minus the stored year) and outputs the result to a 7-segment display.


* **Student Grade System:** Converts numerical marks into letter grades (80–99 = A, 60–79 = B, 40–59 = C, 00–39 = F). If an invalid hexadecimal number is entered, a red LED blinks to indicate an invalid input.



## Application of Theoretical Components

* **D Flip-flops/Registers:** Retain the captured randomized House value and user-inputted Year between operations.


* **JK Flip-flops:** Drive the sequential state transitions required for randomized House assignment.


* **Decoders:** 2-to-4 decoders drive the House LEDs, while 3-to-8 decoders convert the 3-bit Year code to feed the academic eligibility logic via OR gates.


* **Up-Counters:** Maintain the accumulated, live statistics for the four houses and seven years.


* **Multiplexers (MUX):** Select year-dependent data for the Course Eligibility Segment.


* **Subtractors & Adders:** Handle the Graduation Countdown arithmetic.


* **7-Segment Displays:** Convert binary values into human-readable digits for the Year, student counts, course counts, graduation countdown, and grades.


* **Combinational Logic (AND/OR/NOT):** Controls conditions, such as determining if a student is a Prefect (Y5 OR Y6 OR Y7) or N.E.W.T. eligible (Y6 OR Y7).



## User Guideline

1. **Power On:** Switch on the circuit's power supply so all displays initialize to zero.


2. **Select House & Year:** Set the 2-bit House logic toggles (00 to 11) and the 3-bit Year logic toggles (001 for Year 1, up to 111 for Year 7).


3. **Register:** Press the Register push-button to store the current House and Year in the D flip-flop register.


4. **Observe Outputs:**
* Confirm the correct House LED (Red, Yellow, Blue, or Green) turns on.


* Read the registered student's academic year on the 7-segment display.


* Check the Library Eligibility and Academic Eligibility LEDs (Flying Lessons, O.W.L., etc.) based on the year.


* View the automatically updated house-wise and year-wise statistics.


* View the Available and Minimum Required Course displays.


* View the Graduation Countdown.




5. **View Grades:** Input student marks to view the corresponding letter grade on the 7-segment display.



## Team Members

* [Mohsina Islam (240042146)](https://github.com/muhsina-1)
* [A. N. M. Mohaiminur Rahman (240042142)](https://github.com/leigion-broken11)
* [Lamisa Ibnat Zaman (240042141)](https://github.com/lamisazaman)
* [Mugdho Ranin Rahman Mahee (240042154)](https://github.com/Mugdho54)
* [Ummul Khaer Fatema (240042153)](https://github.com/ummulkhaer-max)
* [Tanbirul Islam (240042133)](https://github.com/tanbirulislam-hash)
