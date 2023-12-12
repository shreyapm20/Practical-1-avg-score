# Score of student
marklist = [10,27,None,94,20,None,67,20,10,94,20,89,0,90,None,57,28,20,None,90,56]
 #n=int (imat "Enter no of students "))
 # for i in range(n):
 # mark = int(input (f"Enter marks (i+1) student :"))
 #marklist.append(mark)
print (marklist) 
total = 0
absent_student = 0
freq = {}
max_val = marklist [0] 
min_val =  marklist [0]
for mark in marklist:
      if mark == None: 
           absent_student += 1
      else:
           total += mark
           # calculate Max and min marks
           if mark < min_val:
                min_val = mark
           if max_val < mark: 
                max_val = mark
                #calculating frequency
           if freq.get(mark) == None:
                freq[mark]=1
           else:
                freq[mark] += 1
print ("a.Average Score of the class = ",total/len (marklist)) 
print ("b.Highest Score= ",max_val ,"and Lowest Score =",min_val)
print ("c. Number of absent student= ",absent_student)
highest_freq = 0
highest_freq_mark = 0
for mark in freq:
     if freq[mark] > highest_freq: 
          highest_freq = freq[mark] 
          highest_freq_mark=mark
print ("d. Mark with highest frequency:", highest_freq_mark)            
