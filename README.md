
# Histograms in matplotlib

### .  Univariate graph

### .  Use histograms for numerical variables only.

## Data Sets:

height_of_children_in_cms = np.array([100,100.70,101.5,102.3,103,103.2,103.5,104.5,105,106.2,107,100.7,102.3,102.3])

plt.hist(height_of_children_in_cms)

plt.title("Histogram of the height of children")

plt.show()

![Screenshot from 2025-04-04 14-51-14](https://github.com/user-attachments/assets/e9cb8ae9-6868-4759-b86b-4ff08e03be7c)

plt.hist(height_of_children_in_cms, color='g')

plt.title("Histogram of the height of children")

plt.xlabel("Height of children(in cms)")

plt.show()

![Screenshot from 2025-04-04 15-04-40](https://github.com/user-attachments/assets/88afd9f4-2849-4a61-b475-9b05e72afd01)


## Pie charts in matplotlib¶

. For categorical variables

fruits = ['Apples', 'Bananas', 'Strawberries','Oranges', 'Pears', 'Grapes']
count_of_fruits = [23, 17, 35, 29, 12, 41]

plt.pie(count_of_fruits, labels = fruits)

plt.show()


![Screenshot from 2025-04-04 15-09-02](https://github.com/user-attachments/assets/33ce305d-8438-489a-8e5b-9d52ba801c87)


# Subplots

x = np.linspace(-10,9,20)

print(x)

[-10.  -9.  -8.  -7.  -6.  -5.  -4.  -3.  -2.  -1.   0.   1.   2.   3.
   4.   5.   6.   7.   8.   9.]

### create a cubic function

y = x**3

plt.plot(x,y)

plt.show()

![Screenshot from 2025-04-04 15-43-10](https://github.com/user-attachments/assets/d71b539b-5d63-4efc-8643-083e3a5c19c7)


plt.subplot(2,2,1) #m - no. of rows, n-no. of columns, p=position of the current graph

plt.plot(x,y,'b*-')

plt.subplot(2,2,2)

plt.plot(x,y,'y--')

plt.subplot(2,2,3)

plt.plot(x,y,'m:')

plt.subplot(2,2,4)

plt.plot(x,y,'g--')

plt.show()

![Screenshot from 2025-04-04 15-48-52](https://github.com/user-attachments/assets/840e4a31-c3b8-4b5a-845b-288c15b5fe39)


plt.subplots_adjust(wspace=0.5) #wspace is used to adjust the spacing between the columns

plt.subplot(2,2,1) #m - no. of rows, n-no. of columns, p=position of the current graph

plt.plot(x,y,'b*-')

plt.subplot(2,2,2)

plt.plot(x,y,'y--')

plt.subplot(2,2,3)

plt.plot(x,y,'m:')

plt.subplot(2,2,4)

plt.plot(x,y,'g--')

plt.show()

![Screenshot from 2025-04-04 15-52-25](https://github.com/user-attachments/assets/59fc687d-178a-4a93-b300-1e8d3324f6f4)

plt.figure(figsize=(20,10))

plt.suptitle("Cubic Function Graphs", fontsize=20, fontweight=20, verticalalignment="bottom")

plt.subplot(2,2,1) #m - no. of rows, n-no. of columns, p=position of the current graph

plt.plot(x,y,'b*-')

plt.title("sub plot 1")

plt.subplot(2,2,2)

plt.plot(x,y,'y--')

plt.title("sub plot 2")

plt.subplot(2,2,3)

plt.plot(x,y,'m:')

plt.title("sub plot 3")

plt.subplot(2,2,4)

plt.plot(x,y,'g--')

plt.title("sub plot 4")

plt.tight_layout()

plt.show()

![Screenshot from 2025-04-04 15-55-04](https://github.com/user-attachments/assets/bcdf0e06-459d-426c-a18a-53e07c394b0f)


web_monday = [123, 645, 950, 1290, 1630, 1450,1034,1295,465,205,80]

web_tuesday = [95, 680, 889, 1145, 1670,1323,1119,1265,510,310,110]

web_wednesday = [105,630,700,1006,1520,1124,1239,1380,580,610,230]

time_hrs = [7,8,9,10,11,12,13,14,15,16,17]


plt.figure(figsize=(10,7))

plt.plot(time_hrs, web_monday, linewidth =2,linestyle="--", marker='*' , markersize = 8, label = "Website traffic on Monday" )

plt.plot(time_hrs, web_tuesday, linewidth =2,linestyle="-.", marker='^', markersize = 8, label = "Website traffic on Tuesday")

plt.plot(time_hrs, web_wednesday, linewidth =2, linestyle=":", marker='+', markersize = 10, label = "Website traffic on Wednesday")

plt.xticks(np.arange(6,18))

plt.legend(loc="upper right", bbox_to_anchor=(1.3,1) ) # to move the default position of the legend on the graph

plt.grid(True)

plt.show()

![Screenshot from 2025-04-04 15-58-09](https://github.com/user-attachments/assets/3f1a6f09-4598-46db-ac52-80de3f4c9f3f)


plt.figure(figsize=(20,10))

plt.suptitle("Website traffic analysis", fontsize = 20, verticalalignment="bottom")

plt.subplot(1,3,1)

plt.plot(time_hrs,web_monday,color='g',marker='o')

plt.title("Website traffic on Monday")

plt.xlabel("Time in hours spent on the website")

plt.ylabel("Number of customers on Monday")

plt.subplot(1,3,2)

plt.plot(time_hrs,web_tuesday,color='m',marker='o')

plt.title("Website traffic on Tuesday")

plt.xlabel("Time in hours spent on the website")

plt.ylabel("Number of customers on Tuesday")

plt.subplot(1,3,3)

plt.plot(time_hrs,web_wednesday,color='y',marker='o')

plt.title("Website traffic on Wednesday")

plt.xlabel("Time in hours spent on the website")

plt.ylabel("Number of customers on Wednesday")

plt.tight_layout()

plt.show()


![Screenshot from 2025-04-04 16-00-07](https://github.com/user-attachments/assets/5bf009f5-8bcb-4845-b277-52b8b919842d)











