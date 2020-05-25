# oye-s-matplotlib
#first we import the necessary python libraries we need
import matplotlib.pyplot as plt
%matplotlib inline
import numpy as np
x = np.arange(0,20)
y = x*2
z = x**2

#we create a plot figure
fig = plt.figure()

#then we add our axes
ax = fig.add_axes([0,0,1,1])
ax.plot(x,y)

#we label the axes and give a title
ax.set_xlabel('x-axis')
ax.set_ylabel('y-axis')
ax.set_title('Title')

#the output below is the result we get from the code above
Text(0.5, 1.0, 'Title')

#we call the variable 'x' to get our points for the x-axis
x
array([ 0,  1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11, 12, 13, 14, 15, 16,
       17, 18, 19])
#we do the same for variable 'y' to get the points for our y-axis
y
array([ 0,  2,  4,  6,  8, 10, 12, 14, 16, 18, 20, 22, 24, 26, 28, 30, 32,
       34, 36, 38])
#we do the same for the z-axis
z
array([  0,   1,   4,   9,  16,  25,  36,  49,  64,  81, 100, 121, 144,
       169, 196, 225, 256, 289, 324, 361], dtype=int32)
#we can also do subplots i.e constructing a smaller plot in a larger one
fig = plt.figure()

#add axes to our respective plots(plot one i.e the larger plot)
ax1 = fig.add_axes([0,0,1,1])

#add axes for plot two(smaller plot)
ax2 = fig.add_axes([0.2,0.5,.2,.2])

#then we input the commands below to visualize our plots
ax1.plot(x,y)
ax2.plot(x,y)

#the commands below are for giving titles for our plots
ax1.set_title('larger plot')
ax2.set_title('smaller pot')
Text(0.5, 1.0, 'smaller pot')

fig = plt.figure()

ax1 = fig.add_axes([0,0,1,1])
ax2 = fig.add_axes([0.2,0.5,.4,.4])
ax1.plot(x,y,z)
ax2.plot(x,y)
ax1.set_title('larger plot')
ax1.set_xlabel('x')
ax1.set_ylabel('z')
ax2.set_title('smaller plot')
ax2.set_xlabel('x')
ax2.set_ylabel('y')
ax2.set_xlim([20,22])
ax2.set_ylim([30,35])
(30.0, 35.0)

fig,axes = plt.subplots(nrows=1,ncols=2) #we can also customize our plots

#we can choose different colours for the plot line, here i chose red
#the term lw stands for line width i.e how thick we want our line to be
#'marker' is for marking points on our plots,you can choose a different markers like '*', i chose 'o'
#for plot 1 and '*' for plot 2
#marker size is for thickening our marker , i set mine to 3
axes[0].plot(x,y,color='red',lw=.5,marker='o',markersize='3')
axes[0].set_title('maths')
axes[1].plot(x,z,color='green',lw=.5,marker='*',markersize='4')
axes[1].set_title('english')

#the command below is for making our output neat incase we have any over laps
plt.tight_layout()

fig,axes = plt.subplots(nrows=1,ncols=2, figsize=(10,2))
#another example only that in this case i adjusted the figure size by setting 'figsize' to (10,2)
axes[0].plot(x,y,color='red',lw=.5,marker='o',markersize='3')
axes[0].set_title('maths')
axes[1].plot(x,z,color='green',lw=.5,marker='*',markersize='2')
axes[1].set_title('english')
plt.tight_layout()

#quite easy, yeah?...lol
#end...

 
