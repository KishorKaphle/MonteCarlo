import numpy as np
import random
import matplotlib.pyplot as plt


X = list (np.arange(0, 5, 0.05)) #Rather than making coordinate continuous, we can make it discrete with step size say 0.05
Y = list (np.arange(0, 5, 0.05))
total_area = 5*5


# Lets find the area of top left quadarant of a square with length 5 unit.

# Since our square's dimension is 5, we can generate random numbers from 0 to 5 only for both x and y axis

trails = 1000
probability = []
area = []
events = range (1, trails, 10)

for trail in range (1, trails, 10):

    
    counter = 0
    success = 0

    while counter < trail:
    # For upper left qudarant, max and min coordinate for x will be 0 & 5 and for y 2.5 & 5. So we will calculate probabilty of random number (x and y) falling
    # into range of upper left quadarant by which we can find probabistic value of area of that quadarnt. 
        x = random.uniform (0, 5)
        y = random.uniform (0, 5)

        if (x <=2.5) and (y>=2.5 and y<=5):
            success +=1
        counter +=1
        print ('...', counter)

    probability.append ((success/trail))
    area.append ((success/trail)*total_area)
    #print ('probabiltiy = ', (success/trails))



plt.subplot(121)
plt.plot(events, probability)
plt.xlabel ('No of trails')
plt.ylabel ('Probabilty values')


plt.subplot(122)
plt.plot (events, area)
plt.xlabel ('No of trails')
plt.ylabel ('Approx. area of quadarant')
plt.show()
