# Building Calculator

from tkinter import *

root = Tk()

# Creating Window
root.geometry('1000x800')
root.title('The GUI calculator')
root["bg"] = "purple1"

# Declaring a Click() function


def click(event):
    global input_value
    text = event.widget.cget("text")

    # declaring conditions for =, c
    if text == "=":
        if input_value.get().isdigit():
            value = int(input_value.get())
        else:
            value = eval(screen.get())
        input_value.set(value)
        screen.update()
    elif text == "C":
        input_value.set("")
        screen.update()
    else:
        input_value.set(input_value.get() + text)
        screen.update()


# Declaring variables
input_value = StringVar()
input_value.set("0")

# Creating entries
screen = Entry(root, textvariable=input_value, font="lucida 30 bold")
screen.pack(fill=X, padx=20, pady=10)

# Creating frame for buttons
frame = Frame(root, bg="purple1")
frame.pack()

# Buttons

button = Button(frame, text="9", padx=15, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=15, pady=5)
button.bind('<Button-1>', click)

button = Button(frame, text="8", padx=15, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=15, pady=5)
button.bind('<Button-1>', click)

button = Button(frame, text="7", padx=15, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=15, pady=5)
button.bind('<Button-1>', click)

# Creating frame for buttons
frame = Frame(root, bg="purple1")
frame.pack()

# Buttons

button = Button(frame, text="6", padx=15, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=15, pady=5)
button.bind('<Button-1>', click)

button = Button(frame, text="5", padx=15, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=15, pady=5)
button.bind('<Button-1>', click)

button = Button(frame, text="4", padx=15, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=15, pady=5)
button.bind('<Button-1>', click)

# Creating frame for buttons
frame = Frame(root, bg="purple1")
frame.pack()

# Buttons

button = Button(frame, text="3", padx=15, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=15, pady=5)
button.bind('<Button-1>', click)

button = Button(frame, text="2", padx=15, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=15, pady=5)
button.bind('<Button-1>', click)

button = Button(frame, text="1", padx=15, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=15, pady=5)
button.bind('<Button-1>', click)

# Creating frame for buttons
frame = Frame(root, bg="purple1")
frame.pack()

# Buttons

button = Button(frame, text="0", padx=15, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=13, pady=5)
button.bind('<Button-1>', click)

button = Button(frame, text="+", padx=15, pady=5, font="lucida 28 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=17, pady=5)
button.bind('<Button-1>', click)

button = Button(frame, text="-", padx=16, pady=0, font="lucida 33 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=15, pady=0)
button.bind('<Button-1>', click)

# Creating frame for buttons
frame = Frame(root, bg="purple1")
frame.pack()

# Buttons

button = Button(frame, text="*", padx=20, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=14, pady=5)
button.bind('<Button-1>', click)

button = Button(frame, text="/", padx=20, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=14, pady=5)
button.bind('<Button-1>', click)

button = Button(frame, text="%", padx=15, pady=5, font="lucida 26 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=13, pady=5)
button.bind('<Button-1>', click)

# Creating frame for buttons
frame = Frame(root, bg="purple1")
frame.pack()

# Buttons

button = Button(frame, text="=", padx=14, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=15, pady=5)
button.bind('<Button-1>', click)

button = Button(frame, text="C", padx=13, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=13, pady=5)
button.bind('<Button-1>', click)

button = Button(frame, text=".", padx=19, pady=5, font="lucida 30 bold", relief=RAISED, borderwidth=5)
button.pack(side=LEFT, padx=18, pady=5)
button.bind('<Button-1>', click)


root.mainloop()
