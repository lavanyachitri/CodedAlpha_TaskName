# CodedAlpha_TaskName
 [chatbot.py](https://github.com/user-attachments/files/29162686/chatbot.py)
import random

def simple_chatbot():
    """
    Note:-To stop or exit give exit or quit or bye

    """
    # Predefined responses to choose from randomly
    greetings = ["Hello!", "Hi there!", "Hey! How can I help you today?", "Hi! Nice to meet you.","Hey hi!!","Hey there!"]
    wishes1=["hey! good morning..","good morning :)","good morning,have a nice day"]
    wishes2=["good night","good night dear","good night,hope you had a great day!!","good night:)"]
    wishes3=["good afternoon","good afternoon dear..","good afternon:)"]
    print("Bot: Hello! I am a simple chatbot.")

    
    while True:
        # Get input from the user and remove extra spaces
        user_input = input("You: ").strip().lower()
        
        # Condition to exit the chat
        if user_input in ["exit", "quit", "bye"]:
            print("Bot: Goodbye! Have a great day!")
            break
            
        # Condition to check for greetings
        elif user_input in ["hi", "hello", "hey","heyy","hii","hi bot"]:
            # Pick and print a random greeting response
            print(f"Bot: {random.choice(greetings)}")
        #condition to greet to wish
        elif user_input in ["good morning","hey!good morning ","hey,good morning"]:
            print(f"Bot:{random.choice(wishes1)}")
        elif user_input in ["good night","hey!good night","hey,good night"]:  
            print(f"Bot:{random.choice(wishes2)}")
        elif user_input in ["hey!good afternoon","good afternoon","hey,good afternoon"]:
            print(f"Bot:{random.choice(wishes3)}")
        # Catch-all condition for unrecognized text
        else:
            print("Bot: I'm sorry, I'm the basic chatbot i can only greet you")

print(simple_chatbot.__doc__)
simple_chatbot()
