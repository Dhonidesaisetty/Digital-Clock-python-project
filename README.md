Project #19 - Digital Clock

A Python program that shows the current time as a digital clock in the terminal. Instead of printing plain numbers, each digit is drawn in a seven-segment display style using _ and | characters. The clock updates every second.

Sample Output

 __   __       __   __       __   __ 
|  | |__   *  |__  |__   *  |  | |__ 
|__|  __|  *   __| |__|  *  |__|  __|

Press Ctrl-C to quit.

Features

	•	Shows the current time in a 12-hour format (hours, minutes, seconds)
	•	Draws digits in seven-segment style
	•	Colons made of asterisks (*) between hours, minutes and seconds
	•	Updates every second
	•	Stops cleanly when you press Ctrl-C

Project Structure

Python_Project/
├── digitalclock.py   # Main program: reads the time and displays the clock
├── sevseg.py         # Module that draws numbers as seven-segment digits
└── README.md

Requirements

	•	Python 3.x
	•	No external libraries (uses only the built-in sys and time modules)

How to Run

	1.	Download or clone the repository:

git clone https://github.com/<your-username>/<your-repository>.git
cd <your-repository>

	2.	Make sure digitalclock.py and sevseg.py are in the same folder.
	3.	Run the program:

python digitalclock.py

	4.	Press Ctrl-C to quit.

How It Works

	1.	time.localtime() reads the current time from the computer.
	2.	tm_hour % 12 converts 24-hour time to 12-hour time (0 is shown as 12).
	3.	sevseg.getSevSegStr() turns hours, minutes and seconds into 3-line digit drawings.
	4.	splitlines() splits each drawing into top, middle and bottom rows.
	5.	The rows are printed side by side, with * placed between them to form the colons.
	6.	An inner loop waits (time.sleep(0.01)) until the second changes, then the clock is redrawn.
	7.	except KeyboardInterrupt catches Ctrl-C and ends the program with sys.exit().

Concepts Used

	•	while loops and break
	•	try / except (handling KeyboardInterrupt)
	•	Importing and creating your own module
	•	String methods: zfill(), splitlines()
	•	The time module

Author

	•	Name: D. Dhoni
	•	USN: 25BTRA018
	•	Course: CSE (GenAI) - A

Credits

Based on The Big Book of Small Python Projects by Al Sweigart (Project #19, Digital Clock).
