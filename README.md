Here's a funny short readme for your Kanye-inspired app, including instructions for getting it up and running.

Kanye Says...
"You may be talented, but you're not Kanye West."

Ever find yourself in a creative rut? Facing a problem that seems insurmountable? Asking yourself, "What would Yeezus do?"

Fear not. This app is your direct line to the unparalleled wisdom of Mr. West himself. With the click of a button, receive a profound, and definitely not random, quote from the mind of a genius. Let Kanye's words guide you, inspire you, and remind you that your biggest problem is you're not him.

Features
Infinite Wisdom: A boundless stream of Kanye quotes, delivered fresh to your desktop.
Minimalist Design: Because genius doesn't need clutter.
Aesthetic Background: A visually pleasing backdrop for your daily dose of inspiration.
The Man Himself: A clickable Kanye head to summon his knowledge. What more could you want?
Getting Started: A Guide for the Chosen
To get this divine inspiration flowing on your machine, you'll need to follow these simple steps.

Prerequisites
Python: Make sure you have Python 3 installed. If not, go get it. What are you waiting for?
Pip: This should come with your Python installation.
Installation & Setup
Clone this divine repository or create the files yourself:

Create a new folder for your project. Inside that folder, you'll need three things:

main.py (or whatever you want to call your Python script)
background.png (a 300x414 pixel image for the background)
kanye.png (a small image of Kanye's head for the button)
Install the necessary libraries:

Open your terminal or command prompt and run the following command. This will install the requests library, which is crucial for communicating with the digital ether of Kanye's mind. Tkinter comes standard with Python, because even Python knows what's good.

Bash

pip install requests
Add the code:

Paste the following code into your main.py file:

Python

from tkinter import *
import requests



def get_quote():
    response = requests.get("https://api.kanye.rest/")
    response.raise_for_status()
    data = response.json()
    quote = data["quote"]
    canvas.itemconfig(quote_text, text=quote)



window = Tk()
window.title("Kanye Says...")
window.config(padx=50, pady=50)

canvas = Canvas(width=300, height=414)
background_img = PhotoImage(file="background.png")
canvas.create_image(150, 207, image=background_img)
quote_text = canvas.create_text(150, 207, text="Kanye says..", width=250, font=("Arial", 20, "bold"), fill="white")
canvas.grid(row=0, column=0)

kanye_img = PhotoImage(file="kanye.png")
kanye_button = Button(image=kanye_img, highlightthickness=0, command=get_quote)
kanye_button.grid(row=1, column=0)



window.mainloop()
(Note: I took the liberty of slightly reducing the font size so that more of Kanye's wisdom can fit on the screen. You're welcome.)

Find your images:

You'll need to find a background.png and a kanye.png and save them in the same folder as your Python script.
For background.png, something visually interesting but not too distracting works best. A moody sky, a brutalist architecture photo, you get the vibe.
For kanye.png, a transparent image of Kanye's head is highly recommended for maximum aesthetic.
Run the application:

In your terminal, navigate to your project folder and run:

Bash

python main.py
Receive the gospel.

Click the Kanye button and let the inspiration wash over you.

"I will go down as the voice of this generation, of this decade, I will be the loudest voice."

Now you have a piece of that voice on your desktop. Use it wisely. Or don't. He's not the boss of you. But he is a genius.
