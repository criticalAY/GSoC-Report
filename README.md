![GSoC logo](https://developers.google.com/open-source/gsoc/resources/downloads/GSoC-logo-horizontal.svg)

<h1 align="center">criticalAY - Ashish Yadav<br>2024 <br> 
  <a href="[AnkiDroid](https://github.com/ankidroid/Anki-Android)">AnkiDroid</a> </h1>

## Catch me up
| Handles | User Name |
| --- | --- |
| **Github** | [criticalAY](http://github.com/criticalAY) |
| **Twitter**  | [criticalAY_](https://x.com/criticalAY_) |
| **LinkedIn**  | [criticalAY](https://www.linkedin.com/in/criticalay/) |

## My mentors
| Name | Profile |
| --- | --- |
| **David Allison** | [Github](https://github.com/david-allison) |
| **Shridhar Goel**  | [LinkedIn](https://www.linkedin.com/in/shridhargoel/_) |

## Project summary

[AnkiDroid](https://github.com/ankidroid/Anki-Android) is a companion Android application for [Anki](https://github.com/ankitects/anki), a 
flashcards application that helps people learn and memorize a diverse variety of topics. 

[Instant Add Note Editor & Multimedia UI/UX](https://summerofcode.withgoogle.com/programs/2024/projects/HHr5HsjN) consisted of
* Streamlining the process of adding [cloze notes](https://docs.ankiweb.net/editing.html#cloze-deletion) to AnkiDroid
* Improving the app's UI & UX for adding multimdedia [Images/Drawing/Camera/Audio Recordings/Inserting files]
* Decoupling the app's multimedia handling

## What did I do?

### Community Bonding Period
Community Bonding is the initial time that Google gives to be involved in the community and activities that happen within an organization. Since the community was small and I already had been contributing and knew the community, it went very well. I enjoyed it and started my coding during this period so that I could compensate for the time that I wouldn't be active due to my university exams.

### Coding period
 - Week 1: I spent my time setting up the project and the necessary files required for the project: designs, icons, and other resources. I then set up the [Intent filters](https://developer.android.com/guide/components/intents-filters), text intents, etc. I created a rough layout for the instant editor dialog and shared it in the public channel and discord for discussion
- Week 2: I started working on the code and created a PR/s(pull request) so that the mentors can review it and give feedback.
  * The app used ActionMode.Callback to control adding additional items to the context menu in Text Fields. I extracted this for reuse in my project
  * UI improvements in the instant note editor dialog such as edit text fields, error/warning text, etc.
  * Implemented a feature to long press, select multiple words, and convert them to cloze using the extracted ActionMode.Callback.
 
- Week 3: Continued to work on the Instant Note Editor code.
  * Created an extension method for cloze fields, allowing for more efficient and reusable code when dealing with cloze deletions and insertions. This extension method helped in standardizing the way cloze fields are managed across the app.
  * Improved the error validation code: used the backend to validate, and displayed improved errors/warnings
  * We decided to migrate the business logic to a `ViewModel`.
    
- Week 4: Worked on the open PR handling the suggestions and feedback received from the mentors
  * Initially, we used EditText and Chip drawables for the user interface to display words. There were multiple limitations to this approach, and after a detailed discussion we shifted to using ChipGroups.
  * Updated logic for the cloze field, separating logic into a 'single tap mode' and 'advanced edit text' mode.
    
- Week 5: This week, I had university exams so my time was spent improving the open PRs
  
- Week 6: Created a PR to improve the Instant Editor business logic and started setting up the second part of the project: the Multimedia Editor.
  * Cloze number logic improvements such as the cloze patterns bug fixes and dialog discard logic setup for the Instant Note Editor.
  * Setting up Multimedia activity for the second sub-project.
    
- Week 7: Continued to work on the open Instant Note Editor PR and created a new PR for multimedia editor 
  * Continued to fix the Instant Note Editor bugs.
  * Implemented multimedia UI options for camera and gallery. This new feature allows users to seamlessly integrate multimedia content into their notes. Users can either take a new photo using the camera option or select an existing image from their gallery. This functionality enhances the note-taking experience by enabling richer, more dynamic content. The multimedia UI editor includes intuitive controls for adding, viewing, and managing multimedia elements within the notes, ensuring a user-friendly experience.
  * The multimedia editor feature is set to dev only, meaning it is currently accessible only to developers within the project. This ensures that the feature is thoroughly tested and refined before being released to a wider audience. It is not in the alpha stage yet, so it is kept out of the hands of regular users until it meets the necessary stability and usability standards.
    
- Week 8: Wrapped up Instant Note Editor and continued to work on Multimedia UI/UX.
  * Got Instant Note Editor ready for public use which will be released in a controlled manner i.e. alpha -> beta -> stable.
  * Set up Audio and Video clip options in Multimedia and created a PR.
    
- Week 9: Continued to work on the Multimedia UI/UX.
  * Resolved suggestions on the open Multimedia UI/UX PR.
  * Created PR for Audio Recording and Drawing options
    
- Week 10: Wrapping up Multimedia UI/UX
  * Resolved the suggestions and marked the Multimedia UI/UX ready for public use.


## Link to pull requests created as a part of GSoC by chronological order
 1. [Instant Note Editor to allow adding cloze card](https://github.com/ankidroid/Anki-Android/pull/16393)
 2. [Extract ActionMode.Callback from NoteEditor](https://github.com/ankidroid/Anki-Android/pull/16401)
 3. [Extension method to get cloze field name](https://github.com/ankidroid/Anki-Android/pull/16424)
 4. [Ese field check from backend and display error accordingly](https://github.com/ankidroid/Anki-Android/pull/16432)
 5. [Init: Instant Note Editor Activity](https://github.com/ankidroid/Anki-Android/pull/16497)
 6. [Enhancements: Instant Note Editor Improvements](https://github.com/ankidroid/Anki-Android/pull/16534)
 7. [New Multimedia UI](https://github.com/ankidroid/Anki-Android/pull/16673)
 8. [Enhancement: add long press listener on cloze button ](https://github.com/ankidroid/Anki-Android/pull/16735)
 9. [Refactor: cloze builder pattern for words](https://github.com/ankidroid/Anki-Android/pull/16736)
 10. [Refactor: use prefill value in integer dialog](https://github.com/ankidroid/Anki-Android/pull/16745)
 11. [Enable instant editor for public use](https://github.com/ankidroid/Anki-Android/pull/16760)
 12. [Enhacement: add Audio and Video multimedia options](https://github.com/ankidroid/Anki-Android/pull/16769)
 13. [Fix: cloze number incorrect on undo](https://github.com/ankidroid/Anki-Android/pull/16779)
 14. [Refactor: Multimedia options converted to sealed class](https://github.com/ankidroid/Anki-Android/pull/16796) *Closed after discussion*
 15. [Multimedia UI/UX: Add Drawing & Recording options and set multimedia public](https://github.com/ankidroid/Anki-Android/pull/16798)
 16. [Refactor: vibration methods to use Duration](https://github.com/ankidroid/Anki-Android/pull/16803)
 17. [Refactor: move audio package to multimedia package ](https://github.com/ankidroid/Anki-Android/pull/16816)

## Results

<details><summary>Before Instant Note Editor</summary>
  The user had to copy and paste the text in the app and then create a cloze note or share the copied text to AnkiDroid will
  opened the NoteEditor Screen: 
 <p align="center">
    <img alt="" src="media/legacy-editor.png" width="30%" height="30%">
</p>
</details>

<details><summary>After Instant Note Editor</summary>
 Users can select, and share selected text to AnkiDroid `Instant Note` will help them to create cloze notes without actually opening the app:
  <p align="center">
 <img alt="" src="media/cloze-editor.png" width="30%" height="30%">   
<img alt="" src="media/clozed-words.png" width="30%" height="30%">
    <img alt="" src="media/advance-edit.png" width="30%" height="30%">
</p>
</details>

<details><summary>Old Multimedia UI</summary>
 <p align="center">
    <img alt="" src="media/mm_o.png" width="30%" height="30%">
    <img alt="" src="media/mm_oi.png" width="30%" height="30%">
</p>
</details>

<details><summary>New Multimedia</summary>
 <p align="center">
    <img alt="" src="media/mm_b.png" width="30%" height="30%">
    <img alt="" src="media/mm_i.png" width="30%" height="30%">
</p>
</details>


## Plans after GSoC?
Having successfully fulfilled all the commitments outlined in my GSoC proposal, my focus now shifts towards further enhancing the quality and robustness of the codebase. One critical area that I plan to address is the creation of comprehensive test suites, including both Unit Tests and Android Tests. These tests are essential for ensuring the reliability and stability of the application, and I intend to develop them as part of my ongoing contributions to the project.

My journey with AnkiDroid does not end with the conclusion of GSoC. I am committed to continuing my involvement with the project, and leveraging the experience and knowledge I have gained to make meaningful contributions. By staying actively engaged with the AnkiDroid community, I aim to help maintain and improve the app, ensuring it continues to be a valuable tool for users worldwide.


