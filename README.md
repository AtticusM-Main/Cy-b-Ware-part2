# Cy-B-ware — Part 2
https://youtu.be/WUxAuFdHelc
A C# console chatbot that teaches users cybersecurity best practices.
What this part adds
•	Plays a voice greeting (WAV) when the app starts.
•	Keeps a remembered user name (prompts until a non-empty name is entered).
•	Displays an ASCII art logo on startup.
•	Provides interactive Q&A guidance about basic cybersecurity hygiene.

Project layout
•	Program.cs — program entry
•	Chatbot.cs — chatbot logic, PlayGreeting() and conversational features
•	greeting.wav — startup audio greeting (place in project root / output folder)
•	README.md — project documentation
•	.NET 8 SDK
•	NuGet package: System.Windows.Extensions
•	This provides System.Media.SoundPlayer on non-Windows stacks/modern .NET where needed.
•	Install via Visual Studio NuGet Package Manager or: dotnet add package System.Windows.Extensions

Build & run
•	From the project folder: dotnet build dotnet run
•	Or open the solution in Visual Studio and press Run.

Audio/greeting
•	Chatbot.PlayGreeting() uses a local WAV file and System.Media.SoundPlayer.
•	Ensure greeting.wav is copied to the output (set Build Action = Content and Copy to Output Directory = Always/If Newer in project file or via Visual Studio file properties).
Notes
•	ASCII logo created using Figlet (e.g., Spectre.Console figlet generator). No runtime dependency required if the ASCII art is embedded as text.
•	Input validation ensures the user must enter a non-empty name before proceeding.
Contributing
•	Fork, add small focused changes, and open a pull request.
•	Keep changes limited to the scope of the chatbot and follow existing coding style.
