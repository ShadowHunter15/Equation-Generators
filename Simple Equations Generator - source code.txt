import random
print("This is an equation generator.")
print("Round your answers to two decimal place where necesary");
list_or_test = input("Do you want it as a test or as a list (for worksheets and copyinng purposes) enter list for list and test for test: ");
if list_or_test =="test":

  Z = int(input("Please enter the number of questions you want: "));
  for i in range(Z):
    A = random.randint(-20, 35);
    B = random.randint(-1000, 1000);
    Y = random.randint(1, 1000);
    M = " + " 
    if A == 0:
        continue;
    if B < 0:
        M = " ";
    print(str(i + 1) + str(". ") + str(Y) +  " = " + str(A) + "x" + M + str(B));

    input1 = input("Show answer? y for yes and anykey for no ");
    if input1 == "y":
          if B > 0:
             First_step = Y + B;
             Second_step = First_step / A; 
             Rounded_Second_Step = round(Second_step, 2);
             print("                                                   Answer: " + str(Rounded_Second_Step));
             
          else:
             First_step = Y - B;
             Second_step = First_step / A; 
             Rounded_Second_Step = round(Second_step, 2);
             print("                                                   Answer: " + str(Rounded_Second_Step));
    else:
        break;
elif list_or_test == "list":

 Z = int(input("Please enter the number of questions you want: "));
 answers = [];

 for i in range(Z):
    A = random.randint(2, 35);
    a = random.randint(-20, -2);
    B = random.randint(1, 1000);
    Y = random.randint(1, 1000);
    Aa = random.randint(1, 2);
    if Aa == 1:
      print(str(i + 1) + str(". ") + str(Y) + " = " + str(A) + "x" + " + " + str(B));
      First_step = Y - B;
      Second_step = First_step / A;  
      Answer = round(Second_step, 2);
      answers.append(Answer)
    elif Aa == 2:
        print(str(i + 1) + str(". ") + str(Y) + " = " + str(a) + "x" + " + " + str(B));
        First_step = Y - B;
        Second_step = First_step / a;  
        Answer = round(Second_step, 2);
        answers.append(Answer);
 print("")
 print("")
 print("---------------------------------------------------------------------------------------------------------------------")
 print("")
 print("")   
 for i in range(len(answers)):
            print("The answer for question " + str(i + 1) + " is: " + str(answers[i]));     
    

for zz in range(1):
  input("Press anykey to quit: ")


    

     
     

