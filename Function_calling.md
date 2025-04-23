Since LLM's have knowledge only on the Pre-Trained data and not on current events like the Weather today etc

We have Function calling to solve this problem

We can define a Function that provides details about the weather today and pass it to the functions parameter

  Example:
    def get_current_weather(Location):
      # apis for getting the weather today
    
    
    function=[
    {
        "name": "get_current_weather",
        "description": "Get the current weather in a given location",
        "parameters": {
            "type": "object",
            "properties": {
                "location": {
                    "type": "string",
                    "description": "The city and state, e.g. San Francisco, CA",
                },
                "unit": {"type": "string", "enum": ["celsius", "fahrenheit"]},
            },
            "required": ["location"],
        },
    }
    ]
    
    
    response=openai.ChatCompletion.Create(
            model="gpt-3.5-turbo",
            messages=messages,
            functions=function,
            }
