# Health-CheakUp
name = input("Enter your Name: \n")
age = int(input("Ente your age: \n"))
hight = float(input("Enter your hight in cm:\n"))
waight = float(input("Enter your waight in kg: \n"))
avg_male_waight=hight-100
avg_female_waight= hight-103
gender = input("Enter your gender\n(M for male) \n(F for female)\n")
if gender == "M":
    print("Hello Mr.", name, "How are you .\nWelcome to your health cheakup.")
    health_rea = waight - avg_male_waight
    if health_rea == 0:
        print('you have a good health')
    elif health_rea <= (-1) and health_rea >= (-5):
        print('This is not something to worry about, smile and take care of yourself.\n')
    elif health_rea <= (-5):
        print('You are losing waight, pay attention to your health and take a protein rich diet.\n  You have to gain',
              abs(round(health_rea, 2)), 'Kg for better health')
    elif health_rea >= 1 and health_rea<= 5 :
        print('This is not something to worry about, smile and take care of yourself.\n')
    elif health_rea> 5 :
        print('You are getting too fat, your weight is',health_rea,' more than normal; You should eat a low fat diet\n')
    else:
        print('Enter the correct detail.')
elif gender == "F":
    print("Hi Miss.", name, "How are you .\nWelcome to your health cheakup.")
    fhealth_rea = waight - avg_female_waight
    if fhealth_rea == 0:
        print('you have a good health')
    elif fhealth_rea <= (-1) and fhealth_rea >= (-5):
        print('This is not something to worry about, smile and take care of yourself.\n')
    elif fhealth_rea <= (-5):
        print('You are losing weight, pay attention to your health and take a protein rich diet.\n  You have to gain',
              abs(round(fhealth_rea, 2)), 'Kg for better health')
    elif fhealth_rea >= 1 and fhealth_rea <= 5:
        print('This is not something to worry about, smile and take care of yourself.\n')
    elif fhealth_rea > 5:
        print('You are getting too fat, your weight is', fhealth_rea, 'more than normal; You should eat a low fat diet\n')
    else:
        print('Enter the correct detail.')

else:
    print('Please Enter Correct Detail.')
