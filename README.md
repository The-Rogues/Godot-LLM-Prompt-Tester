# Godot-LLM-Prompt-Tester
A Godot project that utilizes the NobodyWho plugin to interface with a locally stored language model, aiming to run an AI chatbot on the user's hardware.

This project utalizes gemma-2-2b-it-Q4_K_M.gguf, which was downloaded from https://huggingface.co/bartowski/gemma-2-2b-it-GGUF/tree/main. Ideally, this project can use any gguf file/llm, but I haven't tested many, so there may be an exception. The latest version of Godot allows for the GGUF file to be stored in the same folder as the source files of the project. Godot does not natively understand gguf files, so they are not visible in the editor environment, howeveer they can be viewed in the computer's file system.

## How to open in Godot
* If you haven't already, download the latest version of the Godot game Engine from: https://godotengine.org/
* Download the zipfile from this Google drive (https://drive.google.com/file/d/1LNGbNQuuZklrUv74OxpxLgFYFjG4yEf5/view?usp=drive_link) and extract its contents somewhere that's easy to find
* Open Godot and click import
* Navigate to where you stored the extracted folder, click on the folder, then click ``Select this folder``
* Click ``Import`` with ``Edit now`` checked
* The project will open in the Godot editor

## How to change LLM/GGUF and run
* To change the LLM model, drag the gguf file of your choice into the same folder as the source files
* Once the new gguf file is in the folder, you can close the file manager and click on the ``NobodyWhoModel`` Node in the scene hierarchy
* After clicking the node, look at the properties inspector (Usually to the right of your screen) and click the file icon next to the ``Model Path`` property, which will open Godot's file navigator
* Click and open the gguf file you want to use
* You can then press the play icon to run the game
* Note: You will need a strong computer to successfully receive a response; otherwise, the program will close without errors. The specs the program was succesfully tested in detailed below

## Successful Hardware specs
* CPU: Intel(R) Core(TM) 15-10300h CPU @ 2.50GHz
* GPU 0: Intel(R) UHD Graphics (4139 MB total | 128 MB dedicated)
* GPU 1: NVIDIA GeForce GTX 1650 Ti
* Memory: 8.0 GB

## System Prompt
* If you click on the `NobodyWhoChat` Node, you will see that one of its properties includes a `System Prompt` text field. As far as I know, this field allows you to request a specific type of response from the AI, such as "Talk like a pirate" or "Respond with a single short sentence."
* I haven't tested it too much yet, but so far it feels effective.
