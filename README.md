# Boggle-Game-With-GUI

Overview:
  
  This project is a desktop implementation of the Boggle word game built using Java Swing.
  The goal of the project was to combine GUI development with game logic, file I/O, and controlled user interaction in a clean, maintainable way.

  Players form words by clicking adjacent letters on a 4×4 grid. Valid words are checked against a dictionary file and saved automatically. The game enforces adjacency rules and prevents reusing letters within the same word

Key Features:
  
  Interactive **4×4 letter grid** using Swing components
  
  Randomized board generation with vowels and consonants
  
  Enforced adjacency rules (horizontal, vertical, diagonal)
  
  Prevents selecting the same letter twice in a single word
  
  Dictionary-based word validation (minimum length: 3)
  
  Tracks unique words found during gameplay
  
  Saves valid words to a text file
  
  Reset functionality to clear the current word

Implementation Details
  
  The board is represented using a `JButton[][]`, allowing each button to function as both a UI element and part of the game state.
  
  Button clicks are handled using lambda-based `ActionListener`s for clarity and readability.
  
  Adjacency rules are enforced by tracking the previously selected cell (`lastRow`, `lastCol`).
  
  Words are built incrementally using a `StringBuilder` for efficiency.
  
  A dictionary is loaded from an external `words.txt` file using the class loader, keeping game data separate from logic.
  
  Valid words are written to `savedWords.txt` and stored in memory to prevent duplicates.


How to Run
  
  1. Ensure Java (JDK) is installed.

  2. Project structure should include:
    gui/BoggleGame.java
    words.txt

  3. Compile the program:
    javac gui/BoggleGame.java

  4. Run the program:
    java gui.BoggleGame


How to Play
  
  1. Click letters to begin forming a word.

  2. Each selected letter must be **adjacent** to the previous one.

  3. Letters cannot be reused within the same word.
  
  4. When a valid word is completed:

  It is saved to `savedWords.txt`
  
  The board resets automatically for the next word

  5. Use the **Reset** button to clear the current word manually.

     
Skills Demonstrated
  
  Java GUI development with Swing
  
  Event-driven programming
  
  State management across user interactions
  
  File input/output
  
  Data validation and control flow
  
  Designing user constraints through logic rather than UI limitations


Author: Mashroof Samin
