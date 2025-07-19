# hangman-game
def get_bot_reply(user_input):
    """
    Return a response based on user input.
    """
    user_input = user_input.lower().strip()

    if user_input in ['hello', 'hi', 'hii']:
        return "Hi there! May i can help me sir"
    elif user_input in ['how are you', 'how are you doing']:
        return "I'm fine, thanks! How can I help you?"
    elif user_input in ['bye', 'goodbye', 'exit']:
        return "Goodbye! Have a nice day!"
    elif user_input in ['what is your name']:
        return "I'm a simple chatbot created using Python by abhay."
    else:
        return "Sorry, I didn't understand that."

def start_chatbot():
    """
    Start the chatbot conversation loop.
    """
    print("🤖 Chatbot: Hello! Type something to start chatting. Type 'bye' to exit.")

    while True:
        user_input = input("You: ")
        reply = get_bot_reply(user_input)
        print("🤖 Chatbot:", reply)

        if user_input.lower() in ['bye', 'goodbye', 'exit']:
            break

# Run the chatbot
if __name__ == "__main__":
    start_chatbot()
