# register-form-using-python

from tkinter import *
root = Tk ()
root.geometry("500x300")

def getvals():
    print("Accepted")
    
#Heading
Label(root, text="python Registratation form",font="arial 15 bold").grid(row=0,column=3)

#Field name
name = Label(root, text='Name')
phone = Label(root, text='Phone')
gender = Label(root, text='Gender')
group = Label(root, text='Group')

#packing fields
name.grid(row=1,column=2)
phone.grid(row=2,column=2)
gender.grid(row=3,column=2)
group.grid(row=4,column=2)

#variable for storing data
namevalue = StringVar
phonevalue = StringVar
gendervalue = StringVar
groupvalue = StringVar
checkvalue = IntVar

#creating entry field
nameentry = Entry(root, textvariable = namevalue)
phoneentry = Entry(root, textvariable = phonevalue)
genderentry = Entry(root, textvariable = gendervalue)
groupentry = Entry(root, textvariable = groupvalue)

#packing entry field
nameentry.grid(row=1,column=3)
phoneentry.grid(row=2,column=3)
genderentry.grid(row=3,column=3)
groupentry.grid(row=4,column=3)

#creating checkbox
checkbtn =Checkbutton(text="remember me", variable= checkvalue)
checkbtn.grid(row=5,column=3)

#submit button 
Button(text="Submit", command=getvals).grid(row=6,column=3)

root.mainloop()
