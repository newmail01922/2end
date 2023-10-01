+++
title = "Navigating the Course"
date = 2020-08-29T16:48:44-07:00
weight = 10
+++

The course exercises are free and open source. The content of this webpage is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons CC-By-ND 4.0 License</a>.

### Suggesting Changes

![Edit Page](/00_course_intro/images/edit-page.png?classes=shadow&outline&width=10pc)

{{% notice tip %}}
All materials are hosted on GitHub, and suggesting changes via Pull Requests are welcome. Just click the Edit this page button on the top right corner of any course page. 
{{% /notice %}}

### Navigation

View the course contents in the side bar on the left.

#### Arrows

The course can be navigated sequentially to the page before or after via the left and right arrows on each page.

![Navigate](/00_course_intro/images/arrows.png?classes=shadow&outline&width=10pc)

{{% notice tip %}}
You can also use the left and right keyboard arrows to navigate between pages.
{{% /notice %}}

#### Breadcrumbs
import random

# List of words for the game
word_list = ["apple", "banana", "cherry", "grape", "orange", "strawberry", "watermelon"]

# Choose a random word from the list
word_to_guess = random.choice(word_list)

# Initialize variables
attempts = 6
guessed_letters = []

# Display initial message
print("Welcome to the Word Guessing Game!")
print("Try to guess the word. You have", attempts, "attempts.")

# Main game loop
while attempts > 0:
    # Display the word with dashes for missing letters
    display_word = ""
    for letter in word_to_guess:
        if letter in guessed_letters:
            display_word += letter
        else:
            display_word += "_"

    print(display_word)

    # Ask the user for a letter guess
    guess = input("Guess a letter: ").lower()

    # Check if the guess is a single letter and not guessed before
    if len(guess) == 1 and guess.isalpha() and guess not in guessed_letters:
        guessed_letters.append(guess)

        # Check if the guess is in the word
        if guess in word_to_guess:
            print("Correct guess!")
        else:
            print("Incorrect guess.")
            attempts -= 1
    else:
        print("Invalid input. Please guess a single letter you haven't guessed before.")

    # Check if the user has guessed the entire word
    if set(word_to_guess).issubset(guessed_letters):
        print("Congratulations! You've guessed the word:", word_to_guess)
        break

# Check if the user won or lost
if attempts == 0:
    print("Game over! You've run out of attempts. The word was:", word_to_guess)


![Header](/00_course_intro/images/header.png?classes=shadow&outline)


Use the breadcrumb links on the floating header of each page to jump between related sections.


#### Table of Contents


![Table of Contents](/00_course_intro/images/toc.png?classes=shadow&outline&width=25pc)


Click on the "Table of Contents" Icon in the page header to jump between sections in the page.

### Expanding Sections

![Expand Section](/00_course_intro/images/expand-section.png?classes=shadow&outline&width=7pc)


Sometimes additional instructions or information will be available via the expand section arrow. Keep an eye out for this icon:



### Copying Code

To copy code and commands, click on the clipboard icon ((<i class='fa fa-clipboard-list'></i>) on the top right of any code box.

Try it now by copying the code below and pasting it into a note.

```python
def greeting():
    print("Hello, World!")
```

{{% notice tip %}}
You can even copy code intended for the Python REPL. The prompt characters won't be copied over.
{{% /notice %}}

### Searching

![Search](/00_course_intro/images/search.png?classes=shadow&outline&width=15pc)

The whole course is searchable via the search bar on the top left.

### Clearing History of Read Pages

![Clear History](/00_course_intro/images/clear_history.png?classes=shadow&outline&width=10pc)


Once a section is read, a check mark will appear to the right of that section. To clear it, hit the "Clear History" button at the bottom of the table of contents on the left hand side.

{{% notice info %}}
The course material is heavy in information and links. I suggest that you follow the links **after class** as a source of additional information, so that you don't get distracted from the important material.
{{% /notice %}}
