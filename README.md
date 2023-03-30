# jarvis-assistand
Jarvis is a voice-based personal assistant for Google Chrome that helps you increase productivity while browsing the web. With Jarvis, you can use voice commands to set timers, reminders, translate phrases, search the web, and much more.


## Some of Jarvis's features include:

* Timer: Simply say "set a timer for X minutes" and Jarvis will start counting down.

* Reminder: Set reminders for important tasks or events by saying "remind me to do X at Y time."

* Translation: Translate phrases or sentences from one language to another by saying "translate X to Y language."

* Web search: Look up information on the web by saying "search for X on Google."

* Weather: Check the weather in your area by saying "what's the weather like today?"

Jarvis is designed to make your web browsing experience more efficient and convenient. With its voice-based interface, you can easily perform tasks without having to type or click. Try out Jarvis today and see how it can improve your productivity!


## Here's a code snippet that I'm leaving to help you out with Jarvis, which I developed for my personal use.

``` 
javascript

<!DOCTYPE html>
<html>
  <head>
    <title>Artyom.js Chat Example</title>
  </head>
  <body>
    <h1>Artyom.js Chat Example</h1>
    <div id="chatlog"></div>
    <input type="text" id="userinput" />
    <button id="speakbtn">Speak</button>

    <script src="https://sdkcarlos.github.io/sites/artyom-js/releases/artyom.min.js"></script>
    <script>
      var artyom = new Artyom();

      // Start the voice recognition
      artyom.initialize({
        lang: "en-US",
        continuous: true,
        debug: true,
        listen: true,
      });

      // Add a command
      artyom.addCommands({
        indexes: ["hello", "hi", "hey"],
        action: function () {
          var response = "Hello there!";
          artyom.say(response);
          addToChatLog("Artyom: " + response);
        },
      });

      // Handle user input
      document.getElementById("speakbtn").addEventListener("click", function () {
        var userInput = document.getElementById("userinput").value;
        if (userInput) {
          artyom.say(userInput);
          addToChatLog("User: " + userInput);
          document.getElementById("userinput").value = "";
        }
      });

      // Add to chat log
      function addToChatLog(message) {
        var chatLog = document.getElementById("chatlog");
        var messageNode = document.createElement("p");
        messageNode.innerText = message;
        chatLog.appendChild(messageNode);
      }
    </script>
  </body>
</html>

```
I don't mean to boast, but mine is even better as it works with full voice commands. Using the Artyom.js library, I created a simple chat application where the user can write text in the input box and listen to Artyom's voice response by clicking the 'Speak' button. Additionally, Artyom can respond with a specific answer when the user says a certain command.

Creator and developer [Akif Garpe](https://github.com/akifgrape) 🔥
