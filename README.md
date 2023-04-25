
from tkinter import *
root = Tk()
root.title("Simple Calculator")

entry = Entry(root, width=50,borderwidth=5)
entry.grid(row=0,column=0,columnspan=3,padx=15,pady=15)
def my_click(number):
    #entry.delete(0,END)
    current= entry.get()
    entry.delete(0,END)
    entry.insert(0,str(current)+str(number))

def my_click_clear():
    entry.delete(0,END)

def my_click_add():
    first_number= entry.get()
    entry.delete(0, END)
    global  f_number
    global math
    math= "addition"
    f_number= int(first_number)

def my_click_equal():
    second_number= entry.get()
    entry.delete(0, END)
    if math == "addition":
        entry.insert(0,f_number+int(second_number))
    if math == "subtraction":
        entry.insert(0,f_number-int(second_number))
    if math == "multiplication":
        entry.insert(0,f_number*int(second_number))
    if math == "division":
        entry.insert(0,f_number/int(second_number))
def my_click_subtract():
    first_number = entry.get()
    entry.delete(0, END)
    global f_number
    global math
    math = "subtraction"
    f_number = int(first_number)
def my_click_multiply():
    first_number = entry.get()
    entry.delete(0, END)
    global f_number
    global math
    math = "multiplication"
    f_number = int(first_number)
def my_click_divide():
    first_number = entry.get()
    entry.delete(0, END)
    global f_number
    global math
    math = "division"
    f_number = int(first_number)

my_button_1 = Button(root, text="1", command= lambda: my_click(1), padx=40, pady=20)
my_button_2 = Button(root, text="2", command= lambda: my_click(2), padx=40, pady=20)
my_button_3 = Button(root, text="3", command= lambda: my_click(3), padx=40, pady=20)
my_button_4 = Button(root, text="4", command= lambda: my_click(4), padx=40, pady=20)
my_button_5 = Button(root, text="5", command= lambda: my_click(5), padx=40, pady=20)
my_button_6 = Button(root, text="6", command= lambda: my_click(6), padx=40, pady=20)
my_button_7 = Button(root, text="7", command= lambda: my_click(7), padx=40, pady=20)
my_button_8 = Button(root, text="8", command= lambda: my_click(8), padx=40, pady=20)
my_button_9 = Button(root, text="9", command= lambda: my_click(9), padx=40, pady=20)
my_button_0 = Button(root, text="0", command= lambda: my_click(0), padx=40, pady=20)
my_button_clear = Button(root, text="Clear", command= my_click_clear, padx=90, pady=20)
my_button_add = Button(root, text="+", command= my_click_add, padx=40, pady=20)
my_button_equal = Button(root, text="=", command= my_click_equal, padx=100, pady=20)
my_button_subtract = Button(root, text="-", command= my_click_subtract, padx=40, pady=20)
my_button_multiply = Button(root, text="*", command= my_click_multiply, padx=40, pady=20)
my_button_divide = Button(root, text="/", command= my_click_divide, padx=40, pady=20)
my_button_1.grid(row=3, column=0)
my_button_2.grid(row=3, column=1)
my_button_3.grid(row=3, column=2)
my_button_4.grid(row=2, column=0)
my_button_5.grid(row=2, column=1)
my_button_6.grid(row=2, column=2)
my_button_7.grid(row=1, column=0)
my_button_8.grid(row=1, column=1)
my_button_9.grid(row=1, column=2)
my_button_0.grid(row=4, column=0)
my_button_clear.grid(row=4, column=1,columnspan=2)
my_button_add.grid(row=5, column=0)
my_button_equal.grid(row=5, column=1,columnspan=2)
my_button_subtract.grid(row=6, column=0)
my_button_multiply.grid(row=6, column=1)
my_button_divide.grid(row=6, column=2)
root.mainloop()
