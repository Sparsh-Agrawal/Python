import tkinter 
import random 

colours = ['Red','Blue','Green','Pink','Black','Yellow','Orange','White','Purple','Brown'] 
score = 0
timeleft = 30

def startGame(event): 
	
	if timeleft == 30: 
		
		countdown() 
		 
	nextColour() 

def nextColour(): 
 
	global score 
	global timeleft 

	if timeleft > 0: 

		e.focus_set() 

		if e.get().lower() == colours[1].lower(): 
			
			score += 1

		e.delete(0, tkinter.END) 
		
		random.shuffle(colours) 
		
		label.config(fg = str(colours[1]), text = str(colours[0])) 
		
		scoreLabel.config(text = "Score: " + str(score)) 


def countdown(): 

	global timeleft 

	if timeleft > 0: 

		timeleft -= 1
		
		timeLabel.config(text = "Time left: " + str(timeleft)) 
							
		timeLabel.after(1000, countdown) 


gui = tkinter.Tk() 

gui.title("YOU THINK ! YOU LOSE") 

gui.geometry("375x200") 

instructions = tkinter.Label(gui, text = "Type in the colour of the words, and not the word text !", font = ('Helvetica', 12)) 
instructions.pack() 

scoreLabel = tkinter.Label(gui, text = "Press enter to start", 
									font = ('Helvetica', 12)) 
scoreLabel.pack() 

timeLabel = tkinter.Label(gui, text = "Time left: " + str(timeleft), font = ('Helvetica', 12)) 
				
timeLabel.pack() 

label = tkinter.Label(gui, font = ('Helvetica', 60)) 
label.pack() 

e = tkinter.Entry(gui) 
 
gui.bind('<Return>', startGame) 
e.pack() 

e.focus_set() 

gui.mainloop()
