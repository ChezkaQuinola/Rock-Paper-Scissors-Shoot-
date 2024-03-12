```py
scene.background= vector(255/255,197/255,122/255) #sets the background color
scene.camera.pos = vector(0,0,3) #sets the position of the camera

''' left hand ''' #codes to create the left hand
#FUNCTIONS
def create_left_arm_and_hand(): #defines a function for the left hand
    # Create left arm
    left_arm = box(size=vector(2, 0.5, 0.5), pos=vector(-2.5, -1, 0)) #gives the arm all the parameters
    # Create left hand
    left_hand = box(size=vector(0.6, 0.6, 0.6), pos=vector(-1.5, -1, 0))  #gives the hand all the parameters
    return left_arm, left_hand #returns the function
left_arm, left_hand = create_left_arm_and_hand() #calls the function

''' right hand ''' #codes to create the right hand
#FUNCTIONS
def create_right_arm_and_hand(): #defines a function for the right hand
    # Create right arm
    right_arm = box(size=vector(2, 0.5, 0.5), pos=vector(2.5, -1, 0)) #gives the arm all the parameters
    # Create right hand
    right_hand = box(size=vector(0.6, 0.6, 0.6), pos=vector(1.5, -1, 0)) #gives the hand all the parameters
    return right_arm, right_hand #returns the function
right_arm, right_hand = create_right_arm_and_hand() #calls the function

#COMPOUNDS
you = compound([left_arm, left_hand]) #creates a compound shape for all the left hand codes to make it easier to call
you.color = vector(255/255,235/255,205/255) #sets the color
opp = compound([right_arm, right_hand]) #creates a compound shape for all the right hand codes to make it easier to call
opp.color = vector(222/255,184/255,135/255) #sets the color

''' PAPER ''' #codes to create the fingers for the paper response
#VARIABLES
lp_finger1 = box()  #creates a box and assigns it to lp_finger1
lp_finger1.size = vector(2/3,0.5/3,0.5/3) #sets the size
lp_finger1.pos = vector(-1,-0.7,0) #sets the position
lp_finger1.rotate(angle=0.3, axis=vec(0,0,1), origin=vector(-1,-0.85,0)) #sets the rotation
lp_finger2 = box() #creates a box and assigns it to lp_finger2
lp_finger2.size = vector(2/3,0.5/3,0.5/3) #sets the size
lp_finger2.pos = vector(-1,-1,0) #sets the position
lp_finger3 = box() #creates a box and assigns it to lp_finger3
lp_finger3.size = vector(2/3,0.5/3,0.5/3) #sets the size
lp_finger3.pos = vector(-1,-1.25,0) #sets the position
lp_finger3.rotate(angle=-0.1, axis=vec(0,0,1), origin=vector(-1,-0.85,0)) #sets the rotation
lp_finger4 = box() #creates a box and assigns it to lp_finger4
lp_finger4.size = vector(2/3,0.5/3,0.5/3) #sets the size
lp_finger4.pos = vector(-1.4,-0.45,0) #sets the position
lp_finger4.rotate(angle=0.5, axis=vec(0,0,1), origin=vector(-1,-0.85,0)) #sets the rotation

#VARIABLES
rp_finger1 = box() #creates a box and assigns it to rp_finger1 
rp_finger1.size = vector(2/3,0.5/3,0.5/3) #sets the size
rp_finger1.pos = vector(1,-0.7,0) #sets the position
rp_finger1.rotate(angle=-0.3, axis=vec(0,0,1), origin=vector(1,-0.85,0)) #sets the rotation
rp_finger2 = box() #creates a box and assigns it to rp_finger2
rp_finger2.size = vector(2/3,0.5/3,0.5/3) #sets the size
rp_finger2.pos = vector(1,-1,0) #sets the position
rp_finger3 = box() #creates a box and assigns it to rp_finger3
rp_finger3.size = vector(2/3,0.5/3,0.5/3) #sets the size
rp_finger3.pos = vector(1,-1.25,0) #sets the position
rp_finger3.rotate(angle=--0.1, axis=vec(0,0,1), origin=vector(1,-0.85,0)) #sets the rotation
rp_finger4 = box() #creates a box and assigns it to rp_finger4
rp_finger4.size = vector(2/3,0.5/3,0.5/3) #sets the size
rp_finger4.pos = vector(1.4,-0.45,0) #sets the position
rp_finger4.rotate(angle=-0.5, axis=vec(0,0,1), origin=vector(1,-0.85,0)) #sets the rotation

left_paper = compound([lp_finger1,lp_finger2,lp_finger3,lp_finger4]) #creates a compound shape for left paper shape to make it easier to call
left_paper.visible = False #sets initial visibility to false

right_paper = compound([rp_finger1,rp_finger2,rp_finger3,rp_finger4]) #creates a compound shape for right paper shape to make it easier to call
right_paper.visible = False #sets initial visibility to false

left_paper.color = vector(255/255,235/255,205/255) #sets the color
right_paper.color = vector(222/255,184/255,135/255) #sets the color

''' SCISSORS '''
#VARIABLES
ls_finger1 = box() #creates a box and assigns it to ls_finger1
ls_finger1.size = vector(2/3,0.5/3,0.5/3) #sets the size
ls_finger1.pos = vector(-1,-0.7,0) #sets the position
ls_finger1.rotate(angle=0.3, axis=vec(0,0,1), origin=vector(-1,-0.85,0)) #sets the rotation
ls_finger2 = box() #creates a box and assigns it to ls_finger2
ls_finger2.size = vector(2/3,0.5/3,0.5/3) #sets the size
ls_finger2.pos = vector(-1,-1,0) #sets the position

rs_finger1 = box() #creates a box and assigns it to rs_finger1
rs_finger1.size = vector(2/3,0.5/3,0.5/3) #sets the size
rs_finger1.pos = vector(1,-0.7,0) #sets the position
rs_finger1.rotate(angle=-0.3, axis=vec(0,0,1), origin=vector(1,-0.85,0)) #sets the rotation
rs_finger2 = box() #creates a box and assigns it to rs_finger2
rs_finger2.size = vector(2/3,0.5/3,0.5/3) #sets the size
rs_finger2.pos = vector(1,-1,0) #sets the position

left_scissors = compound([ls_finger1, ls_finger2]) #creates a compound shape for left scissors shape to make it easier to call
left_scissors.visible =  False #sets initial visibility to false
left_scissors.color = vector(255/255,235/255,205/255) #sets the color

right_scissors = compound([rs_finger1, rs_finger2]) #creates a compound shape for right scissors shape to make it easier to call
right_scissors.visible =  False #sets initial visibility to false
right_scissors.color = vector(222/255,184/255,135/255) #sets the color

''' USER INPUT ''' #codes to make user input work
option = input('Choose one: Rock, Paper, Scissors') #creates a text input for person's choice

right_option_random = random() # Generate a random number between 0 and 1 for the right hand choice

#IF-STATEMENTS
# Determine the right hand choice based on the random number
if right_option_random < 1/3:  # 1/3 probability for rock
    right_option = 'rock' #if input is 'rock'
elif right_option_random < 2/3:  # 1/3 probability for paper
    right_option = 'paper' #if input is 'paper'
else:  # 1/3 probability for scissors
    right_option = 'scissors' #if input is 'scissors'

#VARIABLES
i = 0 #initialize animation iterator for opp
j = 0 #initialize animation iterator for you
rotation_angle1 = 0.05 #controls the rotation angle for you
rotation_angle2 = -0.05  #controls the rotation angle for opp
max_loops = 8  #checks the amount of loops before it stops
target_loops = max_loops * 2 #makes the target loops 2x the max_loops
opp_loops = 0 #initializes the amount of loops

# Rotate the hands
#WHILE-LOOPS
while True:
    rate(60) #sets framerate to 60fps
    
    you.rotate(angle=rotation_angle1, axis=vec(0, 0, 1), origin=vector(-3, -1, 0)) #rotates the arm
    #MATH-LOGIC
    j += 1 #adds +1 for j
    #IF-STATEMENT
    if abs(j * rotation_angle1) >= 1.25: #checks if the absolute value of the product of j and 0.05 is greater than or equal to 1.25
        rotation_angle1 *= -1 #reverses the rotation
        j = 0 #resets the iterator
    
    # Rotate for "opp"
    opp.rotate(angle=rotation_angle2, axis=vec(0, 0, 1), origin=vector(3, -1, 0)) #rotates the arm
    #MATH-LOGIC
    i += 1 #adds +1 for i
    #IF-STATEMENT
    if abs(i * rotation_angle2) >= 1.25: #checks if the absolute value of the product of i and -0.05 is greater than or equal to 1.25
        rotation_angle2 *= -1 #reverses the rotation
        i = 0 #resets the iterator
        
        #INDEPENDENT RESEARCH -> BREAKING A LOOP
        #MATH-LOGIC
        # Check for the number of loops for "opp"
        opp_loops += 1 #adds +1 to the opp_loops
        #IF-STATEMENT
        if opp_loops >= max_loops: #checks if the opp_loops is greater than the max_loops
            break #ends the animation

#INDEPENDENT RESEARCH -> DELAYS
#FOR-LOOPS
#Introduce a delay for changing visibility for right hand
for _ in range(1): #60 frames per second, so 1 frame for 0.0167 seconds--as soon as the loop above breaks, the delay starts
    rate(60) # 60 fps

#IF-ELSE
#Set visibility based on random choice for right hand
if right_option == 'rock': #if option is rock
    right_paper.visible = False #make paper's visibility false
    right_scissors.visible = False #make scissors's visibility false
elif right_option == 'paper': #if option is paper
    right_paper.visible = True #make paper's visibility true
    right_scissors.visible = False #make scissors's visibility false
elif right_option == 'scissors': #if option is scissors
    right_paper.visible = False #make paper's visibility false
    right_scissors.visible = True #make scissors's visibility true

#FOR-LOOPS
#Introduce a delay for changing visibility for left hand
for _ in range(1): #60 frames per second, so 1 frame for 0.0167 seconds--as soon as the loop above breaks, the delay starts
    rate(60)

#IF-ELSE
#Set visibility based on user input
if option == 'rock' or option == 'r': #if user input is rock or r
    left_paper.visible = False #make paper's visibility false
    left_scissors.visible = False #make scissors's visibility false
elif option == 'paper' or option == 'p': #if user input is paper or p
    left_paper.visible = True #make paper's visibility true
    left_scissors.visible = False #make scissors's visibility false
elif option == 'scissors' or option == 's': #if user input is scissors or s
    left_paper.visible = False #make paper's visibility false
    left_scissors.visible = True #make scissors's visibility true
else: #if none of the options above were inputted
    print('Invalid choice. Please choose Rock, Paper, or Scissors.')
    txt = text(text='GAME OVER', pos=vector(-3.5, 0, -5), color=color.red) #create a game over screen
    scene.background = vector(0, 0, 0) #change the background to black
    opp.visible = False #make everything invisible
    you.visible = False #make everything invisible
    
scene.autoscale = False #stops the scene from autoscaling

#LISTS
messages = ["Rock!", "Paper!", "Scissors!", "Shoot!"] #creates a list of text

num_messages = len(messages) #Number of messages

#LISTS
text_objects = [] #create a list to store text objects

#FOR-LOOPS
# Create text objects and add them to the list
for i in range(num_messages): #for every i in num_messages
    text_object = text(text=messages[i], pos=vector(-15+i*10, 1, 0), color=color.red, height = 0.3) #sets the parameters for the messages
    text_objects.append(text_object) #appends this to the text_objects list

#WHILE-LOOPS
# Animation loop
while True:
    rate(10)  # Limit the animation rate
#FOR-LOOPS
    # Move text objects from left to right
    for text_obj in text_objects:
        text_obj.pos.x -= 2 #makes the x position 2
        #IF-STATEMENT
        if text_obj.pos.x < -25:  #reset the text's position when it goes beyond the right edge
            text_obj.pos.x = 25 #resets the position

```
