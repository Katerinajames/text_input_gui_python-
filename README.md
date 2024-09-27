 StringVar is an object variable that holds characters .In our case it holds the  string of our label  (self.label_text=tk.StringVar()) 
 
 self.label_text.set("My name is:") we set the value of our string 
 
 self.name_text=tk.StringVar() Our next step is to hold  the name that the user will enter 
 
 self.label=tk.Label(self ,textvar= self.label_text ) We create the  Label  and we assign the string value ("My name is:") 
 
 self.label.pack(fill=tk.BOTH, expand=1, padx=100, pady=10) We place our label within our app window 
 
 self.name_entry=tk.Entry(self, textvar=self.name_text) We create an entry widget so that the user can enter his/her name (for additional information  https://www.geeksforgeeks.org/python-tkinter-entry-widget/)
 
 self.name_entry.pack(fill=tk.BOTH, expand=1, padx=20, pady=20)We place our entry widget  within our app window 
 
 hello_button=tk.Button(self, text="Say Hello",command=self.say_hello) We create a hello_button 
 
 hello_button.pack(side=tk.LEFT, padx=(20, 0), pady=(0, 20)) The hello_button is placed within our window 
 
 goodbye_button = tk.Button(self, text="Say Goodbye",command=self.say_goodbye) We create a goodbye _button
 
 goodbye_button.pack(side=tk.RIGHT, padx=(0, 20), pady=(0, 20))The goodbyre _button is placed within our window 
 def say_hello(self):
		message = "Hello there " + self.name_entry.get()
		msgbox.showinfo("Hello", message)   The implementation of the function  say_hello helps to print the users name in a pop up window 
 def say_goodbye(self):
		if msgbox.askyesno("Close Window?", "Would you like to  close this window?"):
			message = "Window will close in 2 seconds - goodybye " + self.name_text.get()
			self.label_text.set(message)
			self.after(2000, self.destroy)
		else:                    
                   msgbox.showinfo("Not Closing", "Great! This window will stay open.") The implementation of the function  say_goosbye   provides the user with the choice to close the window 
		    

Our source  is the book "Tkinter gui programming by example by  David Love 
