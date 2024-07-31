# Artificial-intelligence- task 1

# Define a dictionary of rules and responses
rules = {
    "hello": "Hello! How can I assist you today?",
    "hi": "Hi! What's on your mind?",
    "how are you": "I'm doing well, thanks! How about you?",
    "what is your name": "My name is Chatty, nice to meet you!",
    "default": "I didn't understand that. Can you please rephrase?"
}

def respond(user_input):
    # Convert user input to lowercase
    user_input = user_input.lower()
    
    # Check if the user input matches a rule
    for rule in rules:
        if rule in user_input:
            return rules[rule]
    
    # If no rule matches, return the default response
    return rules["default"]

# Test the chatbot
while True:
    user_input = input("You: ")
    response = respond(user_input)
    print("Chatty:", response)
